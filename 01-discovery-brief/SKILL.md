---
name: discovery-brief
description: Build a problem-framing brief — RACI, Discover phase, Define phase (pressure-tested product outcome + hypotheses) — to kick off a new discovery project, per Teresa Torres' Continuous Discovery Habits. STEP 1: use before interviewing, opportunity mapping, or solution work begins. Trigger on "kick off discovery," "write a discovery brief," "frame this problem," "what should our outcome be," "who owns what on this project," "new project kickoff," a fuzzy idea that needs a real-problem gut-check, confusing a business outcome with a product outcome, or a request for a RACI chart for a discovery/design/development effort.
---

# Discovery Brief

Forces problem-first thinking before anyone touches a solution. Three parts — **RACI** (who owns what), **Discover** (is this real, and for whom?), **Define** (what does winning look like, what are we betting on?) — that anchor a new discovery project.

Companion to the rest of the Torres-flow skills (`continuous-interviewing`, `opportunity-mapping`, etc.), not a replacement. Use when the user wants a durable, shareable problem-framing doc — the kind that goes in front of a director — with a rigorously pressure-tested outcome at its core.

Solo-driver mode: often the person running this has no PM/eng partner in the room yet. Push them to pressure-test their own thinking rather than assuming a trio will catch gaps later — that pushback IS the value of this skill.

## Scoping the conversation

- **Just the outcome** ("what should our north-star be") → jump straight to 2a below, but still ask the business-context question first — an outcome disconnected from a business goal won't get buy-in.
- **The full brief** ("kick off discovery," "frame this problem," "new project kickoff") → run RACI → Discover → Define in order.

Run this as an interview either way. Don't ask everything at once — write up each section as you go so the user can course-correct early. Push back where an answer is vague, secretly a solution in disguise, or unsupported by evidence.

## 0. RACI Chart

*(Skip if the user only wants the outcome.)*

Ask who's involved and in what capacity across Discovery, Design, Development: **Responsible** (does the work), **Accountable** (owns/signs off — usually one per stage), **Consulted** (input before decisions), **Informed** (told after). A person can hold different roles at different stages — don't assume static roles. Build as a table: rows R/A/C/I, columns Discovery/Design/Development.

## 1. Discover

*(Skip if the user only wants the outcome.)*

Work through in order — each answer should sharpen the next. Don't let the user skip the problem statement and jump to "what we should build."

**What is the problem?** Push for the user's-eye view, not the company's. If the user gives a solution ("we need a better search bar"), reflect back the implied problem. Usable shapes:
- [User type] struggles with [obstacle], which causes [negative outcome].
- [User type] can't [achieve goal] because [problem or blocker].
- [User type] experiences [frustration/inefficiency], leading to [undesired result].

**Who has this problem?** Get specific — role, job-to-be-done, context, constraints. If "all users," push: who feels it most acutely?

**How do we know it's real?** Need both qualitative signal (interviews, tickets, usability findings) and quantitative scale (analytics, survey data, volume). No evidence yet → say so and flag it as a gap, don't let a hunch pass as validated.

**What assumptions explain why it occurs?** Capture root-cause guesses, flagged explicitly as unproven — feeds Hypotheses later.

**What's been tried?** Prior attempts/workarounds, what worked/didn't. "Nothing" → ask about workarounds users invented themselves, often a signal in disguise.

**How do competitors/others solve this?** Adjacent tools or manual workarounds today. Look for differentiation, not just parity.

**What's the business opportunity/risk?** Connect the problem to a business outcome both ways: what's unlocked if solved, what worsens if ignored (churn, revenue, brand, competitive gap).

## 2. Define

### 2a. The outcome

The heart of Define — don't let it collapse into a vague "success looks like..." line; give it the full pressure-test.

A product outcome is a measurable change in customer behavior that drives a business result — NOT the business result itself, NOT an output.
- Business outcome (too broad to own): "Increase revenue 20%"
- Product outcome (right altitude): "Increase the percentage of dealers who complete self-service quoting"
- Output (not an outcome): "Ship the new quoting flow"

A usable outcome is:
1. **A behavior** — something a customer does, not something the company earns
2. **Measurable** — a number that moves
3. **Owned by the team** — their decisions can plausibly move it
4. **Not a proxy for a feature** — if it describes a solution, it's an output in disguise

Process:
1. **Start from business context** (from "business opportunity/risk" above, or ask directly).
2. **Draft 2-3 candidates** as "[Increase/decrease] the [%/#] of [customers] who [behavior]." Push for behaviors, not features.
3. **Pressure-test each** against the 4 criteria — call out if secretly an output or business metric.
4. **Check sphere of influence.** If this doesn't move in 90 days, is that on this team, or on forces outside their control? Latter → too broad.
5. **Recommend one**, with reasoning and any baked-in assumption flagged (e.g., "assumes self-serve quoters convert more — worth validating"). This becomes the brief's success criteria.

### 2b. Candidate solutions

*(Skip if the user only wants the outcome.)*

Ideas only, tied back to the problem they address. Hypothesis-generating options, not commitments — if the user starts spec'ing a feature in detail, redirect to solution-mapping/design-brief territory.

### 2c. Hypotheses

*(Skip if the user only wants the outcome.)*

- **Discovery hypothesis** (risky assumption to de-risk before building): "We believe [assumption is true]. We can validate this by [experiment/test]. We'll gain confidence if [signal/insight]."
- **Delivery hypothesis** (direction validated, testing impact): "We believe [solution] will lead to [user behavior], which will drive [product/business outcome]. We'll know we're right when [measurable signal]."

Most kickoffs need one Discovery hypothesis per risky assumption from Discover (including the outcome's own, from 2a). Only write Delivery hypotheses if validation is already in hand.

## 3. Handoff

- **Full brief:** point to `continuous-interviewing` (step 2) to build a weekly interview habit against this outcome. Offer to kick it off directly.
- **Candidate solutions already sketched:** also mention `design-brief`, which turns the problem/success criteria/candidates into a UI direction.
- **Unvalidated risky assumption** in the Discovery hypotheses (including the outcome's own): flag it — worth testing via `solution-mapping`'s assumption-testing phase before design locks in a direction.

## Output format

Outcome only → present inline in chat: **business context** (1-2 sentences), **recommended outcome statement**, **why this altitude is right** (ties to the 4 criteria), **open assumption(s)**, **next step pointer** (continuous-interviewing).

Full brief → always save as a markdown file (create_file into outputs, then present_files), never just printed in chat. Name it `[project-name]-discovery-brief.md`:

```
# [Project Name] — Discovery Brief

## RACI
[table: R/A/C/I rows × Discovery/Design/Development columns]

## Discover
### The problem
### Who has this problem
### Evidence
### Assumptions about root cause
### What's been tried
### How others solve this
### Business opportunity/risk

## Define
### Outcome
[recommended outcome statement, why this altitude is right, open assumptions]
### Candidate solutions (directional, not commitments)
### Hypotheses
#### Discovery hypotheses
#### Delivery hypotheses (only if applicable)

## Next step
[continuous-interviewing to build an opportunity space against this outcome; design-brief if candidates are ready; solution-mapping's assumption-testing phase if unvalidated Discovery hypotheses remain]
```

## Common failure modes to flag

- Problem statement is a feature request in disguise ("users need a dashboard")
- "Evidence" is really an internal opinion or a single anecdote
- Assumptions written as if already validated facts
- Outcome is really a project/feature name, or a vanity metric with no tie to value
- Outcome is stated as a solution, or too big for one team to influence
- Delivery hypotheses show up before any discovery validation
- RACI has more than one Accountable per stage, or none at all
