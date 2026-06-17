---
name: init-state
description: Read WORKFLOW.md and MEMORY_STATE.md to determine current state
model: haiku
color: cyan
---
Execute the Cold Start Protocol from WORKFLOW.md Section 0.1:

1. Read WORKFLOW.md in full.
2. Check if docs/marketing/MEMORY_STATE.md exists.
   - If YES: Read it. Report the current step, status, and items remaining.
   - If NO: Report 'Fresh start - no state file found.'
3. Check all CSV files in docs/marketing/data/ for current status.
4. Report: current phase, current step, items completed, items remaining.
5. If resuming mid-step, list exactly which items still need processing.

Output a clear status summary so the next step knows where to begin.