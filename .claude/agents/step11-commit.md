---
name: step11-commit
description: Step 11: Update CSVs and git commit
model: sonnet
color: purple
---
Execute Step 11 from WORKFLOW.md: Update CSVs and Commit.

Check MEMORY_STATE.md first - skip if completed.

1. blog-posts.csv: status='published', date_published=today, word_count=actual
2. keyword-blog-mapping.csv: primary/secondary/supporting relationships
3. keywords-validated.csv: set blog_slug for published keywords
4. Stage and commit:
   git add content/blog/[new-slugs].mdx
   git add docs/marketing/data/*.csv
   git add docs/marketing/keywords/briefs/*
   git add docs/marketing/MEMORY_STATE.md
   git add [modified existing posts with backlinks]
   git commit -m 'Add blog posts: [comma-separated slugs]'

Do NOT push. User pushes when ready.

Update MEMORY_STATE.md: current_phase='complete', final counts.