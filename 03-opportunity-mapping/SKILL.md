---
name: opportunity-mapping
description: Turn interview snapshots into a mapped, prioritized opportunity space — the top of an Opportunity Solution Tree plus a call on which opportunity to pursue first — following Teresa Torres' Continuous Discovery Habits. This is STEP 3 of a new discovery project — use it once several customer interviews have been run (see continuous-interviewing skill) and before generating candidate solutions. Trigger whenever the user has a batch of interview notes/snapshots to make sense of, wants to build an opportunity tree, needs to organize needs/pains/desires into themes, has multiple candidate opportunities and needs to pick one, is deciding what to work on next, or says things like "I have a bunch of interview notes, now what," "help me build my opportunity space," or "which of these opportunities should I tackle first."
---

# Opportunity Mapping

Solo-driver mode: the designer is doing the tagging, clustering, and prioritization call themselves. Two distinct risks come with that:
- **Synthesis drift** — a single person's clustering can drift toward their own pet theories. Explicitly flag any theme that rests on one or two interviews rather than a pattern, and don't let it get treated as settled just because it made it onto the tree.
- **Missing voices in the prioritization call** — without a PM/eng partner to argue the business-viability or feasibility side, the designer needs to explicitly reason through those angles themselves rather than defaulting to "what feels most interesting to design."

## Core principle

An "opportunity" is a customer need, pain point, or desire — framed from the customer's point of view, not the business's. Opportunities are NOT solutions. "Dealers can't tell if a quote saved" is an opportunity; "add a save confirmation toast" is a solution, and it belongs later in the tree.

Not every opportunity gets pursued at once, either. Torres recommends picking ONE opportunity at a time to go deep on, rather than spreading solution effort across the whole tree. The choice should be deliberate, not just "whichever came up most in interviews."

## Process

### Part A — Map the opportunity space

**1. Pull every tagged moment across snapshots.**
Gather the tagged moments (needs/pains/desires) from all interview snapshots so far into one list.

**2. Cluster into opportunities.**
Group tagged moments that point at the same underlying need. Name each cluster as an opportunity statement, written from the customer's perspective, e.g.:
- "Dealers don't trust that their quote data saved correctly"
- "Contractors want to compare quote versions without losing the original"

Avoid solution-shaped names ("Need an autosave feature") — reframe as the underlying need.

**3. Look for sub-opportunities.**
Some opportunities are actually a parent need with smaller needs nested underneath (e.g., "trust that data saved" might break into "wants visual confirmation" and "wants a way to recover from an accidental navigation-away"). Nest these as child opportunities under the parent — this becomes the tree structure. Each parent should have multiple children, and each child should be unique enough to stand on its own. If multiple children in the same parent are really the same need, merge them. If a child is really a solution in disguise, flag it and move it to the solution layer of the tree instead.

**4. Build the opportunity tree.**
Structure as a tree with the outcome (from skill 01) at the top, then the "when" layer, then the opportunity clusters directly beneath it starting with "I need" or "I want." Pull the "when" layer straight from continuous-interviewing's cross-interview timeline (skill 02) rather than re-deriving it — carry over each moment's evidence count and outlier flag as-is. Attach each opportunity cluster under the specific moment(s) it arises from; an opportunity with no moment to attach to is a signal it may not be well-grounded in the interviews yet. Each opportunity should plausibly, if addressed, move the outcome. If an opportunity doesn't connect to the outcome, flag it — it may belong to a different outcome or project.

**5. Note evidence strength.**
For each opportunity, tag how many separate interviews surfaced it. Distinguish "recurring pattern across N interviews" from "single mention, worth watching."

### Part B — Prioritize the candidates

**1. Lay out the candidates.**
Pull the first-level opportunities from the tree built in Part A.

**2. Score each on a few dimensions.**
For each candidate opportunity, reason through:
- **Evidence strength** — how many interviews support it, and how strong/specific the signal was (carry this forward from Part A, step 5)
- **Size of impact on the outcome** — if solved well, how much would this plausibly move the outcome metric?
- **Feasibility** (your best guess, standing in for the eng voice that isn't in the room) — is this something buildable in a reasonable timeframe, or does it likely require large platform investment? If too large for reasonable timeframe, flag it as an opportunity to split into smaller sub-opportunities that could be solved independently.
- **Business viability** (your best guess, standing in for the PM voice) — does solving this create risk or cost the business would push back on?
- **Market/timing** — is there an external reason this needs to happen now (competitive pressure, a dependency, a compliance deadline)?

**3. Make the call — and flag it as provisional.**
Recommend one opportunity to pursue first, with reasoning shown across the dimensions above. Because this is being scored solo, explicitly flag which dimensions (feasibility, viability) are your best guess and should get a real gut-check from an engineer or PM stakeholder before committing significant design time.

**4. Park the rest, don't discard them.**
Note the other opportunities as parked, not dead — they stay on the tree for a future pass once the current one is resolved (or de-prioritized after a bad assumption test).

## Output format

Always save the output as a single self-contained HTML file (via create_file into the outputs directory, then present_files) — don't just print the tree and scores inline in chat. Name the file `[project-name]-opportunity-map.html`. Inline all CSS and any diagram markup (SVG) directly in the file — no external stylesheets, fonts, or CDN scripts — and make sure it's readable in both light and dark viewing (avoid pure black/white blocks that only work in one mode). The page has two parts:

**1. Opportunity tree (visual map)**
Render the tree as SVG or styled nested HTML boxes: outcome at the top, "when" moments in the middle layer, opportunities and sub-opportunities nested beneath. Carry the solid-vs-outlier marker styling for "when" nodes over from the continuous-interviewing timeline (skill 02), so overlapping and outlier moments stay visually distinct here too. Each opportunity node should show:
- The opportunity statement
- Evidence strength (e.g., a small badge: "5 interviews" vs "1 mention")
- A visual flag on any node noted as a solution-in-disguise or not clearly laddering to the outcome

**2. Prioritization matrix**
Below the tree, render a 2×2 scatter plot (SVG) of the first-level opportunities:
- X-axis: confidence to pursue now (a rough blend of feasibility + viability + timing)
- Y-axis: impact on the outcome
- Bubble size: evidence strength
- The recommended pick visually called out (e.g., highlighted border/color); parked opportunities shown muted/greyed

Underneath the matrix, include a compact scorecard table (one row per opportunity, one column per dimension from Part B step 2) so the reasoning behind each point's placement is legible, not just the plot. Close with:
- **Recommended pick**, clearly marked, with reasoning
- **Guesses to validate**: which feasibility/viability calls need a second opinion before moving forward
- **Parked opportunities** for later

## When to move on

Once the opportunity space feels reasonably stable (new interviews are landing on existing branches more often than creating new ones) and one opportunity has been selected, move to solution-mapping (skill 05) — it takes the opportunity all the way through candidate solutions, assumption mapping, and a first assumption test.
