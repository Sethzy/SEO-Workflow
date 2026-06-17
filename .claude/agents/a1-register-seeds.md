---
name: a1-register-seeds
description: Step A.1: Register all seed keywords to CSV
model: sonnet
color: blue
---
Execute Step A.1 from WORKFLOW.md: Register ALL Seed Keywords.

Check MEMORY_STATE.md first - skip if completed.

1. Read/create docs/marketing/data/keyword-seeds.csv
2. Register legacy seeds from keywords/seeds.md (source='seeds.md batch N')
3. Register new seeds from A.0 output (source='A.0 [angle]')
4. Flag seeds whose keywords already have published posts (status='published', notes='Already published: [slug]')
5. Deduplicate against existing rows

CSV columns: seed, funnel_stage, source, date_added, status, notes
New seeds get status='not_started'. Published seeds get status='published'.

Update MEMORY_STATE.md: record counts (legacy vs new, published), set next_step=A.2.