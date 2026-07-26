---
name: jtbd-discovery
description: Turn a fuzzy "customers want X" into a real Jobs-to-be-Done statement before any problem-framing work starts. This is STEP 0 of a new discovery project — use it before discovery-brief, whenever a request arrives as a feature/solution ("they need a dashboard") or a vague want rather than a job the customer is trying to get done. Produces a four-part job statement (when/but/help me/so I), top desired outcomes, today's competing solutions/workarounds (what's being hired and fired), and a job map of stage-by-stage job statements across the eight universal job stages (define, locate, prepare, confirm, execute, monitor, modify, conclude). Trigger whenever the user hands you a feature request that's really a job in disguise, says things like "customers want X," "users are asking for Y," "what job is this really serving," wants to write a job statement, or needs to pressure-test a raw ask before it becomes a discovery brief.
---

# JTBD Discovery

The front door to discovery, one step before `discovery-brief`. Someone brings a fuzzy "customers want X" — this skill turns it into a real job statement before RACI, Discover, or Define even start.

```
jtbd-discovery → discovery-brief → continuous-interviewing → opportunity-mapping → solution-mapping → roadmap
```

Lightweight by design: no full Switch interview protocol, no ODI importance/satisfaction scoring. Just a clean job statement, a short list of outcomes in plain language, and a look at what's filling the job today.

## Core principle

A job is the progress someone is trying to make in a given situation — not a feature, not a persona, not a demographic. If the user hands you a solution ("they need a dashboard"), don't take it at face value: push back and ask what job the dashboard is a hack for. Same pressure-testing instinct as `discovery-brief` — a request stated as a solution is a job in disguise, and the real job is usually one level up.

## JTBD statement template

Use this four-part form — it makes the barrier explicit instead of leaving it implicit, which is what separates a sharp job statement from a mushy one:

> When [situation/context], but [barrier], help me [goal], so I [outcome].

**Good examples:**

- **Discord:** "When I want to jump into my favorite game, but I don't know if there are people around to play, help me safely coordinate with a group of like-minded gamers, so I can easily find a way to enjoy my favorite multiplayer game."
- **Peloton:** "When I need an option to workout, but I can't go to my favorite studio, help me get a convenient and inspiring indoor workout, so I can feel my best for myself and my family."
- **Tuned:** "When I want to feel connected to my partner, but don't have a special way to share my feelings, help me be more emotionally expressive, so we can strengthen our bond."

Each one names a *real* barrier (not "no solution exists") and ties the outcome to an emotional payoff, not just a functional one. Use these as the bar for "done" when you draft the job statement in step 5 below — if the barrier clause could be deleted without losing meaning, push the user for a sharper one.

## Universal Job Map (Eight Stages)

The core job statement captures the job as a whole. The Universal Job Map (see [myles-innovation.com/blog/jtbd-canvas-guide](https://myles-innovation.com/blog/jtbd-canvas-guide/)) breaks that job into the process the customer actually runs to get it done — useful because friction and unmet outcomes usually live inside one specific stage, not the job in the abstract.

1. **Define** — Determine what needs to be done and plan the approach.
2. **Locate** — Find and gather inputs, materials, and information.
3. **Prepare** — Set up the environment and necessary resources.
4. **Confirm** — Verify readiness before starting execution.
5. **Execute** — Perform the core task.
6. **Monitor** — Track ongoing progress and performance.
7. **Modify** — Make adjustments or handle changes as needed.
8. **Conclude** — Finish, clean up, and document the process.

Every job map stage gets written in the same four-part shape as the core statement (when/but/help me/so I) — just scoped tightly to that slice of the process instead of the whole job. A stage statement that reads as a bare task description ("order the coffee") hasn't been done yet; it needs its own situation, barrier, and outcome, even in miniature.

## Process

Run this as a conversation, not a form — ask one thing at a time and write up each piece as you go so the user can correct course early. Four things must get asked no matter what: **who** this is for, **why** they want it (motivations), **what's blocking them** (barriers), and **what they're hiring or firing today**. The steps below fold those into the natural flow rather than treating them as a separate checklist.

**1. Core audience.** Who exactly is this for? Push for defining characteristics — enough to picture a specific person, not a demographic label like "small business owners." A job belongs to a situation, but you still need to know whose situation it is, or you risk designing for "everyone," which is really no one.

**2. Situation/trigger.** What's happening right before this need shows up? This is the "When..." clause. Anchor on context and circumstance, not on the audience again — that was step 1.

**3. Motivations.** What are they actually trying to make progress on, both functionally and emotionally? If the answer is a feature or a tool, reflect back the underlying job and ask again — "what would that let you do that you can't do now?" This becomes the "help me..." clause.

**4. Barriers.** What's stopping them from making that progress today? This is the "but..." clause, and it's the one people skip — don't let it go unasked. A statement without a real barrier reads generic; naming the barrier is what makes it land.

**5. Desired outcomes.** What does "done" look like for them? Pull 2-4, in plain conversational language (e.g., "Feel confident the quote won't need revisions") — not the ODI metric-style "minimize the time it takes to..." phrasing. These aren't measured yet, just named. The strongest one becomes the "so I..." clause.

**6. What they're hiring / firing.** What are they using or doing today instead? Push past "nothing" — jobs are almost always being done by something today, even if it's a workaround, a spreadsheet, a manual process, or a competitor's half-fit tool ("hiring"). Also ask what they've tried and abandoned, and why ("firing") — that's often more diagnostic than what's currently working, since it tells you what not to build.

**7. Pull of the status quo** *(optional — only if it surfaces naturally, don't force it)*. What's dragging them back to what they do today even if the new thing sounds better? A one-liner is enough — you don't need the full push/pull/anxiety/habit Switch model, just whatever surfaces in conversation.

**8. Job map pass.** Once the core statement holds up, draft a job statement for each of the eight Universal Job Map stages yourself, using the audience, situation, barriers, and outcomes already gathered — don't restart the four-question interview eight times, that breaks the "lightweight by design" principle. Present all eight in one batch and let the user correct or fill gaps, the same way you'd sanity-check a first draft. Not every stage will be rich for every job — a quick, honest one-liner beats a padded one; if a stage genuinely doesn't apply (e.g. "Confirm" is trivial for an impulse buy), say so instead of inventing a barrier.

## Output format

Always save as a markdown file (`create_file` into outputs, then `present_files`) — don't just print it in chat. Name it `[job-name]-jtbd.md`:

```markdown
# [Job Name] — Jobs to Be Done

## Core Audience
[who this is for — specific enough to picture, not a demographic label]

## Job Statement
When [situation], but [barrier], help me [motivation], so I [expected outcome].

## Top Desired Outcomes
- ...
- ...

## What They're Hiring / Firing Today
- Hiring: [what they use or hack together today instead]
- Firing: [what they've tried and abandoned, and why]

## What's Pulling Them Back to the Status Quo
[optional — only if it surfaced naturally]

## Job Map
Stage-by-stage job statements, same when/but/help me/so I shape as above, scoped to that slice of the process.

- **Define:** When..., but..., help me..., so I...
- **Locate:** When..., but..., help me..., so I...
- **Prepare:** When..., but..., help me..., so I...
- **Confirm:** When..., but..., help me..., so I...
- **Execute:** When..., but..., help me..., so I...
- **Monitor:** When..., but..., help me..., so I...
- **Modify:** When..., but..., help me..., so I...
- **Conclude:** When..., but..., help me..., so I...

## Next Step
Feeds discovery-brief's problem statement — the job statement above becomes the seed for "what is the problem?"
```

## Common failure modes to flag

- The "job" is actually a feature or solution restated ("they need a dashboard" isn't a job)
- Desired outcomes are written as ODI-style metrics instead of plain language
- "Hiring/firing" gets answered as "nothing" without a second push
- The situation described is really a persona/demographic, not a triggering context
- The audience is left vague ("small business owners") instead of a picturable, specific person
- The barrier clause is missing or generic ("no good solution exists") instead of naming the real thing in their way
- A job map stage is written as a bare task ("execute: order the coffee") instead of a real when/but/help me/so I statement
- Every job map stage gets forced through a full interview round instead of being drafted from what's already known and handed back for a quick correction
- A stage that genuinely doesn't apply gets padded with an invented barrier instead of being flagged as trivial/not applicable

## Handoff

Always end by pointing to `discovery-brief` — offer to kick it off directly, using the job statement above as the seed for its problem statement.
