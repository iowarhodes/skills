---
name: prioritize-opportunities
description: Decide which opportunity on the opportunity tree to pursue first, following Teresa Torres' Continuous Discovery Habits. This is STEP 4 of a new discovery project — use it once an opportunity tree exists (see opportunity-mapping skill) and before generating solutions. Trigger whenever the user has multiple candidate opportunities and needs to pick one, is deciding what to work on next, or says things like "which of these opportunities should I tackle first" or "help me prioritize my opportunity tree."
---

# Prioritize Opportunities

Solo-driver mode: without a PM/eng partner to argue the business-viability or feasibility side, the designer needs to explicitly reason through those angles themselves rather than defaulting to "what feels most interesting to design."

## Core principle

Not every opportunity gets pursued at once. Torres recommends picking ONE opportunity at a time to go deep on, rather than spreading solution effort across the whole tree. The choice should be deliberate, not just "whichever came up most in interviews."

## Process

### 1. Lay out the candidates
Pull the first-level opportunities from the tree (skill 03 output).

### 2. Score each on a few dimensions
For each candidate opportunity, reason through:
- **Evidence strength** — how many interviews support it, and how strong/specific the signal was
- **Size of impact on the outcome** — if solved well, how much would this plausibly move the outcome metric?
- **Feasibility** (your best guess, standing in for the eng voice that isn't in the room) — is this something buildable in a reasonable timeframe, or does it likely require large platform investment? If too large for reasonable timeframe, flag it as an opportunity to split into smaller sub-opportunities that could be solved independently.
- **Business viability** (your best guess, standing in for the PM voice) — does solving this create risk or cost the business would push back on?
- **Market/timing** — is there an external reason this needs to happen now (competitive pressure, a dependency, a compliance deadline)?

### 3. Make the call — and flag it as provisional
Recommend one opportunity to pursue first, with reasoning shown across the dimensions above. Because this is being scored solo, explicitly flag which dimensions (feasibility, viability) are your best guess and should get a real gut-check from an engineer or PM stakeholder before committing significant design time.

### 4. Park the rest, don't discard them
Note the other opportunities as parked, not dead — they stay on the tree for a future pass once the current one is resolved (or de-prioritized after a bad assumption test).

## Output format

- **Ranked list** of opportunities with a one-line reasoning per dimension
- **Recommended pick**, clearly marked
- **Guesses to validate**: which feasibility/viability calls need a second opinion before moving forward
- **Parked opportunities** for later

## When to move on

Once one opportunity is selected, move to generating and mapping candidate solutions against it (skill 05).
