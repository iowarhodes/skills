---
name: assumption-testing
description: Design a small, fast test for a specific risky assumption before building the real thing, following Teresa Torres' Continuous Discovery Habits. This is STEP 7, the final step of a new discovery project's first pass — use it once the riskiest assumption has been named (see assumption-mapping skill). Trigger whenever the user needs to design a test, prototype, or experiment for a specific assumption, wants to validate an idea cheaply before committing engineering time, or says things like "how do I test this without building it" or "what's the fastest way to check if this assumption is true."
---

# Assumption Testing

Solo-driver mode: the designer is likely both designing AND running this test without a PM to help interpret results objectively or an engineer to build a real prototype. Lean on lightweight, fully designer-buildable test formats, and be explicit that results still deserve a second set of eyes before being treated as validated.

## Core principle

The goal is the smallest, fastest, cheapest test that could plausibly prove the risky assumption wrong. Match the test's fidelity to the assumption being tested — don't build a full feature to test a desirability question a simple mockup could answer.

## Process

### 1. Restate the assumption being tested
Pull the top risky assumption from skill 06. State it as a falsifiable claim: "We're assuming that [customers/the business/engineering/users] will ___."

### 2. Pick a test format that matches the assumption type
- **Desirability** assumptions: fake door tests, concierge tests, painted-door prototypes, five-second tests, preference tests between mockups
- **Viability** assumptions: rough cost/effort estimate conversations, a lightweight business-case sketch, checking against known constraints or policies
- **Feasibility** assumptions: a technical spike conversation, a quick proof-of-concept, checking existing system documentation
- **Usability** assumptions: a clickable prototype walked through with 3-5 people, a first-click test, a think-aloud session

Favor formats the designer can build and run solo (mockups, clickable prototypes, first-click tests) over ones needing an engineer's help, unless the assumption specifically requires that.

### 3. Define what "assumption confirmed" vs. "assumption busted" looks like
Before running the test, write down the specific signal that would count as evidence either way. This prevents motivated reasoning after the fact ("well it sort of worked...").

### 4. Run it small
Suggest the smallest viable version: a handful of participants (5 is often plenty for usability-style tests), a short time window, low build cost.

### 5. Decide the next move based on the result
- **Assumption holds** → move forward with building/refining this solution; consider whether a second risky assumption from skill 06 needs testing too before full build
- **Assumption busted** → go back to skill 05's solution list for the next candidate, or back to skill 06 if a different assumption is now the bigger risk
- **Inconclusive** → note what would need to change to get a clean signal, and consider a second small test rather than escalating straight to a full build

## Output format

Always save the test plan as an actual markdown file (via create_file into the outputs directory, then present_files) — don't just print it inline in chat. Name the file `[project-name]-assumption-test.md`. Structure it as:

- **Assumption restated as a falsifiable claim**
- **Test format chosen** and why it matches the assumption type
- **Success/failure criteria**, defined before running it
- **Recommended next step** once the result comes in

## Loop back

This is the end of the first full pass through the discovery cycle for one opportunity. Continuous interviewing (skill 02) keeps running in parallel the whole time — use fresh interview signal to sanity-check whether the opportunity tree needs updating, then cycle back through opportunity-mapping's prioritization step (skill 03) for the next opportunity.
