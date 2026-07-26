---
name: jtbd-discovery
description: Turn a fuzzy "customers want X" into a real Jobs-to-be-Done statement before any problem-framing work starts. This is STEP 0 of a new discovery project — use it before discovery-brief, whenever a request arrives as a feature/solution ("they need a dashboard") or a vague want rather than a job the customer is trying to get done. Produces a Christensen-form job statement, top desired outcomes, and today's competing solutions/workarounds. Trigger whenever the user hands you a feature request that's really a job in disguise, says things like "customers want X," "users are asking for Y," "what job is this really serving," wants to write a job statement, or needs to pressure-test a raw ask before it becomes a discovery brief.
---

# JTBD Discovery

The front door to discovery, one step before `discovery-brief`. Someone brings a fuzzy "customers want X" — this skill turns it into a real job statement before RACI, Discover, or Define even start.

```
jtbd-discovery → discovery-brief → continuous-interviewing → opportunity-mapping → solution-mapping → roadmap
```

Lightweight by design: no full Switch interview protocol, no ODI importance/satisfaction scoring. Just a clean job statement, a short list of outcomes in plain language, and a look at what's filling the job today.

## Core principle

A job is the progress someone is trying to make in a given situation — not a feature, not a persona, not a demographic. If the user hands you a solution ("they need a dashboard"), don't take it at face value: push back and ask what job the dashboard is a hack for. Same pressure-testing instinct as `discovery-brief` — a request stated as a solution is a job in disguise, and the real job is usually one level up.

## Process

Run this as a conversation, not a form — ask one thing at a time and write up each piece as you go so the user can correct course early.

**1. Situation/trigger.** What's happening right before this need shows up? Anchor on context and circumstance, not who the person is. A job belongs to the situation, not the persona.

**2. The job itself.** What are they actually trying to make progress on? If the answer is a feature or a tool, reflect back the underlying job and ask again — "what would that let you do that you can't do now?"

**3. Desired outcomes.** What does "done" look like for them? Pull 2-4, in plain conversational language (e.g., "Feel confident the quote won't need revisions") — not the ODI metric-style "minimize the time it takes to..." phrasing. These aren't measured yet, just named.

**4. Competing solutions.** What are they using or doing today instead? Push past "nothing" — jobs are almost always being done by something today, even if it's a workaround, a spreadsheet, a manual process, or a competitor's half-fit tool. "Nothing" is usually a sign the question needs to be asked differently ("so how do they get this done right now, even if it's painful?").

**5. Pull of the status quo** *(optional — only if it surfaces naturally, don't force it)*. What's dragging them back to what they do today even if the new thing sounds better? A one-liner is enough — you don't need the full push/pull/anxiety/habit Switch model, just whatever surfaces in conversation.

## Output format

Always save as a markdown file (`create_file` into outputs, then `present_files`) — don't just print it in chat. Name it `[job-name]-jtbd.md`:

```markdown
# [Job Name] — Jobs to Be Done

## Job Statement
When [situation], I want to [motivation], so I can [expected outcome].

## Top Desired Outcomes
- ...
- ...

## Current Workarounds / Competing Solutions
[what they use/do today instead]

## What's Pulling Them Back to the Status Quo
[optional — only if it surfaced naturally]

## Next Step
Feeds discovery-brief's problem statement — the job statement above becomes the seed for "what is the problem?"
```

## Common failure modes to flag

- The "job" is actually a feature or solution restated ("they need a dashboard" isn't a job)
- Desired outcomes are written as ODI-style metrics instead of plain language
- "Competing solutions" gets answered as "nothing" without a second push
- The situation described is really a persona/demographic, not a triggering context

## Handoff

Always end by pointing to `discovery-brief` — offer to kick it off directly, using the job statement above as the seed for its problem statement.
