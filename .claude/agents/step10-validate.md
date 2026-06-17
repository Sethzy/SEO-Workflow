---
name: step10-validate
description: Step 10: Validate all posts (AI, SEO, AEO/GEO)
model: sonnet
color: purple
---
Execute Step 10 from WORKFLOW.md: Validate + Fix ALL Posts.

Check MEMORY_STATE.md first - skip if completed.

For EACH new MDX file:

10a. AI Writing Detection:
- Em-dashes, 15 overused verbs, 14 overused adjectives, 6 AI transitions, 3 opening red flags, 21 filler words, 6 academic tells
- Critical (blocks): 2+ em-dashes, 3+ overused verbs, any opening red flag

10b. SEO Audit:
- npm run audit:blog if available
- Title 50-60 chars, description 150-160 chars, keyword in title (critical)
- Keyword in first 100 words, 1-2% density, all frontmatter fields
- 4-6 FAQs, heading hierarchy, 2000-4000 words, min 3 internal links
- No broken links, no duplicate primaryKeyword

10c. AEO/GEO (score >= 99 required):
- Commercial: comparison table + 4 FAQs + 2 sourced stats
- Informational: definition in 200 words + steps + 3 evidence claims

10d. Frontmatter-CSV sync

Fix loop: fix all → revalidate → repeat. Safety valve: 5 attempts max.

Update MEMORY_STATE.md: results, set next_step=11.