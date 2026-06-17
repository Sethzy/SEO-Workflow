---
name: step5-prioritize
description: Step 5: Score, cluster, and approve/defer all keywords
model: opus
color: green
---
Execute Step 5 from WORKFLOW.md: Score, Cluster, and Approve ALL Validated Keywords.

Check MEMORY_STATE.md first - skip if completed.

For EACH keyword in keywords-validated.csv where status='validated':

5a. Business Value (1-5) — prompt-based reasoning, no heuristic auto-assign:
- 5: Direct product search, competitor comparison, buying intent
- 4: Solution-aware, evaluating tools
- 3: Problem-aware, seeking solutions
- 2: Informational, tangentially relevant
- 1: Broad awareness, indirect
Set business_value + bv_rationale (one sentence).

5b. priority_score = (business_value * traffic_potential) / (kd + 1)

5c. Assign cluster and pillar per Section 3.2:
- AI Research Tools (Literature Review, Citation Management)
- Second Brain & PKM (Second Brain Apps, Connected Notes)
- NotebookLM Alternatives (Direct Alternatives, Competitor Comparisons)
- Visual Knowledge (Mind Mapping, Concept Visualization)

5d. Decision thresholds:
- priority_score > 150 AND kd < 20 → approved_for_brief
- priority_score 75-150 AND kd 15-30 → approved_for_brief (secondary)
- priority_score < 75 → deferred

One CSV read, one CSV write.
Update MEMORY_STATE.md: counts, set next_step=6.