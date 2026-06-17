---
name: a2-prepare-ahrefs
description: Step A.2: Prepare Ahrefs research instructions for user
model: sonnet
color: blue
---
Execute Step A.2 from WORKFLOW.md: Prepare Ahrefs Research Instructions.

Check MEMORY_STATE.md first - skip if completed.

1. Read keyword-seeds.csv, filter rows where status='not_started'
2. Group seeds by funnel_stage (BOFU, MOFU, TOFU)
3. Write seed groups to docs/marketing/data/seed-groups.csv:
   seed, funnel_stage, group_label, workflow_run, date_generated, status
4. Prepare structured instructions for 2 Ahrefs sessions:
   - Session 1 (required, 55 credits): Keywords Explorer with filters KD 0-30, Volume 50+, TP 200+
   - Session 2 (optional, up to 45 credits): SERP overview exports
5. Set status='in_progress' for all included seeds in keyword-seeds.csv
6. Present instructions to user

Update MEMORY_STATE.md: set next_step=A.3.