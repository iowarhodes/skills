---
name: roadmap
description: Build an OKR-tied roadmap — Objectives, Key Results, and initiatives placed on a near-term/long-term horizon — auto-populated from existing discovery-brief, opportunity-mapping, and solution-mapping outputs when they exist. STEP 6, the natural close of a first pass through the discovery cycle, but also runs standalone. NOTE — a different skill, `product-management:roadmap-update`, is also installed and handles generic "update my roadmap" requests; trigger THIS skill on more specific phrasing like "build a roadmap from my discovery work," "OKR roadmap," "turn this into a roadmap," "what should our objectives and key results be," or "roadmap this opportunity tree" — not on a bare "update my roadmap," which should go to the other skill.
---

# Roadmap

Turns discovery output (or a standalone conversation) into an OKR-tied roadmap: every initiative ladders up to an Objective and has Key Results, not just a themed list of projects.

```
... → solution-mapping → roadmap
```

**Naming collision note:** `product-management:roadmap-update` is a separate, already-installed skill for generic roadmap updates/reprioritization. This skill is narrower and Torres-flow-specific — it exists to turn discovery-brief/opportunity-mapping/solution-mapping output into an OKR-structured roadmap with validated-vs-speculative confidence tagging. If a request is a plain "update my roadmap" with no discovery context in play, prefer the other skill.

## Time horizons

- **Near-term** = this sprint/month — committed, scoped, someone's building it.
- **Long-term** = this year — directional bets, not yet fully scoped.

## Auto-detect existing work

Before asking the user to build initiatives from scratch, check the project for outputs from earlier Torres-flow skills:
- `*-discovery-brief.md` (skill 01)
- `*-opportunity-map.html` (skill 03)
- `*-solution-map.html` (skill 04)

If found, read them and propose initiatives pre-populated from:
- The **outcome** (discovery-brief's Define section) → candidate Objective
- The **prioritized opportunity** (opportunity-mapping's recommended pick) → candidate initiative
- The **tested solution + its riskiest assumption** (solution-mapping Part B/C) → candidate Key Result — the assumption's validation signal makes a good KR, and whether the test already ran determines the confidence tag below

If nothing's found, run it standalone — ask the user directly for objectives, initiatives, and what "done" looks like for each.

## Process

### 1. Objectives
2-4 big qualitative goals for this horizon. Pull from discovery-brief outcomes if present; otherwise ask directly: "what are the 2-4 big qualitative goals for this cycle?"

### 2. Key Results per objective
2-3 measurable results per objective. Push back on activity-KRs ("ship feature X") — a KR should be an outcome ("increase self-serve completion from 40% to 60%"), not a task. If a proposed KR is really a deliverable, ask what number it's supposed to move.

### 3. Initiatives per KR
The actual workstreams/projects that would move that KR. This is where opportunity-mapping/solution-mapping output slots in directly if it exists — an opportunity or tested solution becomes an initiative under the KR it serves.

### 4. Horizon placement
For each initiative: near-term (this sprint/month) or long-term (this year)? Push back if a long-term initiative has no clear graduation trigger — ask "what would need to be true for this to move to near-term?" A bet with no path to becoming committed work is just a wish, not a roadmap item.

### 5. Confidence flag
For long-term bets specifically, note whether they're **validated** (came from a completed solution-mapping assumption test) or **speculative** (no test run yet). Don't let a speculative bet look as solid as a validated one anywhere on the output — this distinction is the whole point of carrying solution-mapping's evidence forward instead of starting the roadmap from a blank slate.

## Output format

Both required.

**1. Markdown doc** (`create_file` into outputs, then `present_files`). Name it `[project-name]-roadmap.md`:

```markdown
# [Project/Team Name] — Roadmap

## Objectives (this cycle)
### Objective 1: [statement]
**Key Results:**
- KR1: [measurable]
- KR2: [measurable]

**Initiatives:**
| Initiative | Horizon | Confidence | Source |
|---|---|---|---|
| ... | Near-term / Long-term | Validated / Speculative | opportunity-mapping / solution-mapping / manual |

[repeat per objective]

## Open Bets / Unvalidated Assumptions
[long-term initiatives with no validation yet — flag explicitly]
```

**2. Visual swimlane**, rendered inline via the Visualizer (`mcp__visualize__show_widget` — call `read_me` first if not already done this session). One lane per Objective, initiatives placed in Near-term / Long-term columns, confidence shown visually (e.g. solid fill for validated, dashed/outlined for speculative). This is the artifact for the stakeholder conversation; the markdown is the working doc underneath it.

## Handoff

After building, ask whether this should loop back — a long-term speculative initiative is a strong candidate for a `solution-mapping` pass to de-risk it before it graduates to near-term.
