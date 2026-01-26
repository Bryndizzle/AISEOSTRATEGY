# Complete Prompt Inventory — AI SEO Strategy Agent

This document catalogs all 12+ prompts integrated into the workflow, their purposes, inputs, outputs, and integration points.

---

## Core Prompts (Always Execute)

### Prompt 1: Business Fundamentals & Revenue Model
**File**: `/prompts/01_business_fundamentals.md`
**Workflow Stage**: Stage 1 (Strategic Analysis)
**When to Run**: Always (core strategic input)

**Purpose**: Understand business model, revenue streams, commercial context, and strategic positioning.

**Data Sources**:
- Intake form (Sections 1, 2, 3)
- Company website
- LinkedIn company page (via Prompt 2)

**Outputs**:
- Business model analysis (B2B/B2C/B2B2C)
- Revenue streams and deal size
- Sales cycle length
- Commercial priorities
- Product/service positioning

**Feeds Into**:
- Prompt 8 (commercial context for strategy)
- Prompt 9 (JTBD framework)
- Prompt 11 (QA commercial alignment check)
- CRO Analysis (revenue impact calculations)

---

### Prompt 2: LinkedIn Company Research
**File**: `/prompts/02_linkedin_research.md`
**Workflow Stage**: Stage 1 (Strategic Analysis)
**When to Run**: Always (ICP understanding)

**Purpose**: Research company structure, team, LinkedIn content activity, and ICP engagement patterns.

**Data Sources**:
- LinkedIn company page
- LinkedIn employee profiles
- LinkedIn content posts

**Outputs**:
- Company size and team structure
- Active employees on LinkedIn
- Content themes and engagement
- ICP content preferences
- Thought leadership angles

**Feeds Into**:
- Prompt 8 (ICP understanding, competitive positioning)
- Prompt 10 (social media content angles)

---

### Prompt 4: HikeSEO Competitive Analysis
**File**: `/prompts/04_hikeseo_competitive_analysis.md`
**Workflow Stage**: Stage 1 (Strategic Analysis)
**When to Run**: Always (competitive context)

**Purpose**: Distinguish between perceived competitors (client-listed) and actual SEO competitors (search visibility).

**Data Sources**:
- HikeSEO competitive analysis tool
- Intake form (Section 6: Known competitors)

**Outputs**:
- Perceived vs actual SEO competitors
- Competitor SEO investment levels
- Competitive gaps and opportunities
- Market saturation assessment

**Feeds Into**:
- Prompt 6 (identify competitor gaps in Ahrefs)
- Prompt 8 (competitive strategy)
- Prompt 9 (competitor keyword targeting)

---

### Prompt 5: Traffic & Analytics (HikeSEO/GSC)
**File**: `/prompts/05_traffic_analytics.md`
**Workflow Stage**: Stage 3 (Content Architecture)
**When to Run**: Always (baseline metrics)

**Purpose**: Analyze current traffic, search performance, and AI visibility signals.

**Data Sources**:
- HikeSEO (primary for GSC data)
- Google Search Console (via HikeSEO)
- Ahrefs (traffic estimates only - when GSC unavailable)

**Outputs**:
- Current organic traffic levels
- Top performing pages
- Keyword performance (clicks, impressions, CTR, positions)
- AI visibility signals (ChatGPT citations, Perplexity rankings)
- On-site recommendations from HikeSEO

**Feeds Into**:
- Prompt 6 (context for content gaps)
- Prompt 8 (baseline metrics, priority pages)
- CRO Analysis (funnel performance data)
- Prompt 11 (QA measurement framework)

---

### Prompt 6: Ahrefs Content Gap Analysis
**File**: `/prompts/06_ahrefs_content_gap.md`
**Workflow Stage**: Stage 3 (Content Architecture)
**When to Run**: Always (content opportunities)

**Purpose**: Identify content gaps, keyword gaps, and backlink gaps vs competitors.

**Data Sources**:
- Ahrefs Site Explorer
- Ahrefs Content Gap tool
- Ahrefs Keywords Explorer
- Competitor domains (from Prompt 4)

**Outputs**:
- Content gaps (topics competitors rank for, client doesn't)
- Keyword gaps (keywords to target)
- Backlink gaps (link opportunities)
- Top competitor pages by traffic
- Domain Rating and authority metrics

**Feeds Into**:
- Prompt 9 (keyword opportunities)
- Prompt 10 (content titles based on gaps)
- Prompt 12 (content production tasks)

---

### Prompt 7: Reddit Research (Customer Insights)
**File**: `/prompts/07_reddit_research.md`
**Workflow Stage**: Stage 1 (Strategic Analysis)
**When to Run**: Always (customer voice)

**Purpose**: Extract customer pain points, verbatim language, objections, and unmet needs from Reddit discussions.

**Data Sources**:
- Reddit (relevant subreddits for industry/niche)
- Customer discussions and threads

**Outputs**:
- Customer pain points (10-20)
- Verbatim customer language (quotes)
- Common objections
- Unmet needs
- Jobs to be done insights
- Discussion themes

**Feeds Into**:
- Prompt 8 (customer pain points inform strategy)
- Prompt 9 (JTBD framework, verbatim language)
- Prompt 10 (FAQ questions, copy using customer language)
- CRO Analysis (objection handling)

---

### Prompt 8: Full AI + SEO Strategy Document
**File**: `/prompts/08_strategy_document.md`
**Workflow Stage**: Stages 2, 3, 4, 5 (Framework → Architecture → Planning → Creation)
**When to Run**: Always (core deliverable)

**Purpose**: Assemble comprehensive 25-30 page strategy document with 10 sections.

**10 Sections**:
1. Executive Summary
2. Business Context & Challenge
3. Strategic Framework (4-Layer Model)
4. Layer 1: Foundation (Technical, Onpage, Local)
5. Layer 2: High-Intent (Conversion-focused)
6. Layer 3: Authority (Thought Leadership)
7. Layer 4: Awareness (Top-of-Funnel)
8. AI Visibility Strategy
9. 30/60/90-Day Roadmap
10. 12-Month Strategic Plan

**Outputs**:
- Complete strategy document (10,000-12,000 words)
- Executive summary (2-3 pages)
- 4-layer growth model
- Onpage/offpage recommendations split
- 30/60/90-day roadmap
- 12-month strategic plan
- Prioritized backlog

**Feeds Into**:
- Prompt 9 (keyword strategy aligns with layers)
- Prompt 10 (copy examples support priorities)
- Prompt 11 (QA validates completeness)
- Prompt 12 (tasks implement recommendations)

---

### Prompt 9: Jobs to be Done Framework + Keyword Intent Mapping
**File**: `/prompts/09_jtbd_keyword_mapping.md`
**Workflow Stage**: Stage 4 (Detailed Planning)
**When to Run**: Always (keyword strategy)

**Purpose**: Map customer jobs to search intent and create comprehensive keyword strategy (100-200 keywords).

**Data Sources**:
- Reddit research (Prompt 7)
- Ahrefs Keyword Explorer
- HikeSEO keyword tracking
- Content gaps (Prompt 6)

**Outputs**:
- JTBD framework (functional, emotional, social jobs)
- 100-200 keywords with full metadata
- Keyword clusters (8-15 clusters)
- Search intent distribution
- Priority matrix (impact/effort)
- JTBD → keyword mapping

**Feeds Into**:
- Prompt 10 (keywords inform copy and content titles)
- Prompt 11 (QA checks keyword-copy alignment)
- Prompt 12 (page-level keyword targeting)

---

### Prompt 10: Copy Examples & Content Titles Generator
**File**: `/prompts/10_copy_examples_content_titles.md`
**Workflow Stage**: Stage 5 (Core Content Creation)
**When to Run**: Always (implementation copy)

**Purpose**: Generate ready-to-use copy examples and 50-100 content titles.

**Outputs**:
- 15-25 page title/meta description examples
- 50+ FAQ questions with answers (schema-ready)
- 50-100 blog post titles with metadata
- 10-15 social media templates
- 15-20 email subject lines
- 8-12 page introduction examples
- 10-15 CTA variations
- Schema markup (JSON-LD ready)

**Feeds Into**:
- Prompt 11 (QA validates copy quality)
- Prompt 12 (exact copy becomes implementation instructions)

---

### Prompt 11: QA Validation & Quality Assurance
**File**: `/prompts/11_qa_validation.md`
**Workflow Stage**: Stage 7 (Validation & Testing)
**When to Run**: Always (quality gate before delivery)

**Purpose**: Comprehensive 12-criteria quality review.

**12 QA Criteria**:
1. Challenge Alignment (CRITICAL)
2. Data Foundation
3. Specificity & Actionability
4. Consistency Across Sections
5. Commercial Context Integration
6. Prioritization & Sequencing
7. Deliverable Completeness
8. Tone & Audience Appropriateness
9. E-E-A-T Signals
10. AI Visibility Integration
11. Local SEO (if applicable)
12. Measurement Framework

**Scoring**:
- 12/12 or 10-11/12: Pass → Proceed to Stage 8
- 8-9/12: Revise → Re-run QA
- <8/12: Major rework → Re-run affected prompts

**Outputs**:
- QA report with scores
- Revision checklist (if needed)
- Approval or rework recommendation

**Feeds Into**:
- Stage 8 (if passed)
- Iteration loop (if failed)

---

### Prompt 12: Implementation Task Breakdown & Page-Level Action Mapping
**File**: `/prompts/12_implementation_task_breakdown.md`
**Workflow Stage**: Stage 8 (Implementation Guidance)
**When to Run**: Always (execution manual)

**Purpose**: Transform strategy into granular tasks with page-level specifications.

**Outputs**:
- Page-level action specs (15-25 pages)
- Master task list spreadsheet (100-200 tasks)
- Technical SEO tasks (site-wide)
- Content production briefs (50-100 topics)
- Link building campaigns
- Local SEO tasks (if applicable)
- 30/60/90-day task breakdown
- Resource allocation analysis
- Dependencies and critical path

**Feeds Into**:
- Final delivery (implementation manual for team)

---

## Conditional Prompts (Execute Based on Business Type/Goal)

### Prompt 3: Local SEO & GBP Audit
**File**: `/prompts/03_local_seo_gbp.md`
**Workflow Stage**: Stage 3 (Content Architecture)
**When to Run**: IF business type = Local OR geography = Local/UK city

**Purpose**: Audit Google Business Profile and local search presence.

**Data Sources**:
- Google Business Profile
- Google Maps (map pack analysis)
- Review platforms (Google, Trustpilot, etc.)

**Outputs**:
- GBP optimization checklist
- Map pack competitor analysis (top 5 competitors)
- Review analysis (business + 5 competitors)
- NAP consistency check
- Local citation audit
- Local keyword opportunities

**Feeds Into**:
- Prompt 8 (local SEO layer)
- Prompt 10 (location-specific copy)
- Prompt 12 (GBP optimization tasks)

---

### Conditional Prompt: E-commerce IA Audit
**File**: `/prompts/conditional_ecommerce_ia.md`
**Workflow Stage**: Stage 3 (Content Architecture)
**When to Run**: IF business model = E-commerce

**Purpose**: 41-question diagnostic for e-commerce information architecture.

**Outputs**:
- Category page structure analysis
- Product page template recommendations
- Faceted navigation SEO strategy
- Internal linking matrix
- Product schema recommendations
- User-generated content strategy

**Feeds Into**:
- Prompt 8 (e-commerce-specific tactics)
- Prompt 10 (product page copy)
- Prompt 12 (category/product page tasks)

---

### Conditional Prompt: CRO & Conversion Funnel Analysis
**File**: `/prompts/conditional_cro_conversion_analysis.md`
**Workflow Stage**: Stage 6 (Optimization & Enhancement)
**When to Run**: IF primary goal includes leads/revenue/conversions OR business = B2B with deal size OR business = E-commerce

**Purpose**: 5-stage conversion funnel analysis with CRO recommendations.

**5 Funnel Stages**:
1. Traffic Acquisition
2. Landing & Engagement
3. Consideration & Education
4. Conversion Action
5. Post-Conversion & Nurture

**Outputs**:
- Funnel analysis (current state, friction points)
- CRO quick wins (high impact, low effort)
- Form optimization recommendations
- CTA variations
- A/B testing roadmap (5-10 tests)
- Mobile conversion optimization
- Expected CR improvements
- Revenue impact calculations

**Feeds Into**:
- Prompt 11 (QA validates CRO recommendations)
- Prompt 12 (CRO tasks integrated with SEO tasks)

---

## Prompt Execution Summary

### Total Prompts: 13+ (9 core + 4 conditional)

**Core Prompts (Always Execute)**: 9
1. Business Fundamentals
2. LinkedIn Research
4. HikeSEO Competitive Analysis
5. Traffic & Analytics
6. Ahrefs Content Gap
7. Reddit Research
8. Full Strategy Document
9. JTBD + Keyword Mapping
10. Copy Examples & Content Titles
11. QA Validation
12. Implementation Task Breakdown
13. Content Stimulus (Idea → Multi-Channel Activation)

**Conditional Prompts**: 4
- Prompt 3: Local SEO & GBP (if local business)
- E-commerce IA Audit (if e-commerce)
- CRO & Conversion Analysis (if goal = leads/revenue)
- [Note: Prompt numbering intentionally skips #3 in core flow - it's conditional]

---

## Workflow Execution Order

```
Stage 0: Intake & Validation
  ↓
Stage 1: Strategic Analysis
  → Prompt 1 (Business Fundamentals)
  → Prompt 2 (LinkedIn Research)
  → Prompt 4 (HikeSEO Competitors)
  → Prompt 7 (Reddit Research)
  ↓
Stage 2: Framework Definition
  → Prompt 8 (Sections 1-3: Framework)
  ↓
Stage 3: Content Architecture
  → Prompt 5 (Traffic & Analytics)
  → Prompt 6 (Ahrefs Content Gap)
  → Prompt 8 (Sections 4-6: Layer tactics)
  → [CONDITIONAL] Prompt 3 (Local SEO) IF local business
  → [CONDITIONAL] E-commerce IA IF e-commerce
  ↓
Stage 4: Detailed Planning
  → Prompt 8 (Sections 7-9: Roadmap + 12-month plan)
  → Prompt 9 (JTBD + Keywords)
  ↓
Stage 5: Core Content Creation
  → Prompt 8 (Section 10: Assemble document)
  → Prompt 10 (Copy Examples + Content Titles)
  ↓
Stage 6: Optimization & Enhancement
  → [CONDITIONAL] CRO Analysis IF goal = leads/revenue
  ↓
Stage 7: Validation & Testing
  → Prompt 11 (QA - 12 criteria)
  ↓
  IF Pass (≥10/12) → Stage 8
  IF Revise (8-9/12) → Iterate → Re-QA
  IF Fail (<8/12) → Rework → Re-run prompts
  ↓
Stage 8: Implementation Guidance
  → Prompt 12 (Task Breakdown + Page Actions)
  ↓
Stage 9: Documentation & Handoff
  → Package all deliverables
  → Client-ready versions
  ↓
Delivery Complete
```

---

## Data Source Summary

### Primary Tools Used:
1. **HikeSEO**: GSC data, keyword tracking, on-site recommendations, AI visibility
2. **Ahrefs**: DR, backlinks, content gaps, keyword gaps, traffic estimates
3. **Reddit**: Customer insights, verbatim language, pain points
4. **LinkedIn**: Company research, ICP content patterns
5. **Google Business Profile**: Local SEO data (if applicable)
6. **Google Search Console**: Via HikeSEO integration

### Tool Responsibilities:
- **HikeSEO** = Primary for actual GSC data (clicks, impressions, CTR)
- **Ahrefs** = Primary for competitive analysis, DR, backlink profiles
- **Reddit** = Primary for customer voice and JTBD insights
- **LinkedIn** = Primary for B2B ICP and social content strategy

---

## Integration Points Between Prompts

### Sequential Dependencies (must run in order):
1. Prompt 7 (Reddit) → Prompt 9 (JTBD uses verbatim language)
2. Prompt 9 (Keywords) → Prompt 10 (Copy targets keywords)
3. Prompt 10 (Copy) → Prompt 12 (Copy becomes implementation spec)
4. All prompts → Prompt 11 (QA validates everything)
5. Prompt 11 (QA pass) → Prompt 12 (Only run if QA passed)

### Parallel Execution (can run simultaneously):
- Prompts 1, 2, 4, 7 (all Stage 1 research)
- Prompts 5, 6 (both Stage 3 analysis)

### Cross-References:
- Prompt 4 (competitors) informs Prompt 6 (Ahrefs competitive gaps)
- Prompt 5 (traffic) provides context for Prompt 6 (content gaps)
- Prompt 8 (strategy framework) guides Prompt 9 (keyword alignment with layers)
- All prompts feed into Prompt 11 (comprehensive QA check)

---

## Output File Structure

Recommended file organization for deliverables:

```
/deliverables/
  /strategy/
    - executive_summary.md (2-3 pages)
    - full_strategy_document.md (25-30 pages, 10 sections)
    - qa_report.md (validation results)
  /roadmap/
    - 30_60_90_day_roadmap.md
    - 12_month_strategic_plan.md
    - prioritized_backlog.xlsx
  /copy/
    - page_titles_metas.md (15-25 examples)
    - faqs_library.md (50+ with schema)
    - blog_titles_master_list.xlsx (50-100 titles)
    - social_templates.md
    - email_subjects.md
    - page_introductions.md
    - schema_markup.json
  /implementation/
    - master_task_list.xlsx (100-200 tasks)
    - /pages/
      - homepage.md (page-level action spec)
      - service_page_1.md
      - blog_post_1.md
      [15-25 page specs]
    - technical_seo_tasks.md
    - content_production_briefs.md
    - link_building_campaigns.md
    - local_seo_tasks.md (if applicable)
  /research/
    - business_fundamentals.md (Prompt 1 output)
    - linkedin_research.md (Prompt 2 output)
    - competitive_analysis.md (Prompt 4 output)
    - traffic_analytics.md (Prompt 5 output)
    - content_gap_analysis.md (Prompt 6 output)
    - reddit_insights.md (Prompt 7 output)
    - keyword_mapping.xlsx (Prompt 9 output)
    - local_seo_audit.md (Prompt 3 output, if applicable)
    - cro_analysis.md (CRO prompt output, if applicable)
```

---

## Time Estimates

**Per Prompt**:
- Prompt 1: 20-30 min
- Prompt 2: 15-20 min
- Prompt 3: 30-45 min (conditional)
- Prompt 4: 15-20 min
- Prompt 5: 20-30 min
- Prompt 6: 30-45 min
- Prompt 7: 30-45 min
- Prompt 8: 2-3 hours (largest output)
- Prompt 9: 1-2 hours (100-200 keywords)
- Prompt 10: 1-2 hours (50+ copy examples)
- Prompt 11: 30-60 min (QA review)
- Prompt 12: 2-3 hours (100+ task specs)
- CRO Analysis: 1-2 hours (conditional)
- E-commerce IA: 45-60 min (conditional)

**Total Workflow Time**: 10-15 hours for complete AI SEO strategy (including all conditional prompts)

---

## Success Metrics

### Quantitative Targets:
- Customer pain points identified: 10-20 (Prompt 7)
- Keywords mapped: 100-200 (Prompt 9)
- Keyword clusters: 8-15 (Prompt 9)
- FAQs generated: 50+ (Prompt 10)
- Blog titles created: 50-100 (Prompt 10)
- Page-level specs: 15-25 (Prompt 12)
- Implementation tasks: 100-200 (Prompt 12)
- Strategy document length: 10,000-12,000 words (Prompt 8)
- QA score: ≥10/12 (Prompt 11)

### Qualitative Standards:
- All recommendations are specific (no "improve SEO" vagueness)
- All copy uses customer verbatim language
- All keywords have intent categorization
- All tasks have time estimates and owners
- Strategy directly addresses business challenge
- Deliverables are client-ready (no jargon)

---

## Critical Success Factors

1. **Challenge Alignment**: Every output must connect to solving the stated business challenge
2. **Data Foundation**: All recommendations grounded in Ahrefs, HikeSEO, Reddit, LinkedIn data
3. **Specificity**: No generic advice - everything is actionable and specific
4. **Consistency**: Keywords → Copy → Tasks alignment maintained throughout
5. **Commercial Context**: Revenue model and goals drive prioritization
6. **Customer Voice**: Reddit verbatim language appears in copy and strategy
7. **QA Gate**: No delivery without passing QA validation (≥10/12)

---

## Iteration & Improvement

### If QA Fails:
- Score 8-9/12: Revise specific sections, re-run QA
- Score <8/12: Re-run affected prompts, reassemble, re-run QA

### Which Prompts to Re-run Based on QA Failures:
- Challenge misalignment → Re-run Prompt 8 (strategy document)
- Vague recommendations → Re-run Prompts 10, 12 (copy, tasks)
- Missing data → Re-run Prompts 1-7 (research prompts)
- Inconsistencies → Re-run Prompt 11 (cross-reference check)
- Deliverable gaps → Re-run Prompts 8, 10 (strategy, copy)

---

---

### Prompt 13: Content Stimulus - Idea to Multi-Channel Activation
**File**: `/prompts/13_content_stimulus.md`
**Agent File**: `/content_stimulus_agent.md`
**Workflow Stage**: Stage 5 (Core Content Creation) or Standalone
**When to Run**: When transforming ideas into multi-channel content activations

**Purpose**: Transform a single content idea into a comprehensive activation package: expanded content angles, ICP-aligned messaging, and ready-to-publish copy across multiple social channels.

**Operating Modes**:
1. **Full Stimulus Mode**: Complete workflow from idea to multi-channel copy
2. **Idea Expansion Mode**: Generate derivative content angles only
3. **Channel Sprint Mode**: Create copy for specific channels only
4. **ICP Alignment Mode**: Adapt existing content for different ICPs

**Inputs**:
- Content idea/theme/topic
- ICPs (Ideal Customer Profiles)
- Target channels
- Brand voice
- Goal (engagement, traffic, leads)

**Outputs**:
- Core insight validation
- 8-15 derivative content angles (core, contrarian, practical, story, trend)
- ICP deep mapping (pain points, language, channel preferences)
- Channel strategy matrix
- Ready-to-publish copy for:
  - LinkedIn (posts, carousels)
  - X/Twitter (threads, tweets)
  - Instagram (carousels, reels, stories)
  - TikTok (scripts)
  - YouTube (shorts, long-form outlines)
  - Email (subject lines, body copy)
- Content sequencing calendar (2+ weeks)
- Repurposing pathways

**Feeds Into**:
- Prompt 10 (expanded copy examples)
- Prompt 12 (content production tasks)
- Social media calendar

**Feeds From**:
- Prompt 9 (JTBD framework, keyword clusters)
- Prompt 7 (Reddit verbatim language)
- Prompt 2 (LinkedIn ICP insights)

---

## Future Enhancements

Potential additional prompts to consider:
- **Technical SEO Audit Prompt** (currently embedded in Prompt 8, could be standalone)
- **Link Building Target Research** (currently in Prompt 12, could be expanded)
- **Competitive SERP Analysis** (detailed SERP feature opportunities)
- **Content Refresh Prioritization** (for existing content optimization)
- **Schema Markup Generator** (currently in Prompt 10, could be expanded)
- **International SEO Strategy** (for multi-language/multi-region)
