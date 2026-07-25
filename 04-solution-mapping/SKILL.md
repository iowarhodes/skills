---
name: solution-mapping
description: Take a prioritized opportunity all the way through generating candidate solutions, mapping the assumptions behind the strongest ones, and designing a small test for the riskiest assumption — following Teresa Torres' Continuous Discovery Habits. This is STEP 5 of a new discovery project, the final leg of the first full pass through the cycle — use it once one opportunity has been selected (see opportunity-mapping skill). Trigger whenever the user is brainstorming solutions for a specific customer need and wants to avoid jumping to their first idea, wants to figure out what has to be true for an idea to work, is about to build something and wants a gut-check first, needs to design a test/prototype/experiment for a specific assumption, or says things like "what could we build for this," "help me brainstorm solutions," "what has to be true for this to work," or "how do I test this without building it."
---

# Solution Mapping

Solo-driver mode: this skill covers three phases, and going it alone changes the risk in each one differently.
- **Diverging on solutions** — without a trio to argue for a wider range of ideas, deliberately push past the first 2-3 obvious solutions — those are usually the ones anyone would think of. The extra value of this phase is generating options a single mindset (yours) is prone to skip.
- **Mapping assumptions** — without an engineer in the room to flag feasibility risk, or a PM to flag viability risk, be extra rigorous surfacing assumptions in those two categories rather than defaulting to desirability ("will customers like it"), which is the category a designer's instincts cover best already.
- **Testing the assumption** — the designer is likely both designing AND running the test without a PM to help interpret results objectively or an engineer to build a real prototype. Lean on lightweight, fully designer-buildable test formats, and be explicit that results still deserve a second set of eyes before being treated as validated.

## Core principles

- Torres' guidance: generate at least 5-10 solution ideas for one opportunity before converging on which to test. Jumping straight to the first idea (usually "add a feature") skips the divergent thinking that surfaces better, cheaper, or more elegant options.
- Every solution rests on assumptions across four categories: will the customer choose to use it (**desirability**), can the business afford to offer it (**viability**), can it actually be built (**feasibility**), and can people actually use it (**usability**). Testing the solution as a whole is slow and expensive; testing the riskiest individual assumption first is fast and cheap.
- The goal of a test is the smallest, fastest, cheapest experiment that could plausibly prove the risky assumption wrong. Match the test's fidelity to the assumption being tested — don't build a full feature to test a desirability question a simple mockup could answer.

## Process

### Part A — Diverge on solutions

**1. Restate the opportunity.**
Pull the selected opportunity statement from the opportunity-mapping skill's (03) prioritization pick. Keep it visible throughout — every idea should trace back to this specific need.

**2. Diverge before converging.**
Generate a wide range of solution ideas, deliberately varying the *type* of solution, not just surface variations on one idea:
- A UI/interaction change
- A content/copy change
- A process or workflow change (doesn't require new UI)
- A "remove something" solution (sometimes the fix is deleting a step, not adding one)
- A "make it visible" solution (surfacing existing functionality customers don't know about)
- An ambitious/bigger-bet version, even if it seems out of scope for now

Aim for at least 5-8 distinct ideas before evaluating any of them.

**3. Do a light first-pass filter.**
Don't fully evaluate yet, but flag any idea that's obviously a non-starter (e.g., clearly infeasible, clearly against a known constraint) so it doesn't waste Part B's assumption-mapping effort later.

**4. Pick the top 1-2 candidates.**
From the ideas that survive the filter, select the 1-2 most promising to carry into assumption mapping. These become the "top solutions" layer of the tree.

### Part B — Map the assumptions behind the top solutions

**1. Brainstorm assumptions across all four categories.**
For each top solution, list out what has to be true, sorted into:
- **Desirability** — customers actually want this, will notice it, will choose it over their current workaround
- **Viability** — it fits the business model, doesn't create unacceptable cost/risk/support burden
- **Feasibility** — it's technically buildable with reasonable effort/timeline/existing systems
- **Usability** — once built, people can actually figure out how to use it without confusion

Push to fill in all four categories — solo designers tend to over-generate desirability assumptions and under-generate viability/feasibility ones, since those aren't the home turf.

**2. Plot on an assumption map.**
For each assumption, rate two things:
- **Importance**: if this assumption is wrong, does the whole solution fall apart, or is it a minor detail?
- **Evidence**: how much do we already know vs. how much is a total guess?

The assumptions that are both high-importance and low-evidence are the ones to test next — that's the point of the exercise, not to test everything.

**3. Name the riskiest assumption.**
Call out the single assumption (or top 2-3 across both top solutions) that most threatens its solution if wrong. This becomes the target for the test in Part C.

### Part C — Test the riskiest assumption

**1. Restate the assumption as a falsifiable claim.**
"We're assuming that [customers/the business/engineering/users] will ___."

**2. Pick a test format that matches the assumption type.**
- **Desirability** assumptions: fake door tests, concierge tests, painted-door prototypes, five-second tests, preference tests between mockups
- **Viability** assumptions: rough cost/effort estimate conversations, a lightweight business-case sketch, checking against known constraints or policies
- **Feasibility** assumptions: a technical spike conversation, a quick proof-of-concept, checking existing system documentation
- **Usability** assumptions: a clickable prototype walked through with 3-5 people, a first-click test, a think-aloud session

Favor formats the designer can build and run solo (mockups, clickable prototypes, first-click tests) over ones needing an engineer's help, unless the assumption specifically requires that.

**3. Define what "assumption confirmed" vs. "assumption busted" looks like.**
Before running the test, write down the specific signal that would count as evidence either way. This prevents motivated reasoning after the fact ("well it sort of worked...").

**4. Run it small.**
Suggest the smallest viable version: a handful of participants (5 is often plenty for usability-style tests), a short time window, low build cost.

**5. Decide the next move based on the result.**
- **Assumption holds** → move forward with building/refining this solution; consider whether a second risky assumption from Part B needs testing too before full build
- **Assumption busted** → go back to Part A's solution list for the next candidate, or back to Part B if a different assumption is now the bigger risk
- **Inconclusive** → note what would need to change to get a clean signal, and consider a second small test rather than escalating straight to a full build

## Output format

Always save the output as a single self-contained HTML file (via create_file into the outputs directory, then present_files) — don't just print it inline in chat. Name the file `[project-name]-solution-map.html`. Inline all CSS and any diagram markup (SVG) directly in the file — no external stylesheets, fonts, or CDN scripts — and make sure it's readable in both light and dark viewing. Render it as a single tree diagram, narrowing left-to-right or top-to-bottom through five layers:

1. **Opportunity** (root) — the opportunity statement this whole tree traces back to
2. **Solution ideas** — all 5-8+ diverged candidates as sibling branches, each labeled by type (UI change / content / process / removal / visibility / big bet), with non-starter flags visually marked (e.g., greyed/struck through)
3. **Top solutions** — the 1-2 selected candidates visually called out as the branches that continue deeper (e.g., highlighted border/color), with the rest of layer 2 terminating there
4. **Assumptions** — under each top solution, grouped by the four categories (Desirability / Viability / Feasibility / Usability), each assumption tagged with its importance and evidence rating
5. **Riskiest assumption + test** — the leaf nodes: the flagged high-importance/low-evidence assumption(s), each paired with its falsifiable claim, chosen test format, and success/failure criteria

Below the tree, include a compact summary block:
- **Recommended next step** once the test result comes in
- **Guesses to validate** — which feasibility/viability calls in the assumption map are best guesses needing a second opinion

## Loop back

This is the end of the first full pass through the discovery cycle for one opportunity. Continuous interviewing (skill 02) keeps running in parallel the whole time — use fresh interview signal to sanity-check whether the opportunity tree needs updating, then cycle back through opportunity-mapping's prioritization step (skill 03) for the next opportunity.
