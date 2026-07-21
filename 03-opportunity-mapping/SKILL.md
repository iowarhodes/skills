---
name: opportunity-mapping
description: Turn interview snapshots into a mapped opportunity space and the top of an Opportunity Solution Tree, following Teresa Torres' Continuous Discovery Habits. This is STEP 3 of a new discovery project — use it once several customer interviews have been run (see continuous-interviewing skill) and before prioritizing which opportunity to pursue. Trigger whenever the user has a batch of interview notes/snapshots to make sense of, wants to build an opportunity tree, needs to organize needs/pains/desires into themes, or says things like "I have a bunch of interview notes, now what" or "help me build my opportunity space."
---

# Opportunity Mapping

Solo-driver mode: the designer is doing the tagging and clustering themselves. Because a single person's synthesis can drift toward their own pet theories, explicitly flag any theme that rests on one or two interviews rather than a pattern, and don't let it get treated as settled just because it made it onto the tree.

## Core principle

An "opportunity" is a customer need, pain point, or desire — framed from the customer's point of view, not the business's. Opportunities are NOT solutions. "Dealers can't tell if a quote saved" is an opportunity; "add a save confirmation toast" is a solution, and it belongs later in the tree.

## Process

### 1. Pull every tagged moment across snapshots
Gather the tagged moments (needs/pains/desires) from all interview snapshots so far into one list.

### 2. Cluster into opportunities
Group tagged moments that point at the same underlying need. Name each cluster as an opportunity statement, written from the customer's perspective, e.g.:
- "Dealers don't trust that their quote data saved correctly"
- "Contractors want to compare quote versions without losing the original"

Avoid solution-shaped names ("Need an autosave feature") — reframe as the underlying need.

### 3. Look for sub-opportunities
Some opportunities are actually a parent need with smaller needs nested underneath (e.g., "trust that data saved" might break into "wants visual confirmation" and "wants a way to recover from an accidental navigation-away"). Nest these as child opportunities under the parent — this becomes the tree structure. Each parent should have multiple children, and each child should be unique enough to stand on its own. If multiple children in the same parent are really the same need, merge them. If a child is really a solution in disguise, flag it and move it to the solution layer of the tree instead.

### 4. Build the opportunity tree
Structure as a tree with the outcome (from skill 01) at the top, key moments in time in the middle starting with "when," and the opportunity clusters as the layer directly beneath it starting with "I need" or "I want." Each opportunity should plausibly, if addressed, move the outcome. If an opportunity doesn't connect to the outcome, flag it — it may belong to a different outcome or project.

### 5. Note evidence strength
For each opportunity, tag how many separate interviews surfaced it. Distinguish "recurring pattern across N interviews" from "single mention, worth watching."

## Output format

- **Opportunity tree** svg graphic (outcome at top, opportunities as first-level branches, sub-opportunities nested where relevant)
- **Evidence count** per opportunity (how many interviews support it)
- **Flagged risks**: any opportunity that's really a solution in disguise, or that doesn't clearly ladder up to the outcome

## When to move on

Once the opportunity space feels reasonably stable (new interviews are landing on existing branches more often than creating new ones), move to prioritizing which opportunity to pursue first (skill 04).
