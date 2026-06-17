---
name: step6-serp-analysis
description: Step 6: SERP analysis and content strategy for keywords
model: sonnet
color: yellow
---
Execute Step 6 from WORKFLOW.md: SERP Analysis + Content Strategy.

Check MEMORY_STATE.md first - skip if completed.

For EACH keyword in keywords-validated.csv where status='approved_for_brief':

6a. SERP Analysis:
- Web search top 10 results
- Record in serp-analysis.csv: keyword, date, top_10_urls (pipe-separated), top_10_titles, opportunity_type, content_format, competitor_strengths, data_source, notes
- Fallback: training knowledge if web search insufficient (data_source='training_knowledge')

6b. Content Strategy:
- search_intent: commercial | informational | comparison
- content_type: listicle | guide | comparison | how-to
- Target word count: 2,000-4,000 based on SERP
- Update keywords-validated.csv with search_intent and content_type

Update MEMORY_STATE.md: count analyzed, set next_step=7.