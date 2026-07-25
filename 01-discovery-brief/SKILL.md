---
name: discovery-brief
description: Build a deep problem-framing brief (RACI + Discover phase + Define phase + hypotheses) to kick off a new discovery project. Use this whenever the user is starting a new initiative and needs to nail down the problem before jumping to solutions — triggers on phrases like "kick off discovery," "write a discovery brief," "let's frame this problem," "who owns what on this project," "new project kickoff," or when the user has a fuzzy idea and needs to pressure-test whether it's a real, worth-solving problem. This runs alongside (not instead of) outcome-setting and opportunity-mapping work — use it when the user wants the full problem case documented, not just a north-star metric. Also trigger when the user asks for a RACI chart for a discovery/design/development effort.
---

# Discovery Brief

A structured brief that forces problem-first thinking before anyone touches a solution. Two phases — **Discover** (is this real, and for whom?) and **Define** (what does winning look like, and what are we betting on?) — plus a RACI chart matrixed across Discovery, Design, and Development stages.

This is a companion to the Torres-flow skills (`define-outcome`, `opportunity-mapping`, etc.), not a replacement. Use it when the user wants a durable, shareable problem-framing doc — the kind of thing that goes in front of a director or gets pasted into a project kickoff doc.

## Process

Run this as an interview. Don't ask everything at once — work through it in the order below, and write up each section as you go so the user can course-correct early rather than at the end. Push back where an answer is vague, secretly a solution in disguise, or unsupported by evidence — that pushback IS the value of this skill.

### 0. RACI Chart

Ask who's involved and in what capacity across the three stages (Discovery, Design, Development). For each stage, identify:
- **Responsible** — who does the work
- **Accountable** — who owns the outcome / signs off (usually one person per stage)
- **Consulted** — who gives input before decisions are made
- **Informed** — who's kept in the loop after decisions are made

A person can hold different roles at different stages (e.g., Accountable in Discovery, Consulted in Development) — don't assume static roles. Build this as a table: rows = roles (R/A/C/I), columns = Discovery / Design / Development.

### 1. Discover

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

### 2. Define

**What does success look like?**
Get a behavior tied to a metric: "If we solve [problem], users will [behavior], resulting in [product metric]." Reject vague success criteria ("users will be happier") — push for something observable and measurable.

**How might we solve the problem?**
Ideas only, explicitly tied back to the specific problem they address. Frame these as hypothesis-generating options to explore, not commitments — if the user starts spec'ing a feature in detail here, gently redirect to solution-mapping/design-brief territory instead.

**Hypotheses**
Write both types, and be clear about which one applies given where the project actually is:

- **Discovery hypothesis** (use when there's a risky assumption to de-risk before building): "We believe [assumption is true]. We can validate this by [experiment/test]. We'll gain confidence if [signal/insight]."
- **Delivery hypothesis** (use when the direction is validated and you're testing impact): "We believe [solution] will lead to [user behavior], which will drive [product/business outcome]. We'll know we're right when [measurable signal]."

Most kickoffs need at least one Discovery hypothesis per risky assumption surfaced in Discover. Only write Delivery hypotheses if the user already has validation in hand — don't let a team write delivery-style confidence into a brief that hasn't earned it yet.

### 3. Handoff

Once Define is filled in, this brief shouldn't dead-end. Tell the user the natural next step is the `design-brief` skill, which takes the problem/success criteria/candidate solutions from this doc and turns them into a UI direction and experience decisions. Offer to kick that off directly — don't just mention it in passing. If the user has an unvalidated risky assumption sitting in Discovery hypotheses, flag that too: it's worth testing (via `assumption-testing`) before design work locks in a direction.

## Output format

Always save the brief as an actual markdown file (via create_file into the outputs directory, then present_files) — don't just print it inline in chat. Name the file `[project-name]-discovery-brief.md`. Produce a single markdown brief with this structure:

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
### Success criteria
### Candidate solutions (directional, not commitments)
### Hypotheses
#### Discovery hypotheses
#### Delivery hypotheses (only if applicable)

## Next step
[Pointer to design-brief skill to turn this into a UI direction, plus assumption-testing if unvalidated Discovery hypotheses remain]
```

## Common failure modes to flag for the user

- Problem statement is actually a feature request in disguise ("users need a dashboard")
- "Evidence" is really just an internal opinion or a single anecdote
- Assumptions get written as if they're already validated facts
- Success criteria are vague/unmeasurable ("better experience," "more engagement")
- Delivery hypotheses show up before any discovery validation has happened
- RACI has more than one Accountable per stage, or nobody Accountable at all
