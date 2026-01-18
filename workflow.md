# Agent Workflow: Step-by-Step Execution

## Overview

This workflow consolidates 12 specialist prompts into sequential stages. Execute them in order, producing clear outputs at each stage.

---

## Stage 0: Intake & Validation

**Purpose**: Confirm understanding and document assumptions

**Input**: Completed intake form

**Process**:
1. Review all provided information
2. Identify gaps in information
3. List all assumptions being made
4. Confirm understanding with user

**Output**:
```markdown
### Confirmed Details
- [List provided information]

### Assumptions Made
- [ASSUMPTION: Detail what you're assuming and why]
- [ASSUMPTION: ...]

### Ready to Proceed
[Yes/No - await user confirmation if major assumptions made]
```

---

## Stage 1: Strategic Analysis

**Purpose**: Understand the landscape and position

**Input**: Validated intake information

**Process**:
1. Analyse target audience needs and pain points
2. Identify market context and competitive landscape
3. Map success criteria to strategic approach
4. Highlight opportunities and risks

**Output**:
```markdown
### Audience Profile
- [Key characteristics]
- [Primary needs]
- [Pain points]

### Strategic Position
- [Market context]
- [Competitive angle]
- [Unique value]

### Opportunities & Risks
- Opportunities: [List]
- Risks: [List]
```

---

## Stage 2: Framework Definition

**Purpose**: Establish structure and approach

**Input**: Strategic analysis

**Process**:
1. Define core framework/methodology to use
2. Establish key principles and guidelines
3. Set structural boundaries
4. Identify required components

**Output**:
```markdown
### Framework
- [Name and description of approach]

### Core Principles
1. [Principle]
2. [Principle]
3. [Principle]

### Required Components
- [Component]: [Purpose]
- [Component]: [Purpose]
```

---

## Stage 3: Content Architecture

**Purpose**: Design the structure and flow

**Input**: Framework definition

**Process**:
1. Create high-level content structure
2. Define information hierarchy
3. Map user journey or narrative flow
4. Identify key sections and their purpose

**Output**:
```markdown
### Content Structure
1. [Section]: [Purpose]
   - [Sub-section]
   - [Sub-section]
2. [Section]: [Purpose]
   - [Sub-section]

### Narrative Flow
[Describe the journey/progression]

### Key Touchpoints
- [Critical moment]: [Action/Message]
```

---

## Stage 3.5: Page-Level Recommendations (MANDATORY)

**Purpose**: Convert gap analysis into specific page recommendations with AI visibility goals

**Input**: Content architecture, keyword gaps, competitor analysis, AI visibility opportunities

**INSIGHT-LED ROUTING (MANDATORY)**:

Before recommending any page, the agent MUST decide:
1. **Whether a page is required** (evidence-based decision)
2. **The optimal page type** (service, location, comparison, guide, FAQ hub, blog, etc.)
3. **The primary role of the page** (human SEO, AI visibility, or both)

Decisions MUST be based on:
- **Search demand**: Keyword volume, search trends, opportunity size
- **Pain point frequency and intensity**: Reddit mentions, customer objections, problem severity
- **AI citation patterns**: Which queries trigger AI answers, what content AI cites
- **Lack of quality content**: Competitor gap analysis showing weak or missing content

Each page recommendation MUST include a **short decision rationale** explaining why the page is needed and what insight drove the decision.

**Process**:
1. For each priority keyword cluster, **evaluate need first** (insight-led routing)
2. Recommend specific page type only if evidence supports it
3. Map each recommended page to target keyword set, primary intent, funnel stage, and AI visibility goal
4. Use competitor gap analysis to identify missing pages that rivals rank or get cited for
5. Specify exact URL slug, working title, and recommended content format for each page
6. Define 2-3 AI visibility tactics per page (FAQ schema, concise definition blocks, stats boxes, structured data)
7. Prioritize all page recommendations by impact vs effort

**Page Types to Consider**:
- Service page, location page, comparison page, feature page, guide, FAQ hub, glossary, blog post
- Programmatic template, category page, product page, local/location variant
- AI-optimized answer page, definition page, how-to guide, problem-solution page

**Output**:
```markdown
### Page Backlog (Prioritized by Impact vs Effort)

**Note**: Each page includes a **Decision Rationale** based on search demand, pain point intensity (Reddit), AI citation patterns, and competitor content gaps.

| Priority | Page Type | URL Slug | Working Title | Target Keywords | Intent | Funnel Stage | Primary Role | AI Visibility Goal | Content Format | Impact | Effort | Decision Driver |
|----------|-----------|----------|---------------|-----------------|--------|--------------|--------------|-------------------|----------------|--------|--------|----------------|
| 1 | Comparison page | /dealership-vs-locksmith-car-keys/ | Dealership vs Locksmith for Car Keys | dealership vs locksmith, car key replacement cost | Commercial | Middle | Both | Perplexity source for cost comparison | 2,500 words + comparison table + FAQ schema | HIGH | MEDIUM | Reddit #1 objection (47 mentions) + 0 difficulty + competitor cited 8/10 times |
| 2 | Service page | /emergency-car-locksmith/ | Emergency Car Locksmith: 24/7 Service | lost car keys, emergency locksmith | Transactional | Bottom | Both | ChatGPT citation for "lost car key help" | 1,800 words + FAQ schema + LocalBusiness schema | HIGH | MEDIUM | High search volume + emergency pain point + AI citing competitors |
| 3 | Blog post | /can-locksmith-program-transponder-keys/ | Can Locksmith Program Transponder Keys? | can locksmith program transponder key | Informational | Top | AI Visibility | ChatGPT authoritative answer | 2,000 words + HowTo schema + FAQ schema | HIGH | MEDIUM | Reddit #2 question (35 mentions) + competitor cited 10/10 AI queries |
| 4 | Location page (×8) | /car-locksmith-chelmsford/ | Car Locksmith Chelmsford: Same-Day Service | car locksmith chelmsford | Transactional | Bottom | Both | Google AI Overview inclusion | 1,600 words + GeoShape schema + reviews | MEDIUM | LOW | 1,800+ combined searches + local intent + competitor has 8 location pages |

### Page Recommendations from Gap Analysis

**Gap 1**: Competitor ranks for "dealership vs locksmith car key" (140/month, zero difficulty) but client has no comparison content

**Decision Rationale** (Insight-Led Routing):
- **Search demand**: 140/month with 0 difficulty = quick win opportunity
- **Pain point intensity**: Reddit analysis shows "dealership vs locksmith" as #1 decision objection (mentioned 47 times across 15 threads with high anxiety)
- **AI citation pattern**: Competitor page gets cited 8/10 times in ChatGPT for "should I use dealer or locksmith" queries
- **Content gap**: No comparison content exists; competitor has dedicated page ranking #1
- **Conclusion**: Page REQUIRED. Primary role: BOTH (human SEO + AI visibility). Type: Comparison guide.

- **Recommended page**: `/dealership-vs-locksmith-car-keys/`
- **Page type**: Comparison guide
- **Primary role**: Both human SEO (commercial intent) + AI visibility (comparison queries)
- **Primary keywords**: dealership vs locksmith car key, car key replacement dealer vs locksmith
- **Secondary keywords**: cheaper than dealership, locksmith vs dealer cost
- **Search intent**: Commercial investigation (comparing options before purchase)
- **AI search role**: Source for cost comparison queries in ChatGPT, Perplexity
- **Competitor pages**: [competitor-domain.com/dealer-vs-locksmith/], [competitor2.com/pricing-comparison/]
- **Why new page vs expanding existing**: Dedicated comparison pages rank better for "vs" queries; homepage too broad; service pages too specific
- **AI visibility tactics**:
  1. FAQ schema with "Is locksmith cheaper than dealer?" question
  2. Comparison table with structured data (price, time, quality columns)
  3. Concise summary paragraph in first 100 words optimized for snippet extraction
- **Internal linking**: Link from service pages, homepage "why choose us" section, pricing page
- **30/60/90 placement**: Month 1 (closes critical objection gap)

**Gap 2**: No location pages exist; competitor has 8 location variants ranking for "car locksmith {city}"

**Decision Rationale** (Insight-Led Routing):
- **Search demand**: 290/month for "car locksmith Chelmsford" + 8 similar city variants = 1,800+ combined monthly searches
- **Pain point intensity**: Local intent = high urgency (emergency scenarios, same-day need)
- **AI citation pattern**: ChatGPT returns location-specific recommendations 9/10 times for "locksmith near [city]" queries; competitor location pages cited
- **Content gap**: Zero location pages vs competitor with 8 dedicated city pages ranking positions #1-3
- **Conclusion**: Pages REQUIRED (8 total). Primary role: BOTH (local SEO + AI local recommendations). Type: Location service pages (programmatic template).

- **Recommended page**: `/car-locksmith-chelmsford/` (template for 8 cities)
- **Page type**: Location service page (programmatic template)
- **Primary role**: Both local SEO (transactional local intent) + AI visibility (local recommendations)
- **Primary keywords**: car locksmith Chelmsford, auto locksmith Chelmsford, key replacement Chelmsford
- **Secondary keywords**: 24/7 locksmith Chelmsford, mobile locksmith Chelmsford, emergency car keys Chelmsford
- **Search intent**: Transactional local (ready to book, location-specific)
- **AI search role**: Local recommendation in ChatGPT "find car locksmith near Chelmsford"
- **Competitor pages**: [competitor.com/chelmsford/], [competitor2.com/areas/chelmsford/]
- **Why new page vs expanding existing**: Geo-targeted pages rank better for "{service} + {city}" queries; allows unique local content (landmarks, service areas, local testimonials); better internal linking for geographic expansion
- **AI visibility tactics**:
  1. LocalBusiness schema with GeoShape for Chelmsford coverage area
  2. FAQ: "Do you cover Chelmsford and surrounding areas?" with specific neighborhoods listed
  3. Local testimonials with schema markup (Chelmsford customers)
- **Internal linking**: Link from homepage service area section, main service pages, footer
- **30/60/90 placement**: Month 2 (create 3 location pages), Month 3-4 (remaining 5 cities)

**Gap 3**: Competitor gets ChatGPT citations for "can locksmith program transponder key" but client has no educational content

**Decision Rationale** (Insight-Led Routing):
- **Search demand**: 260/month with 0 difficulty (informational, pre-purchase research)
- **Pain point intensity**: Reddit shows this as #2 most-asked question (35 mentions) with HIGH anxiety ("dealers say only they can do it")
- **AI citation pattern**: Competitor blog post cited 10/10 times in ChatGPT, Perplexity, Claude for "can locksmith program transponder" queries
- **Content gap**: Zero educational content; competitor has authoritative 2,000-word guide ranking #1 and getting all AI citations
- **Conclusion**: Page REQUIRED. Primary role: AI VISIBILITY (informational queries dominate AI search). Type: Educational guide/blog post.

- **Recommended page**: Blog post: `/can-locksmith-program-transponder-keys/`
- **Page type**: Educational guide (FAQ-style)
- **Primary role**: AI visibility (informational queries, pre-purchase research)
- **Primary keywords**: can locksmith program transponder key, do locksmiths program car keys, transponder key programming
- **Secondary keywords**: locksmith vs dealer programming, transponder chip programming cost
- **Search intent**: Informational (learning before decision)
- **AI search role**: Authoritative answer for "can locksmith program transponder" in ChatGPT, Claude, Gemini
- **Competitor pages**: [competitor-blog.com/transponder-programming/], [authority-site.com/locksmith-capabilities/]
- **Why new page vs expanding existing**: Educational content needs dedicated article; too detailed for FAQ section; supports service pages via internal links
- **AI visibility tactics**:
  1. HowTo schema for programming process step-by-step
  2. Concise yes/no answer in first 50 words: "Yes, auto locksmiths can program transponder keys using the same diagnostic equipment as dealerships, typically at 40-60% lower cost."
  3. FAQ schema embedded: "What equipment do locksmiths use?" "Is it the same as dealer programming?"
- **Internal linking**: Link from service pages, homepage FAQ, related blog posts
- **30/60/90 placement**: Month 2 (AI visibility priority)

[Continue for all identified gaps...]

### Page Creation vs Optimization Decision Matrix

| Scenario | Create New Page | Optimize Existing Page |
|----------|----------------|------------------------|
| Keyword cluster has no relevant page | ✅ Create | |
| Keyword cluster shares <30% overlap with existing page | ✅ Create | |
| Existing page is too broad/serves different intent | ✅ Create | |
| Keyword cluster is 30-70% overlap with existing | | ✅ Optimize existing |
| Existing page has authority but needs updating | | ✅ Optimize existing |
| Risk of keyword cannibalization | | ✅ Consolidate into existing |

### AI Visibility Tactics Library (Apply to Recommended Pages)

**For ChatGPT Citations**:
- FAQ schema with direct question-answer pairs
- Concise definition in first 100 words (40-60 words optimal)
- Bullet lists for step-by-step processes
- Statistics with citations (increases authority)

**For Perplexity Sources**:
- Comparison tables with clear data
- "According to [source]" citation format
- Structured data (tables, lists, schemas)
- Up-to-date information (2025-2026 data)

**For Google AI Overviews**:
- Featured snippet optimization (40-60 word answers)
- List format for "how to" queries
- Table format for comparison queries
- Strong E-E-A-T signals (author bio, credentials, reviews)

**For Claude/Gemini**:
- Comprehensive explanations (not just snippets)
- Logical structure with clear headings
- Internal links to related topics
- Balanced perspectives on comparisons
```

**Quality Gate**:
- [ ] Every high-priority keyword cluster has been evaluated with insight-led routing
- [ ] Each page recommendation includes a **decision rationale** based on search demand, pain points, AI patterns, and content gaps
- [ ] Each page specifies **primary role**: human SEO, AI visibility, or both
- [ ] Each page recommendation includes specific URL, title, keywords, intent
- [ ] Competitor gaps are explicitly addressed with page recommendations
- [ ] Each page has 2-3 defined AI visibility tactics
- [ ] Page Backlog is prioritized by impact vs effort
- [ ] Recommendations feed directly into 30/60/90-day roadmap (next stage)
- [ ] No pages recommended without evidence-based justification

---

## Stage 4: Detailed Planning

**Purpose**: Break down execution into actionable tasks

**Input**: Content architecture + Page Backlog (from Stage 3.5)

**Process**:
1. List all required deliverables (incorporating Page Backlog recommendations)
2. Identify dependencies
3. Prioritise tasks
4. Estimate complexity (simple/moderate/complex)

**Output**:
```markdown
### Deliverables
- [ ] [Item]: [Complexity] - [Dependencies]
- [ ] [Item]: [Complexity] - [Dependencies]

### Execution Order
1. [Task group]
2. [Task group]

### Critical Path
[Highlight must-complete items]
```

---

## Stage 5: Core Content Creation

**Purpose**: Develop primary content/deliverables

**Input**: Detailed planning

**Process**:
1. Create core content following the architecture
2. Ensure alignment with framework principles
3. Address target audience needs directly
4. Maintain consistent tone and style

**Output**:
```markdown
### Primary Deliverable
[The main content/document/output]

### Supporting Elements
- [Element]
- [Element]

### Quality Check
- Framework alignment: [✓/✗]
- Audience relevance: [✓/✗]
- Tone consistency: [✓/✗]
```

---

## Stage 6: Optimisation & Enhancement

**Purpose**: Refine and strengthen the output

**Input**: Core content

**Process**:
1. Review against success criteria
2. Identify weak points or gaps
3. Enhance clarity and impact
4. Remove redundancy

**Output**:
```markdown
### Improvements Made
- [Area]: [Change and reason]
- [Area]: [Change and reason]

### Remaining Gaps
- [Gap]: [Recommendation]

### Optimised Deliverable
[Enhanced version or diff from Stage 5]
```

---

## Stage 7: Validation & Testing

**Purpose**: Verify quality and fitness for purpose

**Input**: Optimised content

**Process**:
1. Check against all success metrics
2. Test with audience perspective
3. Verify constraint compliance
4. Identify any risks or issues

**Output**:
```markdown
### Success Metrics Review
- [Metric]: [Status and evidence]
- [Metric]: [Status and evidence]

### Audience Validation
- [Does it solve their problem?]
- [Is it accessible/usable?]

### Constraints Check
- [Constraint]: [Compliant ✓/✗]

### Issues Flagged
- [Issue]: [Severity] - [Recommendation]
```

---

## Stage 8: Implementation Guidance

**Purpose**: Provide clear next steps for execution

**Input**: Validated output

**Process**:
1. List immediate next actions
2. Identify required resources
3. Highlight potential blockers
4. Suggest success tracking methods

**Output**:
```markdown
### Immediate Next Steps
1. [Action]: [Who/What/When]
2. [Action]: [Who/What/When]

### Resources Required
- [Resource]: [Purpose]

### Potential Blockers
- [Blocker]: [Mitigation strategy]

### Tracking & Measurement
- [How to monitor success metrics]
```

---

## Stage 9: Documentation & Handoff

**Purpose**: Package everything for delivery

**Input**: All previous stage outputs

**Process**:
1. Compile all deliverables
2. Create executive summary
3. Document decisions and rationale
4. Provide usage instructions

**Output**:
```markdown
### Executive Summary
[2-3 paragraph overview]

### Deliverables Package
- [Item]: [Location/Format]
- [Item]: [Location/Format]

### Key Decisions Log
- [Decision]: [Rationale]

### Usage Instructions
[How to use/implement the deliverables]
```

---

## Workflow Customisation

### Skip Stages
If a stage doesn't apply, document why and skip:
```
**Stage [X]: [Name]** - SKIPPED
Reason: [Explanation]
```

### Add Stages
Insert custom stages as needed:
```
**Stage [X.5]: [Custom Stage]**
Purpose: [Why this is needed]
[Standard stage structure]
```

### Parallel Execution
Some stages can run in parallel if independent:
- Stages 5 & 7 (if testing prototype)
- Stages 2 & 3 (if framework is predetermined)

---

## Quality Gates

Before proceeding to next stage, ensure:
- [ ] Current stage output is complete
- [ ] Output meets quality standards
- [ ] Dependencies for next stage are met
- [ ] No blocking issues remain

---

## Emergency Procedures

**If stuck**:
1. Document the blocker clearly
2. List what you've tried
3. Ask specific question
4. Don't proceed blindly

**If requirements conflict**:
1. Flag the conflict explicitly
2. Present options with trade-offs
3. Recommend preferred approach
4. Await user decision

---

## AI SEO Strategy Agent: Prompt-to-Workflow Mapping

This section maps the 12 SEO prompts to the 9-stage workflow framework.

### Complete Prompt Execution Flow

#### Stage 0: Intake & Validation
**Prompts Executed**: Intake Form Review
**Outputs**:
- Confirmed business challenge (critical for entire strategy)
- Validated assumptions with `[ASSUMPTION: ...]` labels
- Identified required data sources (HikeSEO, Ahrefs, Reddit, LinkedIn)
- Confirmed business type (determines conditional branches)

---

#### Stage 1: Strategic Analysis
**Prompts Executed**:
1. **Prompt 1**: Business Fundamentals & Revenue Model
2. **Prompt 2**: LinkedIn Company Research
3. **Prompt 4**: HikeSEO Competitive Analysis
4. **Prompt 7**: Reddit Research (Customer Insights)

**Data Sources**:
- LinkedIn: Company structure, team, content activity
- Reddit: Pain points, verbatim language, objections
- HikeSEO: Perceived vs actual SEO competitors
- Intake form: Commercial context, ICP, goals

**Outputs**:
- ICP understanding with customer jobs to be done
- Competitive landscape (perceived vs actual SEO competitors)
- Customer pain points and objections (verbatim quotes)
- Market positioning opportunities
- Revenue model and commercial context

**Key Decision Point**: Business type confirmed here determines which conditional prompts run later.

---

#### Stage 2: Framework Definition
**Prompts Executed**:
1. **Prompt 8**: Full AI + SEO Strategy Document (Sections 1-3)
   - 4-Layer Growth Model (Foundation → High-Intent → Authority → Awareness)
   - E-E-A-T Framework
   - Onpage/Offpage SEO split
   - AI Visibility Integration (ChatGPT, Perplexity, Claude, Gemini)

**Outputs**:
- Strategic framework (4-layer model)
- Core SEO principles
- AI visibility approach
- Onpage vs offpage strategic split
- Measurement framework outline

---

#### Stage 3: Content Architecture
**Prompts Executed**:
1. **Prompt 5**: Traffic & Analytics (HikeSEO/GSC)
2. **Prompt 6**: Ahrefs Content Gap Analysis
3. **Prompt 8**: Full AI + SEO Strategy Document (Sections 4-6)
   - Layer-by-layer tactical recommendations
   - Content strategy structure

**Conditional Branches**:
- **IF Local Business**: Execute **Prompt 3** (Local SEO & GBP Audit)
- **IF E-commerce**: Execute **Conditional Prompt: E-commerce IA Audit**

**Data Sources**:
- HikeSEO: GSC data (clicks, impressions, CTR, positions), on-site recommendations
- Ahrefs: Content gaps, keyword gaps, backlink gaps, top competitor pages
- Google Business Profile (if local): Reviews, Q&A, map pack rankings

**Outputs**:
- Site architecture analysis
- Content gap identification (topics, keywords, formats)
- Keyword gap analysis
- Information architecture recommendations
- Page priority hierarchy
- Local SEO structure (if applicable)
- E-commerce category/product page structure (if applicable)

---

#### Stage 3.5: Page-Level Recommendations (MANDATORY)
**Prompts Executed**:
1. **Prompt 6 Extended Analysis**: Convert Ahrefs content gaps into specific page recommendations
2. **AI Visibility Mapping**: For each gap, define AI citation tactics
3. **Competitor Page Mapping**: Identify exact competitor pages/URLs that rank or get cited

**Data Sources**:
- Ahrefs: Competitor pages, keyword gaps, content gaps (from Stage 3)
- HikeSEO: AI visibility opportunities, current page performance (from Stage 3)
- Reddit: Customer pain points inform page topics (from Stage 1)
- Competitor analysis: Pages that rank or get AI citations (from Stage 1)

**Process**:
1. For each keyword cluster from gap analysis, recommend specific page type (service, location, comparison, guide, FAQ hub, etc.)
2. Map each recommended page to:
   - Target keyword set (primary + secondary)
   - Search intent (informational/commercial/transactional)
   - Funnel stage (top/middle/bottom)
   - AI visibility goal (ChatGPT citation, Perplexity source, Google AI Overview, etc.)
3. Identify competitor pages that rank or get cited that client lacks
4. Specify URL slug, working title, content format for each recommended page
5. Define 2-3 AI visibility tactics per page (FAQ schema, definition block, stats box, structured data)
6. Prioritize by impact vs effort

**Outputs**:
- **Page Backlog Table** (prioritized by impact vs effort)
  - Columns: Priority, Page Type, URL Slug, Working Title, Target Keywords, Intent, Funnel Stage, AI Visibility Goal, Content Format, Impact, Effort
- **Detailed Page Recommendations** (15-25 pages minimum)
  - Each recommendation includes: page type, keywords, intent, competitor URLs, why new page vs expanding existing, AI visibility tactics, internal linking strategy, 30/60/90 placement
- **Page Creation vs Optimization Decision Matrix**
- **AI Visibility Tactics Library** (tactics mapped to each recommended page)

**Quality Gate**:
- [ ] Every high-priority keyword cluster has a page recommendation
- [ ] Each page includes specific URL, title, keywords, intent, AI tactics
- [ ] Competitor gaps explicitly addressed
- [ ] Page Backlog prioritized and ready to feed into 30/60/90-day roadmap

**Critical**: This stage output directly feeds Stage 4 (30/60/90-day roadmap). Each recommended page becomes a concrete task like:
- "Month 1, Week 2: Create `/dealership-vs-locksmith-car-keys/` comparison page targeting [keyword cluster] to close objection gap vs [competitor URL]"

---

#### Stage 4: Detailed Planning
**Prompts Executed**:
1. **Prompt 8**: Full AI + SEO Strategy Document (Sections 7-9)
   - 30/60/90-day roadmap
   - 12-month strategic plan
   - Quarterly themes and goals
2. **Prompt 9**: Jobs to be Done Framework + Keyword Intent Mapping
   - 100-200 keywords with intent categorization
   - JTBD → Search query mapping

**Outputs**:
- 30/60/90-day roadmap with specific actions
- 12-month strategic plan with quarterly themes
- JTBD framework (functional, emotional, social jobs)
- Master keyword list (100-200 keywords)
- Keyword clusters with pillar + supporting terms
- Search intent distribution (informational, commercial, transactional, navigational)
- Priority matrix (quick wins, strategic projects, fill-ins)

---

#### Stage 5: Core Content Creation
**Prompts Executed**:
1. **Prompt 8**: Full AI + SEO Strategy Document (Section 10)
   - Complete strategy document assembly (10 sections, 10,000-12,000 words)
   - Executive summary
   - Detailed recommendations
2. **Prompt 10**: Copy Examples & Content Titles Generator
   - 15-25 page title/meta description examples
   - 50+ FAQ questions with answers
   - 50-100 blog post titles
   - Social media templates
   - Email subject lines
   - Page introductions
   - Schema markup (ready-to-implement)

**Outputs**:
- Complete 25-30 page strategy document
- 2-3 page executive summary
- Prioritized backlog with impact/effort matrix
- Ready-to-use copy examples (not templates, actual copy)
- Master content titles spreadsheet
- FAQ library with schema
- Social media content templates

---

#### Stage 6: Optimisation & Enhancement
**Prompts Executed**:
1. **Conditional Prompt: CRO & Conversion Funnel Analysis**
   - Only if goal includes leads/revenue/conversions
   - 5-stage funnel analysis
   - Friction point identification
   - CRO recommendations
   - A/B testing roadmap

**Conditional Execution**:
- Run if primary goal is: leads, revenue, conversions, sales
- Run if business model is B2B with deal size stated
- Run if business model is e-commerce
- Skip if goal is purely visibility/authority without commercial objective

**Outputs** (if executed):
- Conversion funnel analysis (acquisition → landing → consideration → conversion → nurture)
- Friction points per funnel stage
- CRO quick wins (high impact, low effort)
- Form optimization recommendations
- CTA variations
- Mobile conversion optimization
- Expected conversion rate improvements
- Revenue impact calculations

---

#### Stage 7: Validation & Testing
**Prompts Executed**:
1. **Prompt 11**: QA Validation & Quality Assurance
   - 12-criteria comprehensive review
   - Challenge alignment verification
   - Specificity audit
   - Data foundation check
   - Deliverable completeness

**QA Criteria**:
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

**Pass/Fail Thresholds**:
- 12/12 or 10-11/12: Approve for delivery
- 8-9/12: Revise and re-review
- <8/12: Major rework required

**Outputs**:
- QA report with scoring
- Revision checklist (if needed)
- Approval for delivery or iteration requirements

---

#### Stage 8: Implementation Guidance
**Prompts Executed**:
1. **Prompt 12**: Implementation Task Breakdown & Page-Level Action Mapping
   - Granular tasks for 15-25 priority pages
   - Time estimates and dependencies
   - Resource allocation
   - 30/60/90-day task mapping

**Outputs**:
- Page-level action specifications (15-25 pages)
- Master task list spreadsheet with columns:
  - Task ID, Task Name, Page, Category, Priority, Impact, Effort, Dependencies, Owner, Due Date
- Technical SEO implementation tasks (site-wide)
- Content production tasks (50-100 blog posts with full briefs)
- Link building campaigns with target lists
- Local SEO tasks (GBP, citations, reviews) if applicable
- 30/60/90-day task breakdown
- Resource allocation analysis
- Dependencies and critical path
- Quality checklistsfor page optimization and content

**Total Hours Calculation**:
- Onpage SEO: [X hours]
- Technical SEO: [X hours]
- Content creation: [X hours]
- Link building: [X hours]
- Local SEO: [X hours if applicable]
- **Grand Total**: [X hours]

**Gap Analysis**:
- Required hours/week vs available resources
- Recommendations for hiring/contractors if gap exists

---

#### Stage 9: Documentation & Handoff
**Prompts Executed**: Final Assembly & Packaging

**Deliverables Package**:
1. **Executive Summary** (2-3 pages, client-ready, jargon-free)
2. **Complete SEO + AI Visibility Strategy Document** (25-30 pages)
   - 10 sections from Prompt 8
   - Integrated outputs from all prompts
3. **30/60/90-Day Roadmap** (actionable timeline)
4. **12-Month Strategic Plan** (quarterly themes)
5. **Prioritized Backlog** (impact/effort matrix, all recommendations)
6. **Copy Examples Library**:
   - Page titles & meta descriptions (15-25)
   - FAQs with schema (50+)
   - Blog post titles (50-100)
   - Social media templates
   - Email subject lines
   - Page introductions
7. **Master Implementation Spreadsheet**:
   - All tasks with time estimates
   - Page-level actions
   - Content production briefs
   - Link building targets
8. **QA Report** (validation results)

**Client-Ready Versions**:
- Executive summary (standalone)
- Strategy document (business-focused language)
- Roadmap (visual timeline if possible)
- Implementation guide (task list with owners)

---

### Conditional Prompt Flow Diagram

```
Start → Intake Form (Stage 0)
  ↓
Stage 1: Strategic Analysis
  → Prompt 1: Business Fundamentals
  → Prompt 2: LinkedIn Research
  → Prompt 4: HikeSEO Competitive Analysis
  → Prompt 7: Reddit Research
  ↓
Stage 2: Framework Definition
  → Prompt 8 (Sections 1-3): Strategy Framework
  ↓
Stage 3: Content Architecture
  → Prompt 5: Traffic & Analytics
  → Prompt 6: Ahrefs Content Gap
  → Prompt 8 (Sections 4-6): Layer-by-layer tactics
  → [CONDITIONAL] IF Local → Prompt 3: Local SEO & GBP
  → [CONDITIONAL] IF E-commerce → E-commerce IA Audit
  ↓
Stage 3.5: Page-Level Recommendations (MANDATORY)
  → Convert gaps into specific page recommendations
  → Map pages to keywords, intent, funnel stage, AI goals
  → Identify competitor pages to pattern against
  → Create prioritized Page Backlog table
  → Define AI visibility tactics per page
  ↓
Stage 4: Detailed Planning
  → Prompt 8 (Sections 7-9): 30/60/90 + 12-month plan
  → Prompt 9: JTBD + Keyword Mapping
  ↓
Stage 5: Core Content Creation
  → Prompt 8 (Section 10): Assemble complete document
  → Prompt 10: Copy Examples & Content Titles
  ↓
Stage 6: Optimization & Enhancement
  → [CONDITIONAL] IF goal = leads/revenue → CRO Analysis
  ↓
Stage 7: Validation & Testing
  → Prompt 11: QA Validation (12 criteria)
  ↓
  IF QA Score ≥ 10/12 → Proceed to Stage 8
  IF QA Score 8-9/12 → Revise → Re-run QA
  IF QA Score <8/12 → Major rework → Re-run affected prompts
  ↓
Stage 8: Implementation Guidance
  → Prompt 12: Task Breakdown & Page-Level Actions
  ↓
Stage 9: Documentation & Handoff
  → Package all deliverables
  → Create client-ready versions
  ↓
Delivery Complete
```

---

### Data Flow Between Prompts

**Prompt 1 (Business Fundamentals) outputs feed into**:
- Prompt 8 (commercial context for strategy)
- Prompt 9 (JTBD framework informed by business model)
- Prompt 11 (QA validates commercial alignment)

**Prompt 2 (LinkedIn Research) outputs feed into**:
- Prompt 8 (ICP understanding, competitive positioning)
- Prompt 10 (social media content angles)

**Prompt 3 (Local SEO - conditional) outputs feed into**:
- Prompt 8 (local SEO layer in strategy)
- Prompt 10 (location-specific copy)
- Prompt 12 (GBP optimization tasks)

**Prompt 4 (HikeSEO Competitive Analysis) outputs feed into**:
- Prompt 6 (identify competitor gaps in Ahrefs)
- Prompt 8 (competitive strategy)
- Prompt 9 (competitor keyword targeting)

**Prompt 5 (Traffic & Analytics) outputs feed into**:
- Prompt 6 (context for content gaps)
- Prompt 8 (baseline metrics, priority pages)
- CRO Analysis (funnel performance data)
- Prompt 11 (QA measurement framework)

**Prompt 6 (Ahrefs Content Gap) outputs feed into**:
- **Stage 3.5 (Page-Level Recommendations)** - CRITICAL: Gaps become specific page recommendations
- Prompt 9 (keyword opportunities)
- Prompt 10 (content titles based on gaps)
- Prompt 12 (content production tasks)

**Stage 3.5 (Page-Level Recommendations) outputs feed into**:
- **Prompt 8 (30/60/90-day roadmap)** - CRITICAL: Page Backlog becomes month-by-month tasks
- Prompt 10 (copy examples for recommended pages)
- Prompt 12 (page-level implementation specifications)

**Prompt 7 (Reddit Research) outputs feed into**:
- Prompt 8 (customer pain points inform strategy)
- Prompt 9 (JTBD framework, verbatim language)
- Prompt 10 (FAQ questions, copy using customer language)
- CRO Analysis (objection handling)

**Prompt 8 (Strategy Document) outputs feed into**:
- Prompt 9 (keyword strategy aligns with 4-layer model)
- Prompt 10 (copy examples support strategic priorities)
- Prompt 11 (QA validates strategy completeness)
- Prompt 12 (tasks implement strategy recommendations)

**Prompt 9 (JTBD + Keywords) outputs feed into**:
- Prompt 10 (keywords inform copy, content titles target clusters)
- Prompt 11 (QA checks keyword-copy alignment)
- Prompt 12 (page-level optimization targets specific keywords)

**Prompt 10 (Copy Examples) outputs feed into**:
- Prompt 11 (QA validates copy quality and specificity)
- Prompt 12 (exact copy becomes implementation instructions)

**Prompt 11 (QA Validation) outputs determine**:
- Whether to proceed to Prompt 12 (if passed)
- Which prompts to re-run (if failed)

**Prompt 12 (Implementation Tasks) outputs are final**:
- Granular build manual for execution
- No further prompt processing

---

### Business Type Variations

#### For Local Businesses (B2C, service-based):
**Additional Prompts**:
- Prompt 3: Local SEO & GBP Audit (REQUIRED)

**Emphasis**:
- Layer 1 (Foundation): GBP optimization, local schema, NAP consistency
- Layer 2 (High-Intent): Map pack rankings, "near me" keywords
- Reviews and reputation management
- Local link building (chambers, local directories)

**Deliverable Additions**:
- GBP optimization checklist
- Review generation strategy
- Map pack competitive analysis
- Local citation audit

---

#### For E-commerce:
**Additional Prompts**:
- E-commerce IA Audit (41-question diagnostic) (CONDITIONAL)

**Emphasis**:
- Category/product page architecture
- Product schema
- Faceted navigation SEO
- Internal linking strategy for products
- User-generated content (reviews)

**Deliverable Additions**:
- Category page optimization
- Product page templates
- Faceted navigation recommendations
- Internal linking matrix

---

#### For B2B/SaaS:
**Emphasis**:
- Long sales cycle content (nurture sequences)
- Thought leadership (Layer 3 - Authority)
- LinkedIn distribution strategy
- Demo/trial conversion optimization

**Deliverable Additions**:
- Lead nurture content map
- Thought leadership content calendar
- LinkedIn content strategy
- CRO for demo/trial pages

---

### Quality Gates by Stage

**After Stage 1 (Strategic Analysis)**:
- [ ] ICP clearly defined with pain points
- [ ] Competitive landscape mapped
- [ ] Customer verbatim language captured
- [ ] Business model and commercial context understood

**After Stage 3 (Content Architecture)**:
- [ ] Content gaps identified with data
- [ ] Keyword gaps quantified
- [ ] Site architecture issues documented
- [ ] Conditional prompts determined (local/e-commerce)

**After Stage 3.5 (Page-Level Recommendations)** - MANDATORY:
- [ ] Page Backlog table created with 15-25+ page recommendations
- [ ] Each page mapped to: target keywords, intent, funnel stage, AI visibility goal
- [ ] Competitor gap pages identified with specific URLs
- [ ] URL slugs and working titles defined for each page
- [ ] AI visibility tactics specified (2-3 per page)
- [ ] Pages prioritized by impact vs effort
- [ ] Ready to feed into 30/60/90-day roadmap

**After Stage 5 (Core Content Creation)**:
- [ ] Complete strategy document assembled
- [ ] Copy examples are specific (not templates)
- [ ] 50-100 content titles generated
- [ ] FAQ library created

**After Stage 7 (Validation)**:
- [ ] QA score ≥ 10/12
- [ ] Challenge alignment confirmed
- [ ] All deliverables present
- [ ] No vague recommendations remain

**After Stage 8 (Implementation)**:
- [ ] All priority pages have action specifications
- [ ] Total hours calculated
- [ ] Resource gap identified
- [ ] 30/60/90-day tasks mapped

---

### Success Metrics by Stage

Track these metrics to ensure workflow quality:

**Stage 1**: Number of customer pain points identified (target: 10-15)
**Stage 3**: Number of content gaps found (target: 20-30)
**Stage 3.5**: Number of page recommendations created with decision rationales (target: 15-25 minimum, each with evidence-based justification)
**Stage 4**: Number of keywords mapped (target: 100-200)
**Stage 5**: Number of copy examples generated (target: 50+ FAQs, 15+ titles/metas)
**Stage 7**: QA score (target: ≥10/12)
**Stage 8**: Number of granular tasks created (target: 100-200)

---

### Time Estimates by Stage

**Stage 0**: 15-30 minutes (intake review, assumption documentation)
**Stage 1**: 1-2 hours (4 prompts: business, LinkedIn, competitors, Reddit)
**Stage 2**: 30-45 minutes (framework definition)
**Stage 3**: 1-2 hours (traffic, content gaps, conditional prompts)
**Stage 3.5**: 1-2 hours (page-level recommendations, Page Backlog creation, AI tactics mapping)
**Stage 4**: 1-2 hours (roadmap, keyword mapping)
**Stage 5**: 2-3 hours (strategy assembly, copy generation)
**Stage 6**: 1-2 hours (CRO analysis if applicable)
**Stage 7**: 30-60 minutes (QA validation)
**Stage 8**: 2-3 hours (task breakdown, page specifications)
**Stage 9**: 30-45 minutes (packaging, final assembly)

**Total Workflow Time**: 11-17 hours for complete AI SEO strategy (includes mandatory Page-Level Recommendations stage)

---

### When to Skip Stages

**Skip Stage 6 (CRO)** if:
- Goal is purely visibility/authority
- No conversion funnel exists (pure publishing/media)
- User explicitly states "SEO only, no CRO"

**Skip Prompt 3 (Local SEO)** if:
- Not a local business
- No physical location
- Operating purely online/globally

**Skip E-commerce IA Audit** if:
- Not an e-commerce site
- Lead generation or service-based business
