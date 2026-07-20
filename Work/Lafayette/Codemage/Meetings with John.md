## Meeting with John (2.4.26)
**Game that teaches clients how to use Claude Code**
- Designed for students new to coding/AI
- Child safety limits marketed to parents
	- Education safety and responsibility for young devs
- Similar to DragonBox leading kids through challenges
	- Fantasy environment?
- Grants as revenue source?

-------------------------------------------------------------------
## Proof of concept 
- **Idea:** AI-powered web game that would teach students how to use Claude Code
- **Inspiration:** Brilliant, Codewars, Duolingo 
- **Format:** series of computing/vibe-coding challenges that students would complete while working through a fantasy environment
	- Installing Claude Code on device
	- Collaborating with Claude Code in real time
- **Creation**
	- **Frontend:** JS-based (React, Next.js)
	- **Backend:** Python-based (Node/Express, Python/FastAPI)
- **Pricing?**
	- Start with free tier of Claude, then move to Pro tier with Claude Code
- **Possible challenge progression**
	- **Act 1 — The Apprentice:** Simple, constrained tasks. "Tell your familiar to build a shelter." Students learn basic prompting, how to read output, how to accept/reject/refine. The familiar is low-powered and forgiving
	- **Act 2 — The Journeyman:** Multi-step projects with real complexity. "The village needs a water system." Students chain commands, manage context, debug when the familiar misunderstands. Introduces concepts like breaking problems down and checking work
	- **Act 3 — The Steward:** Ethical and safety challenges enter. "The king wants you to build a surveillance system for the city." Students learn about when _not_ to build something, or how to push back on a request, or how to build something responsibly. This is where the AI safety curriculum lives organically inside the narrative rather than feeling like a lecture
- **Marketing**
	- **Kid-facing:** "You're a coder-mage in a world where AI is your superpower"
	- **Parent-facing:** "Your child will learn the #1 skill of the AI era — how to work with AI tools responsibly and effectively"
	- **School/institutional angle** (don't sleep on this): Districts are desperate for AI literacy curriculum that isn't just "here's ChatGPT." A game with structured learning outcomes and teacher dashboards could be a wedge into the B2B education market, which is where the real revenue stability is

-------------------------------------------------------------------
## Meeting with John (2.18.26)
**Game progress update**
- **Share**
	- PoC document
	- Pricing document
	- codemage-demo folder (+ installation instructions)
- **Potential issues**
	- Pricing of Claude Code
	- Worth it for me to buy Claude Max? (Usage limits)
	- Time to complete designs (I am busy)
- Where is the neighborhood in DC? (For apartment searching)
- Ask about using Junction as a meeting space for Claude Club?

-------------------------------------------------------------------
## Meeting with John (3.3.26)
**Progress update**
- Full website demo
- Canva graphic
- North Carolina marketing plan (docx)

**Action items**
- **Claude requests**
	- **Game reworks**
		- ~~Provide LinkedIn certificate on completion of course~~
		- ~~Remove mid-tier pricing~~ 
		- ~~Market full package as $200 per certificate~~
		- ~~Rework first level to follow original demo~~
	- **Marketing**
		- ~~Align levels with NC curriculum~~
		- **~~Find NC parents to reach out to (Cary-Chapel Hill area)~~**
	- **Other**
		- **Figure out logistics of paying for Claude Code through CodeMage**
			- Reach out to Anthropic
- **~~Set up purchase link with Stripe~~**
- ~~Buy domain (codemage.dev available)~~

-------------------------------------------------------------------
## Meeting with John (3.18.26)
**Progress update**
- [Business review](https://docs.google.com/document/d/1kwmbVyGvWSIjSqh1SlvIH45mQaIvEMdBJDJTAu8NtxI/edit?tab=t.0)
- Website and game redesigned with React.js
- Full stack deployed
- Promos posted on social media and listserv
- 14/25 access codes sent out as of 3/18

**Action items**
- **Logistics**
	- **Figure out logistics of paying for Claude Code through CodeMage**
		- Reach out to Anthropic - Drew Bent?
		- Consider just teaching them to use Claude.ai and Claude Cowork instead?
- **Feedback**
	- **Reach out to beta testers with feedback form**
		- [Form link](https://tally.so/r/RGLrEP)
		- Add testimonials if applicable
- **Marketing**
	- **Find new listservs to post on**
		- [[Old pitches]]
	- Post on Reddit
- **UI updates**
	- Update landing page
	- Update pricing
	- Improve curriculum
	- Add upgrade option on main page

-------------------------------------------------------------------
## Meeting with John (4.1.26)
**Progress update**
- [Business review](https://docs.google.com/document/d/1IiGDpCibXUNuLHLyrejRpCTgWSLt7Gf7GGtSSp0sxHA/edit?usp=sharing)
- Minor UI updates
- Curriculum updates (chatbot embedded, level philosophy changed)
- 6/25 access codes redeemed
- 31 families on waitlist 
- Feedback from 1 tester

**Current action items**
- **Pricing is too low**
	- Find ceiling for pricing
	- Find unit economics 
- **Reach out to families on waitlist and schedule Zoom call to sign up**
	- Give out more free codes
- **Follow up with the six beta testers**
- **Find more Davidson Institute equivalent listservs**
	- Find influencers in communities 
	- PTA leaders
	- School counselors 
- **Creating an adaptive AI curriculum** 
- **Rethink curriculum and goals of curriculum**
- **Create testing suite**
	- Find errors to fix and find potential improvements
	- Build browser automation
	- Use developer environment
		- Development (trying out ideas)
		- Staging (making changes)
		- Production (user-facing)

**Future action items**
- Find other similar listservs to post on
- Post promotions on Reddit
- Run Instagram/Google/FaceBook ads?
	- Start with FaceBook after more testimonials?
- Get CodeMage on Product Hunt?
- Find unit economics & pricing ceiling 

-------------------------------------------------------------------
## All-hands Meeting
**Joe’s advice**
- Have two AI agents poke holes in the plan before sending it to Cursor to ship
- Install Context7 MCP
- Always give Claude docs for whatever you’re working on
- Find web errors via Inspect Element → Console

**Best tools**
- **Claude:** planning, PRDs, writing
- **Cursor:** building and editing code
- **VAPI/ElevenLabs:** voice agents
- **Supabase:** database (for persistent memory)
- **SuperPowers/GStack:** Claude Code setup that scans for bugs
	- Joe sending MD doc for SuperPowers/GStack installation

-------------------------------------------------------------------
## Meeting with John (4.15.26)
**Progress update**
- Rebranded to Mosaic (mosaiclearn.dev)
- UI redesign across all pages (landing, contact, login, error, game, etc)
- **Huge game redesign** 
	- Took inspiration from Gemini to add new features/levels
	- Scrapped old curriculum completely
	- Changed chat philosophy to push deeper conversations instead of copy/pasting
	- Added specific objectives that automatically updates when students complete items
	- Correctly implemented AI mentor to encourage & challenge students
	- **Each level is a personalized challenge that results in a built-out project**
		- **Cool features:**
			- Desktop-style interface with different apps/files
			- Built-in terminal with linux sandbox
			- Scratch-style block prompting exercise
			- “Under the hood” visualization
			- “Time machine” for prompt history
- New codes created

**Work on marketing**