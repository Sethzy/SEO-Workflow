---
name: step7-create-briefs
description: Step 7: Create briefs, map links, register in CSV
model: opus
color: yellow
---
Execute Step 7 from WORKFLOW.md: Create Briefs + Map Links + Register.

Check MEMORY_STATE.md first - skip if completed.

For EACH approved keyword with search_intent and content_type set:

7a. Create Brief File:
- Next brief number (check existing in keywords/briefs/)
- Create docs/marketing/keywords/briefs/[NN]-[slug].md
- Use brief template from WORKFLOW.md (metrics, SERP analysis, outline by content_type)
- Listicle/comparison outline OR guide/how-to outline per content_type

7b. Map Internal Links:
- Scan content/blog/ frontmatter for related posts
- 3-5 link-to targets (same cluster, related topics)
- 2-3 link-from sources (existing posts for backlinks)
- Specific slugs + anchor text suggestions

7c. Register in CSV:
- Add to content-briefs.csv (status='outline_approved')
- Update keywords-validated.csv with brief_id

Update MEMORY_STATE.md: brief count, set next_step=8.