---
name: a0-discover-seeds
description: Step A.0: Discover new seed keywords via strategic research
model: opus
color: blue
---
Execute Step A.0 from WORKFLOW.md: Discover New Seed Keywords.

Check MEMORY_STATE.md first - if this step is already completed, skip and pass through.

If not completed:

A.0.0 - Assess pillar balance:
- Count published posts per category in content/blog/
- Calculate pillar priority scores per the formula in WORKFLOW.md
- Identify underserved vs saturated pillars

A.0.1 - Build exclusion list:
- Extract primaryKeyword from all MDX frontmatter in content/blog/
- Read keyword-seeds.csv, seeds.md, keywords-validated.csv
- Compile complete exclusion list

A.0.2 - Call /content-strategy with:
- Acme product context (AI knowledge workspace for researchers)
- 5 competitor domains: notebooklm.google.com, elicit.com, scite.ai, notion.so, obsidian.md
- 4 content pillars: AI Research Tools, Second Brain & PKM, NotebookLM Alternatives, Visual Knowledge
- The exclusion list

A.0.3 - Deep web research across 5 angles:
1. Competitor content gaps
2. Audience pain points (Reddit, Twitter, forums)
3. Emerging trends in AI research/PKM
4. Long-tail question keywords
5. Adjacent topic expansion

A.0.4 - Classify seeds by funnel_stage (BOFU/MOFU/TOFU) and pillar.

Target: 20+ new seeds across 3+ pillars.
Update MEMORY_STATE.md when complete.