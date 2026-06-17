---
description: atlas-seo-pipeline
---
```mermaid
flowchart TD
    start_1([Start])
    init_state[init-state]
    a0_discover_seeds[a0-discover-seeds]
    a1_register_seeds[a1-register-seeds]
    a2_prepare_ahrefs[a2-prepare-ahrefs]
    a3_ahrefs_export{AskUserQuestion:<br/>Step A.3: Run Ahrefs Keywords Explorer (55 credits). Save CSVs to docs/marketing/keywords/ as AHREFS_#91;topic#93;.csv. Are exports complete?}
    a4_consolidate[a4-consolidate]
    step5_prioritize[step5-prioritize]
    step6_serp_analysis[step6-serp-analysis]
    step7_create_briefs[step7-create-briefs]
    step8_generate_mdx[[Skill: atlas-seo]]
    step9_internal_links[step9-internal-links]
    step10_validate[step10-validate]
    step11_commit[step11-commit]
    end_1([End])

    start_1 --> init_state
    init_state --> a0_discover_seeds
    a0_discover_seeds --> a1_register_seeds
    a1_register_seeds --> a2_prepare_ahrefs
    a2_prepare_ahrefs --> a3_ahrefs_export
    a3_ahrefs_export -->|All sessions done| a4_consolidate
    a3_ahrefs_export -->|Required only| a4_consolidate
    a4_consolidate --> step5_prioritize
    step5_prioritize --> step6_serp_analysis
    step6_serp_analysis --> step7_create_briefs
    step7_create_briefs --> step8_generate_mdx
    step8_generate_mdx --> step9_internal_links
    step9_internal_links --> step10_validate
    step10_validate --> step11_commit
    step11_commit --> end_1
```

## Workflow Execution Guide

Follow the Mermaid flowchart above to execute the workflow. Each node type has specific execution methods as described below.

### Execution Methods by Node Type

- **Rectangle nodes**: Execute Sub-Agents using the Task tool
- **Diamond nodes (AskUserQuestion:...)**: Use the AskUserQuestion tool to prompt the user and branch based on their response
- **Diamond nodes (Branch/Switch:...)**: Automatically branch based on the results of previous processing (see details section)
- **Rectangle nodes (Prompt nodes)**: Execute the prompts described in the details section below

## Skill Nodes

#### step8_generate_mdx(atlas-seo)

- **Prompt**: skill "atlas-seo" "For each brief in content-briefs.csv where status=outline_approved: 1) Read brief from keywords/briefs/[brief_id].md. 2) Generate publication-ready MDX with full YAML frontmatter. 3) Save to content/blog/[slug].mdx. 4) Add row to blog-posts.csv (status=reviewed). 5) Update MEMORY_STATE.md after EACH post. Check MEMORY_STATE.md items_remaining to skip completed posts."

### AskUserQuestion Node Details

Ask the user and proceed based on their choice.

#### a3_ahrefs_export(Step A.3: Run Ahrefs Keywords Explorer (55 credits). Save CSVs to docs/marketing/keywords/ as AHREFS_[topic].csv. Are exports complete?)

**Selection mode:** Single Select (branches based on the selected option)

**Options:**
- **All sessions done**: Keywords Explorer + optional SERP exports saved to docs/marketing/keywords/
- **Required only**: Keywords Explorer done. Skip SERP exports — agent handles SERP analysis via web search
