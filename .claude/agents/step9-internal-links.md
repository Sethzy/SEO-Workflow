---
name: step9-internal-links
description: Step 9: Add internal links with /programmatic-seo
model: sonnet
color: purple
---
Execute Step 9 from WORKFLOW.md: Internal Links.

BLOCKING: First invoke /programmatic-seo for hub-spoke linking strategy.

Check MEMORY_STATE.md first - skip if completed.

For EACH new MDX file from Step 8:
1. Read brief's internal linking section (Step 7b)
2. Add 3-5 outbound internal links in article content:
   - /use-cases/[slug], /blog/[slug], /vs/[competitor]
   - Descriptive anchor text, contextual placement
3. Update existing posts with backlinks to new post:
   - Open each 'link FROM' target in brief
   - Add markdown link with relevant anchor text
   - Save modified posts

Rules: Min 3 links/post, max 1 per 200 words, cluster siblings interlink.

Update MEMORY_STATE.md: count, set next_step=10.