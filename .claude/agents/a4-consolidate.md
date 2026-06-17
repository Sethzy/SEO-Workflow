---
name: a4-consolidate
description: Step A.4: Consolidate and normalize Ahrefs exports
model: sonnet
color: blue
---
Execute Step A.4 from WORKFLOW.md: Consolidate and Normalize Exports.

Check MEMORY_STATE.md first - skip if completed.

1. If scripts/consolidate-ahrefs.ts exists, run it first
2. Scan docs/marketing/keywords/ for new AHREFS_*.csv and *_AHREFS.csv files
3. Register new exports in ahrefs-exports.csv (status='unprocessed')
4. For each unprocessed export:
   a. Parse CSV, normalize column names (strip CSS class prefixes)
   b. Keyword research → insert into keywords-validated.csv (status='validated')
   c. Competitor exports → insert into competitor-keywords.csv
   d. Mark as 'processed' in ahrefs-exports.csv
5. Parse serp-notes.md if exists
6. Agent SERP analysis: web search top 20 candidates by priority score, classify as winnable/competitive/brand_heavy
7. Record in serp-analysis.csv (data_source='web_search')
8. Update keyword-seeds.csv: status='exported' for processed seeds
9. Update seed-groups.csv status

Update MEMORY_STATE.md: record counts, set next_step=5.