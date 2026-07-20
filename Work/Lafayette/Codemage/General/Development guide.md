# CodeMage: Development Environment & Testing Guide

## Overview

This guide sets up a three-tier environment pipeline for CodeMage:

| Environment    | URL                  | Supabase     | Stripe    | Purpose                     |
| -------------- | -------------------- | ------------ | --------- | --------------------------- |
| **Local dev**  | localhost:3000       | Dev project  | Test keys | Daily coding & feature work |
| **Staging**    | preview.codemage.dev | Dev project  | Test keys | Test before shipping        |
| **Production** | www.codemage.dev     | Prod project | Live keys | Real users                  |

---

## Part 1: Supabase — Two Separate Projects

This is the most important structural decision. You need **two Supabase projects**: one for dev/staging, one for production. Never connect local or preview deploys to your production database.

### Step 1 — Create a dev Supabase project

1. Go to [supabase.com](https://supabase.com), open your org
2. Click **New project** → name it `codemage-dev`
3. Set a database password and save it in 1Password or similar
4. Once created, go to **Project Settings → API** and copy:
   - `Project URL` (looks like `https://abcxyz.supabase.co`)
   - `anon public` key
   - `service_role` key (keep this secret — never put it in client-side code)

### Step 2 — Migrate your schema to the dev project

Run your existing migrations against the new dev project. The easiest way:

```bash
# From your project root
cd /Users/stellabella/desktop/CodeMage/platform

# Link Supabase CLI to your dev project
npx supabase link --project-ref YOUR_DEV_PROJECT_REF

# Push your migrations
npx supabase db push
```

If you don't have a `supabase/migrations/` folder yet, you can dump the current schema from prod:

```bash
# Pull current prod schema as a migration file
npx supabase db pull --linked
```

### Step 3 — Rename your prod project (recommended)

In the Supabase dashboard, rename your existing project to `codemage-prod` so it's unmistakably clear which is which.

---

## Part 2: Environment Variables

### Local — `.env.local`

This file lives at the project root and is **never committed to git** (it should already be in your `.gitignore`).

```bash
# Supabase (DEV project)
NEXT_PUBLIC_SUPABASE_URL=https://YOUR-DEV-PROJECT.supabase.co
NEXT_PUBLIC_SUPABASE_ANON_KEY=eyJ...dev...
SUPABASE_SERVICE_ROLE_KEY=eyJ...dev...service...

# App
NEXT_PUBLIC_APP_URL=http://localhost:3000

# Anthropic
ANTHROPIC_API_KEY=sk-ant-...

# Stripe (TEST keys — always start with sk_test_ and pk_test_)
NEXT_PUBLIC_STRIPE_PUBLISHABLE_KEY=pk_test_...
STRIPE_SECRET_KEY=sk_test_...
STRIPE_WEBHOOK_SECRET=whsec_...  # from: stripe listen --forward-to localhost:3000/api/webhooks/stripe

# Resend (can use test mode locally)
RESEND_API_KEY=re_...
```

### Vercel — Environment Variable Setup

In the Vercel dashboard for `codemage`:

1. Go to **Settings → Environment Variables**
2. For each variable, you choose which environments it applies to:
   - **Preview** (staging): use dev Supabase URL/keys, Stripe test keys
   - **Production**: use prod Supabase URL/keys, Stripe live keys

**Critical: `NEXT_PUBLIC_APP_URL`**
- Preview: `https://preview.codemage.dev` (or your Vercel preview URL pattern)
- Production: `https://www.codemage.dev` (with www — required for Stripe webhooks)

### How to add variables in Vercel

```
Dashboard → Your project → Settings → Environment Variables → Add

Name: NEXT_PUBLIC_SUPABASE_URL
Value: https://YOUR-DEV.supabase.co
Environments: ✅ Preview  ☐ Production

Name: NEXT_PUBLIC_SUPABASE_URL  
Value: https://YOUR-PROD.supabase.co
Environments: ☐ Preview  ✅ Production
```

---

## Part 3: Git Branch Strategy

Keep it simple. Three branches map to your three environments:

```
main          → Production (www.codemage.dev)
staging       → Staging preview on Vercel
feature/xyz   → Local dev, creates its own Vercel preview URL
```

### Workflow for new features

```bash
# 1. Branch off main
git checkout main && git pull
git checkout -b feature/wave2-promo-codes

# 2. Build & test locally
# ... code in Cursor / Claude Code ...
npm run test        # unit tests
npm run test:e2e    # Playwright (optional locally)

# 3. Push to GitHub — Vercel auto-deploys a preview URL
git push -u origin feature/wave2-promo-codes

# 4. Create PR → merge into staging for final QA
# 5. When confident → merge staging into main (triggers prod deploy)
```

### Setting up the staging branch in Vercel

1. Vercel Dashboard → Settings → Git
2. Under **Preview Branches**, you can assign a custom domain to the `staging` branch
3. Set `preview.codemage.dev` as the domain for the `staging` branch

---

## Part 4: Tool Setup — Cursor + Claude Code

### Cursor (your day-to-day IDE)

Cursor is where you'll spend most of your time. Think of it as VS Code with AI built in.

**Setup:**
1. Download from [cursor.com](https://cursor.com)
2. Open your project: `File → Open Folder → /Users/stellabella/desktop/CodeMage/platform`
3. Sign in and select a model — use **Claude Sonnet 4.5** for most tasks

**Key shortcuts:**
- `Cmd+K` — inline edit (great for quick fixes: "make this responsive", "add error handling")
- `Cmd+L` — open chat sidebar (for larger context questions)
- `Cmd+Shift+P` → "Cursor: Apply to file" — paste a Cowork prompt result

**Recommended Cursor settings (`.cursorrules` file at project root):**
```
You are working on CodeMage, a Next.js 14 App Router project.
Stack: Next.js 14, Supabase, Vercel, Stripe, Resend, Framer Motion 12, Zustand 5.
No src/ directory. App Router only. TypeScript strict mode.
Supabase promo_codes table: primary key is `code` (string), not `id`. 
  Has columns: code, reminder_sent (boolean), expires_at, user_id.
NEXT_PUBLIC_APP_URL must always use www.codemage.dev in production.
All emails use contact@codemage.dev via Resend.
```

### Claude Code (for complex agentic tasks)

Claude Code is your terminal-based agent for larger tasks — refactoring, building full features, running commands. You already use it via Cowork prompts.

**Install/verify:**
```bash
npm install -g @anthropic-ai/claude-code
claude --version
```

**GStack** is a community-built toolkit for Claude Code workflows. It's useful but optional — start without it and add it if you feel like you need better prompt management.

**When to use Cursor vs Claude Code:**

| Task | Use |
|---|---|
| Fix a specific bug | Cursor `Cmd+K` |
| Add a UI component | Cursor chat (`Cmd+L`) |
| Build a full feature (multi-file) | Claude Code / Cowork prompt |
| Run migrations or scripts | Claude Code in terminal |
| Review/understand code | Cursor chat |

---

## Part 5: Testing Suite

You need two layers: **unit/integration tests** (fast, runs on every save) and **end-to-end tests** (slower, runs before merging).

### Layer 1 — Vitest (unit + integration tests)

Vitest is fast, works natively with Vite/Next.js, and has a great DX.

**Install:**
```bash
cd /Users/stellabella/desktop/CodeMage/platform
npm install -D vitest @vitejs/plugin-react jsdom @testing-library/react @testing-library/jest-dom
```

**Add to `package.json`:**
```json
{
  "scripts": {
    "test": "vitest",
    "test:ui": "vitest --ui",
    "test:coverage": "vitest --coverage"
  }
}
```

**Create `vitest.config.ts` at project root:**
```typescript
import { defineConfig } from 'vitest/config'
import react from '@vitejs/plugin-react'

export default defineConfig({
  plugins: [react()],
  test: {
    environment: 'jsdom',
    setupFiles: ['./tests/setup.ts'],
    globals: true,
  },
})
```

**Create `tests/setup.ts`:**
```typescript
import '@testing-library/jest-dom'
```

**Create your first test — `tests/promo-codes.test.ts`:**
```typescript
import { describe, it, expect } from 'vitest'

// Test the promo code validation logic
describe('promo code validation', () => {
  it('accepts valid LAUNCH-XXXX format', () => {
    const isValid = (code: string) => /^(LAUNCH|WAVE2)-[A-Z0-9]{4}$/.test(code)
    expect(isValid('LAUNCH-AB12')).toBe(true)
    expect(isValid('WAVE2-XY99')).toBe(true)
  })

  it('rejects invalid formats', () => {
    const isValid = (code: string) => /^(LAUNCH|WAVE2)-[A-Z0-9]{4}$/.test(code)
    expect(isValid('launch-ab12')).toBe(false)  // lowercase
    expect(isValid('LAUNCH-AB123')).toBe(false) // too long
    expect(isValid('')).toBe(false)             // empty
  })
})
```

**Run tests:**
```bash
npm run test          # watch mode
npm run test:ui       # browser UI (great for visual feedback)
```

### What to write Vitest tests for

Prioritize testing logic that's caused bugs before:

```
tests/
├── promo-codes.test.ts     ← code format validation, expiry logic
├── email-templates.test.ts ← Resend payload structure
├── cron-reminders.test.ts  ← null email filtering, date math
├── stripe-webhook.test.ts  ← signature verification, event parsing
└── auth-flow.test.ts       ← OTP callback redirect logic
```

### Layer 2 — Playwright (end-to-end tests)

Playwright opens a real browser and clicks through your app like a user would.

**Install:**
```bash
npm install -D @playwright/test
npx playwright install chromium  # just Chromium is fine to start
```

**Create `playwright.config.ts`:**
```typescript
import { defineConfig } from '@playwright/test'

export default defineConfig({
  testDir: './tests/e2e',
  fullyParallel: true,
  retries: process.env.CI ? 2 : 0,
  use: {
    baseURL: process.env.PLAYWRIGHT_BASE_URL || 'http://localhost:3000',
    trace: 'on-first-retry',
  },
  webServer: {
    command: 'npm run dev',
    url: 'http://localhost:3000',
    reuseExistingServer: !process.env.CI,
  },
})
```

**Add to `package.json`:**
```json
{
  "scripts": {
    "test:e2e": "playwright test",
    "test:e2e:ui": "playwright test --ui"
  }
}
```

**Create your first E2E test — `tests/e2e/landing.spec.ts`:**
```typescript
import { test, expect } from '@playwright/test'

test('landing page loads', async ({ page }) => {
  await page.goto('/')
  await expect(page).toHaveTitle(/CodeMage/)
  await expect(page.getByText('Start for free')).toBeVisible()
})

test('pricing section visible', async ({ page }) => {
  await page.goto('/')
  await expect(page.getByText('$12')).toBeVisible()
  await expect(page.getByText('$99')).toBeVisible()
})
```

**Create `tests/e2e/auth.spec.ts`:**
```typescript
import { test, expect } from '@playwright/test'

test('login page renders OTP form', async ({ page }) => {
  await page.goto('/login')
  await expect(page.getByPlaceholder(/email/i)).toBeVisible()
})

test('invalid promo code shows error', async ({ page }) => {
  await page.goto('/signup')
  await page.getByPlaceholder(/promo code/i).fill('FAKE-CODE')
  await page.getByRole('button', { name: /continue/i }).click()
  await expect(page.getByText(/invalid/i)).toBeVisible()
})
```

### Layer 3 — Running tests in CI (Vercel + GitHub Actions)

Create `.github/workflows/test.yml`:

```yaml
name: Tests

on:
  pull_request:
    branches: [main, staging]

jobs:
  unit:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v4
      - uses: actions/setup-node@v4
        with:
          node-version: 20
          cache: 'npm'
      - run: npm ci
      - run: npm run test -- --run  # run once, no watch

  e2e:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v4
      - uses: actions/setup-node@v4
        with:
          node-version: 20
          cache: 'npm'
      - run: npm ci
      - run: npx playwright install --with-deps chromium
      - run: npm run test:e2e
        env:
          PLAYWRIGHT_BASE_URL: http://localhost:3000
          NEXT_PUBLIC_SUPABASE_URL: ${{ secrets.TEST_SUPABASE_URL }}
          NEXT_PUBLIC_SUPABASE_ANON_KEY: ${{ secrets.TEST_SUPABASE_ANON_KEY }}
          ANTHROPIC_API_KEY: ${{ secrets.ANTHROPIC_API_KEY }}
```

Add the secrets in **GitHub → Settings → Secrets and variables → Actions**.

---

## Part 6: Stripe Local Testing

Stripe webhooks need a running server to hit. In local dev:

```bash
# Terminal 1: run the app
npm run dev

# Terminal 2: forward Stripe events to localhost
stripe listen --forward-to localhost:3000/api/webhooks/stripe

# Terminal 3: trigger a test event
stripe trigger checkout.session.completed
```

The `stripe listen` command prints a webhook signing secret (`whsec_...`). Put that in `.env.local` as `STRIPE_WEBHOOK_SECRET`.

---

## Recommended File Structure for Tests

```
platform/
├── tests/
│   ├── setup.ts              ← Vitest setup (import jest-dom)
│   ├── promo-codes.test.ts
│   ├── email-templates.test.ts
│   ├── stripe-webhook.test.ts
│   └── e2e/
│       ├── landing.spec.ts
│       ├── auth.spec.ts
│       └── checkout.spec.ts
├── vitest.config.ts
├── playwright.config.ts
└── .cursorrules
```

---

## Quick Reference — Daily Workflow

```bash
# Start work
git checkout main && git pull
git checkout -b feature/my-feature

# Develop (Cursor + Claude Code)
npm run dev
npm run test        # watch mode in another terminal

# Before pushing
npm run test -- --run          # all unit tests pass
npm run build                  # no TypeScript errors

# Push → staging → main
git push -u origin feature/my-feature
# Open PR → merge to staging → QA on preview URL → merge to main
```

---

## Gotchas Specific to CodeMage

- **Supabase `promo_codes`**: PK is `code` (string), no `id` column, no `name` column. Every test that touches this table must reflect that.
- **Stripe webhook URL**: Must be `https://www.codemage.dev/api/webhooks/stripe` (with www) — non-www redirects kill the signature.
- **Resend sender**: Always `contact@codemage.dev` — the shared `onboarding@resend.dev` is blocked once your custom domain is verified.
- **Cron job**: Lives at `app/api/cron/promo-reminders/route.ts` — test by hitting the endpoint directly in dev, or with `stripe trigger` pattern equivalent.
