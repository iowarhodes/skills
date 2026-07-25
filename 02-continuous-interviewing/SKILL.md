---
name: continuous-interviewing
description: Set up and run a weekly continuous customer interviewing habit, following Teresa Torres' Continuous Discovery Habits. This is STEP 2 of a new discovery project — use it right after an outcome has been defined (see discovery-brief skill) and before any opportunity mapping happens, since opportunities get generated FROM these interviews and their aggregated timeline of key moments. Trigger whenever the user wants to plan customer interviews, build an interview snapshot, write interview questions, set up a recurring research cadence, build a timeline of what's happening across interviews, or says things like "I need to start talking to customers" or "how do I get a weekly interview habit going."
---

# Continuous Interviewing

Solo-driver mode: the designer is sourcing, scheduling, running, and synthesizing these interviews themselves — no PM/eng partner sitting in by default. Build in reminders to loop in a second set of eyes on synthesis periodically, since solo synthesis is prone to blind spots.

## Core principle

Continuous interviewing means touching base with customers on a small, steady cadence (Torres recommends weekly) rather than running one big research study. Small and frequent beats large and rare — it keeps the opportunity space current instead of a one-time snapshot that goes stale.

## Process

### 1. Recruit against the outcome, not a persona
Pull up the outcome from step 1. Identify who is closest to the behavior in that outcome statement (e.g., if the outcome is about self-service quoting, recruit dealers who've tried or abandoned quoting recently — not "any dealer").

### 2. Build a lightweight recruiting loop
Suggest low-friction, repeatable recruiting sources: exit-intent prompts, support ticket follow-ups, sales team referrals, an always-on "talk to us" link. The goal is a pipeline that refills itself weekly, not a one-off recruiting sprint.

### 3. Write the interview guide
Generate open-ended, story-based questions anchored to a **recent, specific experience** — not hypotheticals or opinions. Ask about the last time they tried to do the behavior in the outcome, not "what would you want."

Bad: "Would you use a feature that let you save quotes as drafts?"
Good: "Walk me through the last time you tried to put a quote together. What happened?"

### 4. Review the transcript and capture a snapshot
After the interview, work from the recording or transcript rather than relying on live notes — it's easy to miss the exact phrasing in the moment. Read the transcript and pull out a one-page **interview snapshot**:
- A few sentences of context (who, their role, what they were trying to do)
- **Verbatim quotes** for the most notable moments — capture the customer's actual words, not a paraphrase, since exact phrasing often carries the real insight
- **Insights** tagged from those moments — needs, pain points, desires, and any workarounds the customer described, each traced back to the quote it came from

Prioritize getting the quotes and insights right over speed — but don't let transcripts pile up unread; review each one within a day so the context is still fresh enough to catch nuance the transcript alone might miss.

### 5. Key moments in time
For each interview, also produce a chronological list of the most significant events from the conversation. This helps you see the story arc of the interview and is the raw material step 6 rolls up across interviews.

### 6. Aggregate the cross-interview timeline
After each new interview, fold its key moments (step 5) into one running timeline across all interviews so far:
- **Order by journey, not interview date.** Place moments by where they fall in the customer's process (e.g., "starts a quote" → "hits a wall mid-quote" → "saves or abandons"), so moments from different interviews that describe the same point in the journey line up next to each other.
- **Cluster overlapping moments.** When the same or near-same moment shows up across multiple interviews (e.g., "wasn't sure the quote saved" surfaces in 6 of 8 interviews), merge them into one timeline entry tagged with how many interviews it came from.
- **Flag outliers.** A moment that appears in only one or two interviews and doesn't cluster with where the rest of the group converges is an outlier — don't fold it in or discard it. Mark it clearly as low-evidence/an edge case worth watching, distinct from the moments the group is converging on.

This aggregated, evidence-tagged timeline — not any single interview's list — is what becomes the "when" layer of the opportunity tree in opportunity mapping (skill 03). Each overlapping moment is a candidate node opportunities can cluster beneath; outliers may still earn a node, but carried forward with a visibly weaker evidence tag.

### 7. Feed snapshots forward
Each snapshot's tagged moments are the raw material for the opportunity space in the next step. Keep a running log (a google drive spreadsheet) of snapshots so they can be pulled into opportunity mapping.

## Output format

Per interview, produce:
- **Interview snapshot**: context (2-3 sentences) + a list of moments, each with a verbatim quote and its tagged insight (need/pain/desire/workaround)
- **Key moments in time**: a chronological list of the most significant events from the interview
- **Feed snapshots forward**: a running log of all interview snapshots in a google drive spreadsheet
- **Running tally**: after each interview, note whether new insights are still showing up or whether things are converging (a signal for when the opportunity space is getting stable enough to move to mapping)

Across interviews, maintain and refresh one **cross-interview timeline** as a single self-contained HTML file (via create_file into the outputs directory, then present_files) — don't just re-print it in chat each time. Name it `[project-name]-interview-timeline.html`. Inline all CSS and diagram markup (SVG) directly in the file — no external stylesheets, fonts, or CDN scripts — and keep it readable in both light and dark viewing. Render it as a single timeline ordered by the customer's journey:
- Each entry shows the moment description, an evidence badge ("N interviews"), and which interviews it came from
- Overlapping moments (multiple interviews) shown as solid, filled markers along the main line
- Outlier moments (single or rare mention) shown visually distinct — e.g., hollow/dashed marker, off the main line — clearly flagged rather than blended in
- A short legend explaining the solid-vs-outlier marker distinction

## When to move on

Once a handful of interviews (roughly 5-8) are complete, overlapping moments rather than all-new ground, that's the cue to move to opportunity mapping (skill 03) — hand off the cross-interview timeline as its "when" layer. Continuous interviewing itself never fully "ends" — it keeps running in parallel with every later step, and the timeline keeps refreshing as new interviews land.
