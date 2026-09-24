# Survey testing training

### **Meeting with Veronica | August 26, 2026**

**Survey creation process**

1. **Programming**
   - Outsourced to Research Results
2. **Thursday testing**
   - Turn tools on before the first click
   - Look for hidden variables, terminations, and tasks (allows you to skip between points/paths)
   - **Change log process**
     - Copy the change log template
     - Save it in the VENDOR folder
     - When annotating, include date, question, and exact changes
     - Always test before sending out
   - **Things to check**
     - Is everything showing as intended?
     - Is the logic working?
     - Have you tested every path?
     - How is the respondent experience?
   - **Test with survey draft and change log**
3. **Client review**
4. **Soft launch (quality check)**
   - Run the survey among a small pool of respondents (n = 50-100)
   - **Reviewing soft launch data**
     - Download the dataset, open it in SPSS/Q, and go through the list
       - Does the file work?
       - Does the data look real?
5. **Full launch**

# Data quality training

### **Meeting with Veronica | August 28, 2026**

**Why do we check data quality while in-field?**

- The analysis is only as good as the participants
  - Participant response quality is measured via a strike system (3 strikes out)
- Checking provides better estimates of participant counts
- Cutting earlier on is cheaper than cutting later

**Terminology**

- **Strikes:** quality checks built into the survey (attention checks, trick questions, etc)
- **Flags:** small errors signalling poorer quality data
- **LOI:** length of interview (how long the participant spent on the survey)
- **QC age:** question that re-checks the participant’s age
- **OE:** open-ended questions where the participants type their answers

**Steps to the data quality process**

1. **Set up the data quality layout (choose key variables)**
   - Record ID, date, age vs. QC age, strikes, flags, OEs, LOI
2. **Pull the Excel file from Decipher/software of choice**
   - Sort the file by strikes and flags, from highest to lowest
   - Then sort by LOI, lowest first
   - Read every OE in that order
     - Look for gibberish, illogical, contradictory, or off-topic answers, copy-pasted content, AI-generated content
3. **Keep an eye on participant quotas**
   - Every removal changes the proportions of the participant pool
   - Removing 10-20% of the sample is typical
4. **Hand off the removal reports**
   - Mark the record/participant IDs
   - Explain the reason for removal
   - Save the file in the project folder
   - Send the ID list to Research Results/equivalent

# Survey writing training

### **New Hire Team | September 17, 2026**

**Survey structure**

1. **Research overview**
   - Objectives
   - Timelines
   - Quota table
   - Methodology
   - Screening criteria
   - Samples and splits
2. **Screener (qualifying participants)**
   - Bringing the right participants in
   - Filtering the wrong participants out
   - Sorting participants into quota categories
3. **Survey body**
   - Research questions
     - Typically filtered by topic sections
4. **Profiling**
   - Additional demographic questions
   - Age confirmation (quality check)

**What makes a good survey question?**

- The question focuses on one idea only
- The question uses neutral framing (without leading participants or absolute language)
- The question has as many positive options as negative options
- The question is mutually exclusive (no overlap between options)
- The question is written in plain language
- The question has exhaustive options
- The question is answerable

**Common types of survey questions**

- Single select
- Open-ended
- Multi select
- Ranking
- Grid/matrix
- Advanced (MaxDiff, DCM, etc)

# Methodology training

### **New Hire Team | September 24, 2026**

**Methodologies**

1. **MaxDiff**
   - **When should I use it?** When you need to cleanly rank a long list of choices
   - **What question does it answer?** Of these 20 features, which 3 do people care about the most?
   - **What can’t it do?** Specify the gap between rankings - how much more do people like the best-ranked choice? 
   - **How does it work?** 
     - Participants are shown a small set of choices and asked to rank them from best to worst
     - This is repeated until every choice from the full list has been ranked
   - **Duo MaxDiff**
     - Asks participants to rank choices from best to worst based on two different aspects (instead of one)
   - **Ways of handling long lists for MaxDiff**
     - **Express**
       - Best for: medium lists
       - Each person only sees a snippet of the full list
     - **Sparse** 
       - Best for: long lists
       - Each person sees every choice, but fewer times (less precise)
     - **Bandit**
       - Best for: huge massive lists
       - Adaptive design: for each participant, repeatedly unselected choices are dropped 
2. **TURF**
   - **When should I use it?** If you’re picking a lineup of choices, but can only choose a few
   - **What question does it answer?** Which 5 of these 20 choices ensure almost everyone is happy?
   - **What can’t it do?** Talk about volume or revenue
   - **How does it work?**
     - Defines what counts as “reached” (first or second choice)
     - Tries every combination of items
     - Keeps the mix that reaches the most unique people