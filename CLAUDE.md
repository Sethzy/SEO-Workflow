# Atlas SEO Content Pipeline

Ahrefs-driven SEO content workflow for Atlas. Fully machine-executable.

## Quick Start

To run the workflow, provide both files as context:

```
@WORKFLOW.md @MEMORY_STATE.md go
```

## Project Structure

```
.claude/agents/skills/atlas-seo.md   # SEO content generation skill (Step 8)
WORKFLOW.md                           # Master runbook (11 steps, 4 phases)
MEMORY_STATE.md                       # Execution checkpoint (resume state)
docs/marketing/data/                  # CSV trackers (8 files)
docs/marketing/keywords/briefs/       # Content brief files
```

## Skills

| Skill | Location | Used At |
|-------|----------|---------|
| `/atlas-seo` | `.claude/agents/skills/atlas-seo.md` | Step 8: Generate MDX posts |
| `/content-strategy` | (external) | Step A.0: Seed keyword discovery |
| `/programmatic-seo` | (external) | Step 9: Internal linking |

## Workflow Phases

- **Phase A (Research):** Discover seeds, Ahrefs validation, SERP analysis
- **Phase B (Prioritization):** Score, cluster, approve/defer keywords
- **Phase C (Briefs):** SERP analysis, outlines, internal link mapping
- **Phase D (Production):** Generate MDX, add links, validate, commit

One human handoff: Step A.3 (Ahrefs export). Everything else is autonomous.

## State Management

- `MEMORY_STATE.md` is ground truth for workflow position
- CSVs in `docs/marketing/data/` are ground truth for item-level state
- Always read both `WORKFLOW.md` and `MEMORY_STATE.md` before executing any step
