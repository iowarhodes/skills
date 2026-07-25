---
name: discovery-brief
description: Build a deep problem-framing brief (RACI + Discover phase + Define phase, including a pressure-tested product outcome + hypotheses) to kick off a new discovery project, following Teresa Torres' Continuous Discovery Habits. This is STEP 1 of a new discovery project — use it before any interviewing, opportunity mapping, or solution work begins. Trigger whenever the user is starting a brand new discovery initiative or kicking off a new project and needs to nail down the problem and north-star outcome before jumping to solutions — phrases like "kicking off discovery," "write a discovery brief," "let's frame this problem," "what should our outcome be," "who owns what on this project," "new project kickoff," or when the user has a fuzzy idea and needs to pressure-test whether it's a real, worth-solving problem, or is confusing a business outcome (revenue, adoption) with a product outcome (a customer behavior change your product can influence). Also trigger when the user asks for a RACI chart for a discovery/design/development effort.
---

# Discovery Brief

A structured brief that forces problem-first thinking before anyone touches a solution. Three parts — **RACI** (who owns what), **Discover** (is this real, and for whom?), and **Define** (what does winning look like, and what are we betting on?) — that together anchor a new discovery project.

This is a companion to the rest of the Torres-flow skills (`continuous-interviewing`, `opportunity-mapping`, etc.), not a replacement. Use it when the user wants a durable, shareable problem-framing doc — the kind of thing that goes in front of a director or gets pasted into a project kickoff doc — with a rigorously pressure-tested outcome statement at its core.

Solo-driver mode: often the person running this is doing it themselves, without a PM or eng partner in the room yet. Push them to pressure-test their own thinking rather than assuming a trio will catch gaps later — that pushback IS the value of this skill.

## Scoping the conversation

Not every trigger wants the full document. Before running the whole process, gauge what the user actually needs:

- **Just the outcome** ("what should our north-star be," "help me define an outcome" with no mention of a broader brief) → jump straight to the outcome-setting part of Define (below), but still ask the business-context question first — an outcome disconnected from a business goal won't get organizational buy-in.
- **The full brief** ("kick off discovery," "frame this problem," "new project kickoff") → run RACI → Discover → Define in order, all the way through.

Either way, run this as an interview. Don't ask everything at once — work through it in the order below, and write up each section as you go so the user can course-correct early rather than at the end. Push back where an answer is vague, secretly a solution in disguise, or unsupported by evidence.

## 0. RACI Chart

*(Skip if the user only wants the outcome.)*

Ask who's involved and in what capacity across the three stages (Discovery, Design, Development). For each stage, identify:
- **Responsible** — who does the work
- **Accountable** — who owns the outcome / signs off (usually one person per stage)
- **Consulted** — who gives input before decisions are made
- **Informed** — who's kept in the loop after decisions are made

A person can hold different roles at different stages (e.g., Accountable in Discovery, Consulted in Development) — don't assume static roles. Build this as a table: rows = roles (R/A/C/I), columns = Discovery / Design / Development.

## 1. Discover

*(Skip if the user only wants the outcome.)*

Work through these in order. Each answer should sharpen the next — don't let the user skip the problem statement and jump to "what we should build."

**What is the problem we're trying to solve?**
Push for the user's-eye view, not the company's. If the user gives you a solution ("we need a better search bar"), reflect back what problem that solution implies and ask them to state it as a problem instead. Usable shapes:
- [User type] struggles with [obstacle], which causes [negative outcome].
- [User type] can't [achieve goal] because [problem or blocker].
- [User type] experiences [frustration/inefficiency], which leads to [undesired result].

**Who has this problem?**
Get specific — role, job-to-be-done, context, constraints. If the user says "all users," push: who feels this most acutely, and why?

**How do we know it's a real problem?**
Ask for both qualitative signal (interviews, support tickets, usability findings — what are people actually saying) and quantitative scale (analytics, survey data, ticket volume — how many people, how often). If the user doesn't have evidence yet, say so plainly and flag it as a gap to close before investing further — don't let a hunch get dressed up as validated.

**What assumptions do we have about why this problem occurs?**
Capture root-cause guesses per problem. Flag these explicitly as unproven — they feed the Hypotheses section later.

**What has been tried already?**
Prior internal attempts or workarounds. What worked, what didn't, and why. If the user says "nothing," ask about workarounds users have invented themselves — that's often a signal in disguise.

**How do competitors/others solve this?**
Adjacent tools, competitor products, or how users solve it manually today. Look for differentiation opportunities, not just parity checklists.

**What's the business opportunity/risk?**
Connect the user problem to a business outcome. Frame both directions: what's unlocked if solved, what continues/worsens if ignored (churn, missed revenue, brand damage, competitive gap).

## 2. Define

### 2a. The outcome

This is the heart of Define — a compelling, measurable product outcome to anchor the project. Don't let this collapse into a vague "success looks like..." line; give it the full pressure-test.

A product outcome is a measurable change in customer behavior that drives a business result — NOT the business result itself, and NOT an output (a feature, a launch, a deliverable).

- Business outcome (too broad for a team to own directly): "Increase revenue 20%"
- Product outcome (right altitude): "Increase the percentage of dealers who complete self-service quoting"
- Output (not an outcome at all): "Ship the new quoting flow"

A usable outcome is:
1. **A behavior**, not a business metric — something a customer does, not something the company earns
2. **Measurable** — you can point to a number that moves
3. **Owned by the team** — the team's decisions can plausibly move this number
4. **Not a proxy for a feature** — if the outcome describes a solution ("adopt the new dashboard"), it's actually an output in disguise

Work through it in this order:
1. **Start from the business context** captured in "What's the business opportunity/risk?" above (or ask for it directly, if you jumped straight here). An outcome disconnected from a business goal won't get organizational buy-in.
2. **Draft 2-3 candidate outcomes.** For each, write it as "[Increase/decrease] the [percentage/number] of [customers] who [behavior]." Push for behaviors, not features.
3. **Pressure-test each candidate** against the four criteria above. Explicitly call out if a candidate is secretly an output or a business metric.
4. **Check "sphere of influence."** Ask: if this number doesn't move in 90 days, would it be because of something this team controls, or because of forces way outside their control (macroeconomics, sales team behavior, etc.)? If the latter, it's too broad.
5. **Recommend one outcome**, state your reasoning, and flag any assumptions baked into it (e.g., "this assumes dealers who self-serve quotes are more likely to convert — worth validating that link exists before treating it as ground truth"). This becomes the brief's success criteria — the measurable signal everything else in Define ties back to.

### 2b. Candidate solutions

*(Skip if the user only wants the outcome.)*

Ideas only, explicitly tied back to the specific problem they address. Frame these as hypothesis-generating options to explore, not commitments — if the user starts spec'ing a feature in detail here, gently redirect to solution-mapping/design-brief territory instead.

### 2c. Hypotheses

*(Skip if the user only wants the outcome.)*

Write both types, and be clear about which one applies given where the project actually is:

- **Discovery hypothesis** (use when there's a risky assumption to de-risk before building): "We believe [assumption is true]. We can validate this by [experiment/test]. We'll gain confidence if [signal/insight]."
- **Delivery hypothesis** (use when the direction is validated and you're testing impact): "We believe [solution] will lead to [user behavior], which will drive [product/business outcome]. We'll know we're right when [measurable signal]."

Most kickoffs need at least one Discovery hypothesis per risky assumption surfaced in Discover (including the outcome assumption flagged in 2a). Only write Delivery hypotheses if the user already has validation in hand — don't let a team write delivery-style confidence into a brief that hasn't earned it yet.

## 3. Handoff

Once the outcome is set, this shouldn't dead-end:

- **If this was the full brief:** tell the user the natural next step is the `continuous-interviewing` skill (step 2), which builds a weekly interview habit to start generating opportunities against this outcome. Offer to kick that off directly — don't just mention it in passing.
- **If the brief has candidate solutions already sketched:** also mention `design-brief`, which takes the problem/success criteria/candidate solutions from this doc and turns them into a UI direction and experience decisions.
- **If there's an unvalidated risky assumption** sitting in the Discovery hypotheses (including the outcome's own baked-in assumption): flag that too — it's worth testing via `solution-mapping`'s assumption-testing phase before design work locks in a direction.

## Output format

If the user only wanted the outcome, a short outcome brief is enough — present it inline in chat:
- **Business context** (1-2 sentences)
- **Recommended outcome statement**
- **Why this altitude is right** (ties to the 4 criteria)
- **Open assumption(s)** to keep an eye on as discovery proceeds
- **Next step pointer** (continuous-interviewing)

If the user wanted the full brief, always save it as an actual markdown file (via create_file into the outputs directory, then present_files) — don't just print it inline in chat. Name the file `[project-name]-discovery-brief.md`. Produce a single markdown brief with this structure:

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
[Pointer to continuous-interviewing to start building an opportunity space against this outcome, design-brief if candidate solutions are ready to take shape, and/or solution-mapping's assumption-testing phase if unvalidated Discovery hypotheses remain]
```

## Common failure modes to flag for the user

- Problem statement is actually a feature request in disguise ("users need a dashboard")
- "Evidence" is really just an internal opinion or a single anecdote
- Assumptions get written as if they're already validated facts
- Outcome is really a project name or feature ("Launch PellaPro 2.0")
- Outcome is a vanity metric (page views, logins) with no clear tie to value
- Outcome is stated as a solution ("get dealers using the new IA")
- Outcome is too big for one team to influence (company-wide NPS)
- Delivery hypotheses show up before any discovery validation has happened
- RACI has more than one Accountable per stage, or nobody Accountable at all
