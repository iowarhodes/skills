---
name: assumption-mapping
description: Surface and prioritize the riskiest assumptions behind a candidate solution before building or testing it, following Teresa Torres' Continuous Discovery Habits. This is STEP 6 of a new discovery project — use it once candidate solutions exist (see solution-mapping skill) and before designing any test. Trigger whenever the user wants to figure out what could go wrong with an idea, needs to identify assumptions, is about to build something and wants a gut-check first, or says things like "what has to be true for this to work" or "help me map assumptions before I test this."
---

# Assumption Mapping

Solo-driver mode: without an engineer in the room to flag feasibility risk, or a PM to flag viability risk, be extra rigorous surfacing assumptions in those two categories rather than defaulting to desirability ("will customers like it"), which is the category a designer's instincts cover best already.

## Core principle

Every solution rests on assumptions across four categories. Torres frames these as: will the customer choose to use it (**desirability**), can the business afford to offer it (**viability**), can it actually be built (**feasibility**), and can people actually use it (**usability**). Testing the solution as a whole is slow and expensive; testing the riskiest individual assumption first is fast and cheap.

## Process

### 1. Pick the leading candidate solution(s)
Pull the top 1-2 solutions from skill 05 (the ones without early-flagged non-starter issues).

### 2. Brainstorm assumptions across all four categories
For the solution, list out what has to be true, sorted into:
- **Desirability** — customers actually want this, will notice it, will choose it over their current workaround
- **Viability** — it fits the business model, doesn't create unacceptable cost/risk/support burden
- **Feasibility** — it's technically buildable with reasonable effort/timeline/existing systems
- **Usability** — once built, people can actually figure out how to use it without confusion

Push to fill in all four categories — solo designers tend to over-generate desirability assumptions and under-generate viability/feasibility ones, since those aren't the home turf.

### 3. Plot on an assumption map
For each assumption, rate two things:
- **Importance**: if this assumption is wrong, does the whole solution fall apart, or is it a minor detail?
- **Evidence**: how much do we already know vs. how much is a total guess?

The assumptions that are both high-importance and low-evidence are the ones to test next — that's the point of the exercise, not to test everything.

### 4. Name the riskiest assumption
Call out the single assumption (or top 2-3) that most threatens the solution if wrong. This becomes the target for the test in the next step.

## Output format

- **Solution restated**
- **Assumption list**, grouped under Desirability / Viability / Feasibility / Usability
- **Assumption map** (call out which are high-importance + low-evidence)
- **Top risky assumption(s)** to test next, clearly flagged

## When to move on

Once the riskiest assumption is named, move to designing a small test for it (skill 07) — don't jump to full production.
