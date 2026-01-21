# Agent Workflow: Step-by-Step Execution

## Overview

This workflow consolidates 12 specialist prompts into sequential stages. Execute them in order, producing clear outputs at each stage.

---

## Stage 0: Intake & Validation

**Purpose**: Confirm understanding and document assumptions

**Input**: Completed intake form

**Required Information**:
- Business details (name, industry, location, services/products)
- Target audience and customer personas
- Current performance (rankings, traffic, conversions if available)
- Business goals (conversions, awareness, authority)
- Available data (Ahrefs, GSC, competitor info)
- Risk tolerance (conservative, balanced, aggressive)
- **Tone of Voice** (how the brand should sound)

**Tone of Voice Capture**:

Agent must capture TOV using ONE of these methods:

**Method 1: Quick Description** (user provides 1-2 sentences):
- Example: "We're friendly but professional - like a knowledgeable mate who knows their stuff. No corporate jargon, straight-talking Essex business."

**Method 2: Attribute Selection** (user picks 3-5):
- Friendly / Professional / Casual / Formal
- Direct / Conversational / Technical
- Reassuring / Confident / No-nonsense
- Empathetic / Authoritative / Local
- Warm / Bold / Straightforward

**Method 3: Examples** (user provides):
- 1-2 examples of content they LOVE (that sounds like their brand)
- 1-2 examples they HATE (sounds wrong for their brand)

**Method 4: Detailed Template**:
```
Tone of Voice Profile:
- Primary personality: [e.g., Friendly but professional]
- Key attributes: [e.g., Direct, reassuring, no-nonsense]
- Avoid: [e.g., Corporate jargon, over-promising]
- Formality level: [Casual / Professional / Formal]
- Language complexity: [Simple / Technical]
- Example phrases we'd use: [3-5 examples]
- Example phrases we'd NEVER use: [3-5 examples]
```

**If TOV Not Provided**:
- Agent asks: "How would you describe your brand's tone of voice? (e.g., friendly, professional, no-nonsense, etc.)"
- If still unclear, use: "Professional, clear, helpful - avoids corporate jargon and over-promising"

**Process**:
1. Review all provided information
2. **Capture Tone of Voice** (required for all content creation)
3. Identify gaps in information
4. List all assumptions being made
5. Confirm understanding with user

**Output**:
```markdown
### Confirmed Details
- Business: [Name, industry, location]
- Services/Products: [List]
- Target audience: [Description]
- Current performance: [Rankings, traffic if known]
- Business goals: [Conversions / Awareness / Authority]
- Risk tolerance: [Conservative / Balanced / Aggressive]

### Tone of Voice
**Primary tone**: [Description]
**Key attributes**: [3-5 descriptors]
**Avoid**: [What NOT to sound like]
**Example**: [1-2 example phrases in this tone]

[Agent confirms understanding of TOV and will apply consistently across all content]

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

## Stage 2.5: Keyword Priority Analysis (MANDATORY)

**Purpose**: Identify top 20-30 keywords that will drive 80% of results, map to pages, create tracking framework

**Input**: Strategic analysis (Stage 1) + Framework definition (Stage 2) + Current keyword data

**Why Critical**: Without clear keyword priorities, page creation is unfocused. This stage ensures every page targets specific, high-value keywords with realistic traffic projections.

**Process**:
1. Analyze all keyword data (current rankings + competitor gaps)
2. Calculate opportunity scores (volume × position factor × intent multiplier)
3. Identify "The Big One" (highest single opportunity - typically one keyword/cluster with massive potential)
4. Map keywords to specific pages (prevent cannibalization)
5. Create Top 5 quick reference (80/20 rule)
6. Organize by week (timeline for which keywords when)
7. Create tracking framework (tools, metrics, success targets)

**Opportunity Score Formula**:
```
Opportunity Score = (Volume / 100) × Position Factor × Intent Multiplier

Position Factor:
- Position 4-10: 10 points (low-hanging fruit)
- Position 11-20: 5 points
- Position 21-50: 2 points
- Not ranking but competitor ranks: 3 points

Intent Multiplier:
- Transactional (buy, get, near me): 1.5x
- Commercial (cost, vs, best): 1.2x
- Informational (how, why, what): 1.0x
```

**Output**:
```markdown
### THE BIG ONE: [Keyword/Cluster Name]

[Single highest-impact opportunity]

| Keyword | Volume | Current Pos | Target Pos | Page |
|---------|--------|-------------|------------|------|
| [Keyword] | [Vol] | #[Pos] | #1-3 | [URL] |

**Total Volume**: X searches/month
**Current Traffic**: ~X clicks/month
**Potential Traffic**: X-Y clicks/month
**Traffic Gain**: +X-Y clicks/month
**Lead Gain**: +X-Y leads/month
**Revenue Gain**: £X-Y/month

**Action**: [Specific action, timeline]

---

### Top 20 Keywords by Priority

| # | Keyword | Volume | Current Pos | Target Pos | Page | Action | Week |
|---|---------|--------|-------------|------------|------|--------|------|
| 1 | [Keyword] | [Vol] | #[Pos] | #1-3 | [URL] | [Action] | [Week] |
| 2 | [Keyword] | [Vol] | #[Pos] | #1-3 | [URL] | [Action] | [Week] |
[... continue to 20]

---

### Keyword-to-Page Mapping

**Homepage (/):**
- Primary: [Keyword 1], [Keyword 2]
- Secondary: [Keyword 3], [Keyword 4]
- Combined Volume: [X]
- Potential Traffic: [X-Y] clicks/month

**[Page 2] ([URL]):**
- Primary: [Keyword 1], [Keyword 2]
- Secondary: [Keyword 3], [Keyword 4]
- Combined Volume: [X]
- Potential Traffic: [X-Y] clicks/month

[Repeat for all priority pages]

---

### Top 5 Quick Reference (80/20 Rule)

If you only focus on 5 keywords, make it these:

| Priority | Keyword | Volume | Current | Target | Page | Why Critical |
|----------|---------|--------|---------|--------|------|--------------|
| 🔴 #1 | [Keyword] | [Vol] | #[Pos] | #1-3 | [URL] | [Reason] |
| 🔴 #2 | [Keyword] | [Vol] | #[Pos] | #1-3 | [URL] | [Reason] |
| 🟠 #3 | [Keyword] | [Vol] | #[Pos] | #1-3 | [URL] | [Reason] |
| 🟠 #4 | [Keyword] | [Vol] | #[Pos] | #1-3 | [URL] | [Reason] |
| 🟠 #5 | [Keyword] | [Vol] | #[Pos] | #1-3 | [URL] | [Reason] |

---

### Keyword Priority by Week

**Week 1**: [Theme - e.g., "Homepage/Foundation Keywords"]
- [Keyword 1] ([Vol])
- [Keyword 2] ([Vol])
**Action**: [What to do]

**Week 2**: [Theme - e.g., "The Big One"]
- [Keyword 1] ([Vol])
- [Keyword 2] ([Vol])
**Action**: [What to do]

[Continue for 12 weeks]

---

### Tracking Framework

**Primary Tool**: [Google Search Console / Hike SEO / Ahrefs]

**Weekly Metrics**:
- Position changes for top 20 keywords
- Click volume from top 20 keywords
- Impressions and CTR trends

**Success Targets**:
- Week 4: [X] keywords in top 10
- Week 8: [Y] keywords in top 10, [Z] in top 3
- Week 12: [A] keywords in top 10, [B] in top 3

---

### Summary Numbers

**Top 20 Keywords Total:**
- Total Volume: [X] searches/month
- Current Traffic: ~[Y] clicks/month
- Potential Traffic: [A-B] clicks/month
- Traffic Gain: +[C-D] clicks/month
- Lead Gain: +[E-F] leads/month
- Revenue Gain: £[G-H]/month
```

**Quality Gate**:
- [ ] "The Big One" clearly identified (highest-impact opportunity)
- [ ] Top 20 keywords represent at least 80% of realistic opportunity
- [ ] Each keyword mapped to exactly ONE primary page (no cannibalization)
- [ ] Keywords organized by week align with page creation schedule
- [ ] Top 5 Quick Reference truly captures 60-80% of impact
- [ ] Tracking framework is specific (not generic "monitor rankings")
- [ ] Potential traffic numbers are realistic (use CTR benchmarks by position)
- [ ] Revenue projections use client's actual average job value

**Integration with Other Stages**:
- **Feeds into Stage 3 (Content Architecture)**: Keyword clusters inform site structure
- **Feeds into Stage 3.5 (Page Recommendations)**: Each page references specific keywords from Stage 2.5
- **Feeds into Stage 4 (30/60/90 Roadmap)**: Week-by-week plan organized around keyword priorities

---

## Stage 3: Content Architecture

**Purpose**: Design the structure and flow

**Input**: Framework definition + Keyword priorities (from Stage 2.5)

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

## Stage 3.1: Technical SEO Audit (MANDATORY)

**Purpose**: Identify and prioritize technical SEO issues blocking rankings, indexability, and user experience

**Input**: Website URL, Google Search Console access (if available), CMS platform

**Why Critical**: Technical issues can completely block SEO efforts. A slow site with indexability problems won't rank no matter how good the content is. This stage identifies what's broken and how to fix it.

**Process**:
1. **Core Web Vitals Analysis** - LCP, FID/INP, CLS (mobile + desktop)
2. **Indexability & Crawlability Audit** - Robots.txt, sitemap, noindex tags, canonicals, GSC coverage
3. **Mobile Usability Audit** - Mobile-friendly test, viewport, tap targets, text readability
4. **Site Speed Optimization** - Page load time, TTFB, image optimization, caching, CDN
5. **Schema Markup Audit** - Existing schema, missing opportunities (LocalBusiness, Service, FAQPage, HowTo)
6. **Internal Linking Structure** - Orphan pages, broken links, anchor text, pillar/hub structure
7. **HTTPS & Security Audit** - SSL status, mixed content, security headers
8. **URL Structure Audit** - Clean URLs, trailing slashes, parameters, consistency

**Output**:
```markdown
## Technical SEO Audit Summary

### 🔴 CRITICAL Priority (Fix Week 1)

| Issue | Category | Impact | Difficulty | Time | Expected Outcome |
|-------|----------|--------|------------|------|------------------|
| [X] pages not indexed | Indexability | CRITICAL | EASY | 1 hour | [X] high-value pages indexed |
| Robots.txt blocking pages | Indexability | CRITICAL | EASY | 30 mins | [X] pages crawlable |
| Slow LCP (>4s mobile) | Core Web Vitals | CRITICAL | MEDIUM | 4-6 hours | LCP <2.5s |
| Text too small on mobile | Mobile Usability | HIGH | EASY | 30 mins | Better mobile UX |
| LocalBusiness schema missing | Schema | CRITICAL | EASY | 30 mins | Map Pack eligibility |

**Week 1 Total Time**: 9-13 hours
**Week 1 Impact**: Major improvements in indexing, mobile UX, local visibility

---

### 🟠 HIGH Priority (Fix Week 2-3)

| Issue | Category | Impact | Difficulty | Time | Expected Outcome |
|-------|----------|--------|------------|------|------------------|
| High CLS score | Core Web Vitals | HIGH | MEDIUM | 3-4 hours | CLS <0.1 |
| No HTTPS redirect | Security | HIGH | EASY | 15 mins | All traffic HTTPS |
| Render-blocking resources | Site Speed | HIGH | MEDIUM | 3-4 hours | Faster render |
| FAQPage schema missing | Schema | HIGH | EASY | 3-4 hours | FAQ rich results |
| Orphan pages | Internal Linking | MEDIUM | EASY | 2-3 hours | Better discovery |

**Week 2-3 Total Time**: 15-22 hours
**Week 2-3 Impact**: Speed improvements, rich results eligibility

---

### 🟡 MEDIUM Priority (Fix Week 4-6)

| Issue | Category | Impact | Difficulty | Time | Expected Outcome |
|-------|----------|--------|------------|------|------------------|
| Slow TTFB | Site Speed | MEDIUM | MEDIUM | 2-4 hours | Faster initial load |
| No CDN | Site Speed | MEDIUM | EASY | 1-2 hours | 30-50% faster |
| Redirect chains | Indexability | MEDIUM | MEDIUM | 2-3 hours | Better crawling |

**Week 4-6 Total Time**: 13-22 hours

---

## Detailed Fix Instructions

### Fix 1: Pages Not Indexed
**Issue**: [X] important pages not appearing in Google Search Console index
**Cause**: [noindex tag / robots.txt block / redirect / soft 404]

**How to Fix**:
1. Remove noindex tags from affected pages
2. Check robots.txt not blocking pages
3. Submit sitemap to GSC
4. Request indexing via URL Inspection Tool

**Expected Impact**: [X] pages indexed within 1-2 weeks
**Time**: 1 hour

---

### Fix 2: Slow LCP (Largest Contentful Paint)
**Current**: [X]s on mobile (Target: <2.5s)
**Cause**: Large unoptimized images, render-blocking JS

**How to Fix**:
1. Compress hero image to WebP (<150KB)
2. Add `loading="eager"` to above-fold images
3. Preload critical images: `<link rel="preload" as="image">`
4. Implement image CDN (Cloudflare, Cloudinary)

**Expected Impact**: LCP from [X]s to ~2.0s
**Time**: 4-6 hours

---

[Continue for all critical/high priority issues with detailed fix instructions]

---

## Total Technical SEO Effort

**Critical + High Priority (Weeks 1-3)**: 24-35 hours
**Medium Priority (Weeks 4-6)**: 13-22 hours
**Grand Total**: 37-57 hours

**Expected Overall Impact**:
- [X]+ pages indexed
- LCP improved from [X]s to <2.5s
- Mobile usability: PASS
- [X] rich result types eligible
- [X]% faster page loads
```

**Quality Gate**:
- [ ] All critical issues identified with specific fix instructions
- [ ] Time estimates realistic for each fix
- [ ] Expected outcomes quantified (not "better" but "LCP <2.5s")
- [ ] Priority order based on impact vs effort (not just impact alone)
- [ ] Code examples provided where applicable (robots.txt, schema, .htaccess)
- [ ] Integration with 30/60/90 roadmap (Critical = Week 1, High = Weeks 2-3, etc.)

**Integration with Other Stages**:
- **Feeds from Stage 3**: Technical issues may have been identified in gap analysis
- **Feeds into Stage 3.5**: Don't recommend new pages if existing pages can't be indexed
- **Feeds into Stage 7**: Technical fixes integrated into implementation roadmap with priorities

**See Full Enhancement**: `/AGENT_ENHANCEMENTS/stage_3.1_technical_seo_audit.md` for complete audit framework with all 8 categories

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

## Stage 6.5: E-E-A-T Quality Assurance (MANDATORY)

**Purpose**: Ensure all content meets Google's E-E-A-T (Experience, Expertise, Authoritativeness, Trustworthiness) standards

**Input**: Drafted content (from Stage 5, Stage 6, or Full Page Draft Generator)

**Why Critical**: Google's algorithms explicitly prioritize content demonstrating E-E-A-T. Content failing these standards will not rank regardless of technical optimization. This is especially critical for YMYL (Your Money or Your Life) topics.

**Reference**: [Google's Helpful Content Guidelines](https://developers.google.com/search/docs/fundamentals/creating-helpful-content)

**Process**: Audit content against 30 questions across 5 categories:
1. **Content Quality & Originality** (8 questions) - Original information, comprehensive, insightful analysis
2. **Expertise & Experience** (7 questions) - Trust signals, first-hand expertise, clear authorship
3. **Content Creation Process** (4 questions) - Transparency about "How" content was created, AI disclosure
4. **Content Purpose** (6 questions) - "Why" content exists - people-first vs search engine-first
5. **Search Engine-First Red Flags** (5 questions) - Warning signs of manipulative content

**Scoring System**:
- Each question: 1.0 (Pass), 0.5 (Partial), 0.0 (Fail)
- Total: X/30 points

**Pass Thresholds**:
- **Standard Content**: 24/30 (80%) to pass
- **YMYL Content** (health, finance, safety, legal): 27/30 (90%) to pass

**Output**:
```markdown
## E-E-A-T Quality Assurance Audit

**Content**: [Page title]
**Score**: [X]/30 ([X]%)
**YMYL Status**: [Yes/No]
**Overall Status**: ✅ PASS / ⚠️ NEEDS IMPROVEMENT / ❌ FAIL

---

### Scoring by Category

| Category | Score | Percentage | Status |
|----------|-------|------------|--------|
| Content Quality & Originality | [X]/8 | [X]% | ✅/⚠️/❌ |
| Expertise & Experience | [X]/7 | [X]% | ✅/⚠️/❌ |
| Content Creation Process | [X]/4 | [X]% | ✅/⚠️/❌ |
| Content Purpose | [X]/6 | [X]% | ✅/⚠️/❌ |
| Search Engine-First (Red Flags) | [X]/5 | [X]% | ✅/⚠️/❌ |

---

### Critical Issues (Must Fix Before Publishing)

**Priority 1 - CRITICAL** (Scored 0.0):
1. **[Question #]**: [Issue description]
   - **Problem**: [What's wrong]
   - **Fix**: [Specific remediation steps]
   - **Time**: [Estimate]

2. [Continue for all critical issues...]

---

### Improvement Opportunities (Partial Scores)

**Priority 2 - MEDIUM** (Scored 0.5):
1. **[Question #]**: [Issue description]
   - **Problem**: [What could be better]
   - **Fix**: [Specific remediation steps]
   - **Time**: [Estimate]

---

### Strengths (What's Working Well)

✅ [List aspects that scored 1.0]
✅ [Trust signals present]
✅ [Expertise demonstrated]

---

### E-E-A-T Quick Reference Checklist

**Trust Signals**:
- [ ] Author byline with credentials present
- [ ] Author bio or link to About page
- [ ] Business credentials (years in business, certifications, reviews)
- [ ] Sources cited for all statistics/data
- [ ] Professional presentation (no typos, good formatting)

**Expertise Signals**:
- [ ] First-hand experience demonstrated
- [ ] Technical details only expert would know
- [ ] Industry terminology used correctly
- [ ] Common misconceptions corrected

**Originality**:
- [ ] Original insights (not rewritten from competitors)
- [ ] Unique data, research, or case studies
- [ ] Non-obvious information provided

**People-First Content**:
- [ ] Genuinely helpful (not just keyword-optimized)
- [ ] Solves real problem
- [ ] Natural language (not keyword stuffed)
- [ ] Complete information (answers all key questions)

**Red Flags** (Must be NONE):
- [ ] NO keyword stuffing
- [ ] NO content created purely for rankings
- [ ] NO mass content across unrelated topics
- [ ] NO summarizing others without adding value
- [ ] NO writing to hit word count target

---

### Remediation Priority List

**Fix in this order**:

**Priority 1 (MUST FIX BEFORE PUBLISHING)**:
- [ ] [Critical issue 1] - [Time]
- [ ] [Critical issue 2] - [Time]

**Total Time to Fix Critical Issues**: [X] hours

---

### Recommendation

**IF PASS** (✅):
- Content meets E-E-A-T standards
- ✅ **APPROVED FOR PUBLISHING**
- Optional improvements can be implemented later

**IF NEEDS IMPROVEMENT** (⚠️):
- ⚠️ **REVISIONS REQUIRED BEFORE PUBLISHING**
- Fix Priority 1 issues (critical)
- Consider Priority 2 issues (recommended)
- Estimated time to pass: [X] hours

**IF FAIL** (❌):
- ❌ **MAJOR REVISIONS REQUIRED - DO NOT PUBLISH**
- Content does not meet Google's helpful content standards
- High risk of algorithmic penalty or poor rankings
- Consider: Is this content worth creating?

---

### Key Questions to Fix Common Failures

**Content Quality**:
- Q1: Does content provide ORIGINAL information? (not rewritten from competitors)
- Q2: Is it COMPREHENSIVE? (covers all relevant aspects)
- Q3: Provides INSIGHTFUL analysis beyond obvious?

**Expertise**:
- Q9: TRUST signals present? (author credentials, sources cited, business credentials)
- Q12: Written by EXPERT with demonstrable knowledge?
- Q14: FIRST-HAND expertise demonstrated? ("In our experience...")

**People-First vs Search-First**:
- Q20: Created to HELP PEOPLE (not manipulate rankings)?
- Q26: NOT primarily for search engines?
- Q28: NOT just summarizing others?

**YMYL-Specific** (if health/finance/safety topic):
- Must score 27+/30 (90%+)
- Must have clear expert credentials
- Must cite authoritative sources
- Must include disclaimers if giving advice
```

**Quality Gate**:
- [ ] Content scored and categorized
- [ ] All critical issues identified with specific fixes
- [ ] Pass threshold met (24/30 standard, 27/30 YMYL)
- [ ] NO search engine-first red flags present
- [ ] Trust signals present (author, credentials, sources)
- [ ] First-hand expertise demonstrated
- [ ] Content would be useful to direct customers (not just search traffic)

**Integration with Other Stages**:
- **Feeds from Stage 5/6**: Content to audit
- **Feeds into Stage 7**: Only content passing E-E-A-T proceeds to validation
- **Mandatory Quality Gate**: NO CONTENT PUBLISHED WITHOUT PASSING E-E-A-T AUDIT

**YMYL Content Special Requirements**:
- Higher pass threshold: 90% (27/30) vs 80% (24/30)
- Must have expert authorship with clear credentials
- Must cite authoritative sources (medical, financial, legal)
- Must include appropriate disclaimers
- Must be reviewed by qualified professional (ideally)
- Must be updated more frequently (every 6 months minimum)

**See Full Enhancement**: `/AGENT_ENHANCEMENTS/stage_6.5_eeat_quality_assurance.md` for complete 30-question audit framework, scoring rubrics, and detailed remediation guidance

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

## Stage 7.5: Link Building Strategy & Outreach (MANDATORY)

**Purpose**: Provide specific link building targets, outreach templates, digital PR angles, podcast/YouTube opportunities

**Input**: Industry/niche (Stage 1), competitor backlink analysis (Stage 3), page priorities (Stage 3.5), timeline (Stage 7)

**Why Critical**: "Build links" is not a plan. This stage provides 50-100 specific targets, ready-to-use templates, and a 90-day execution roadmap.

**Process**:
1. **Competitor Backlink Gap Analysis** - Identify high-value links competitors have that client doesn't
2. **Resource Page Targets** - 10-20 specific resource pages to pitch
3. **Broken Link Building** - 10-15 broken link opportunities
4. **Guest Posting Targets** - 15-25 blogs/sites with pitch ideas
5. **Digital PR Story Angles** - 10-15 newsworthy angles for journalist outreach
6. **Podcast Outreach** - 10-20 podcasts with episode topic ideas
7. **YouTube Collaborations** - 10-15 channels with collaboration concepts
8. **HARO/Journalist Outreach** - Setup + target publications
9. **Industry Directories** - 5-10 high-DR trade directories
10. **Outreach Templates** - 8 ready-to-use email templates for each tactic

**Output**:
```markdown
## Link Building Strategy: 90-Day Plan

### Target: 30-43 High-Quality Backlinks in 90 Days

**Breakdown by Tactic**:
- Industry directories & associations: 5-10 links
- Resource pages: 4-6 links
- Broken link building: 3-5 links
- Guest posts: 6-10 links
- HARO / journalist features: 4-8 links
- Podcast appearances: 2-4 links
- YouTube collaborations: 1-2 links
- Digital PR: 3-5 links

---

## 1. Competitor Backlink Gap Analysis

**Top Competitor Links (Client Doesn't Have)**:

| Linking Domain | DR | Type | Target URL | Link Context | Difficulty | How to Acquire |
|----------------|----|----|------------|--------------|------------|----------------|
| [domain.com] | 65 | Resource page | [competitor-url] | "Best [service] in [area]" list | LOW | Email webmaster, request inclusion (Template #2) |
| [domain.com] | 72 | Guest post | [competitor-url] | Author bio link | MEDIUM | Pitch guest post on [topic] (Template #1) |
| [domain.com] | 58 | Directory | [competitor-url] | Trade directory listing | EASY | Submit to directory (£[cost]) |

**Total High-Value Gaps**: [X] links identified

---

## 2. Podcast Outreach Targets (10-20 podcasts)

### Podcast 1: [Podcast Name]
- **URL**: [Spotify/Apple/website link]
- **Host**: [Name]
- **Audience**: [Description, size]
- **Why You're a Good Fit**: [Industry expertise, local angle, interesting story]
- **Suggested Episode Topics**:
  1. "[Topic 1 - e.g., 'How to Avoid £400 Car Key Emergencies']"
  2. "[Topic 2 - e.g., 'Starting a Trade Business in Your 20s: Lessons from Essex']"
  3. "[Topic 3 - e.g., 'The Future of Car Security Technology']"
- **Link Opportunity**: Show notes link to website
- **Contact**: [Email or booking form]
- **Priority**: HIGH/MEDIUM/LOW

**Podcast Categories to Target**:
- Local/Regional: Essex business podcasts, entrepreneur shows, community podcasts
- Industry/Trade: Small business podcasts, skilled worker shows, trade-specific shows
- Niche-Relevant: [Industry-specific podcasts based on business type]

### Podcast 2: [Podcast Name]
[Continue for 10-20 podcasts...]

---

## 3. YouTube Collaboration Targets (10-15 channels)

### Channel 1: [Channel Name]
- **URL**: [YouTube channel]
- **Subscribers**: [Count]
- **Content Type**: [Car reviews, DIY, local vlogs, business advice]
- **Average Views**: [Typical view count]
- **Collaboration Ideas**:
  1. "[Video idea 1 - e.g., 'What Happens When You Lose Your Keys - Following a Real Emergency Callout']"
  2. "[Video idea 2 - e.g., 'Testing Car Security - Can a Locksmith Really Open Any Car?']"
  3. "[Video idea 3 - e.g., 'Day in the Life: Emergency Locksmith in Essex']"
- **Value for Creator**: [Unique content, problem-solving, local angle]
- **Link Opportunity**: Video description link
- **Contact**: [Business email from About section]
- **Priority**: HIGH/MEDIUM/LOW

**YouTube Channel Categories**:
- Local Content Creators: [Area] vloggers, community channels
- Industry-Specific: [Automotive, home security, etc. based on business]
- Business/Entrepreneurship: Small business stories, trade skills channels
- Problem-Solving: Life hacks, emergency preparedness, advice channels

### Channel 2: [Channel Name]
[Continue for 10-15 channels...]

---

## 4. Digital PR Story Angles (10-15 angles)

### Story Angle 1: [Compelling Headline]
- **Hook**: [Data/trend/survey that makes this newsworthy]
- **Example Headline**: "[Attention-grabbing headline for journalists]"
- **Data/Statistics**: [Key data supporting story]
- **Target Publications**:
  - Local: [Area newspapers, community sites]
  - Industry: [Trade publications]
  - National: [If broader appeal]
- **Best Timing**: [When to pitch - seasonal, news cycle, events]
- **Link Opportunity**: [Page story would link to]
- **Priority**: HIGH/MEDIUM

**Example** (Locksmith Business):
- **Hook**: "Car Key Replacement Costs Up 40% in 2026 - Dealerships vs Locksmiths Data"
- **Headline**: "Essex Drivers Paying £450 for Keys Dealerships Charge £180 For - New Data"
- **Data**: Analysis of 500 key replacement jobs showing price differences
- **Target**: Essex Chronicle, AutoExpress, MoneySavingExpert, Which?
- **Timing**: January (budgeting season) or post-Christmas (car theft spike)
- **Link**: /dealership-vs-locksmith-car-keys/
- **Priority**: HIGH

### Story Angle 2: [Headline]
[Continue for 10-15 angles...]

---

## 5. Guest Posting Targets (15-25 blogs/sites)

### Target 1: [Blog/Website Name]
- **URL**: [Website]
- **DR**: [Rating]
- **Niche**: [Category]
- **Audience Size**: [Traffic/subscribers estimate]
- **Content Types**: [Guides, how-tos, case studies, listicles]
- **Suggested Topics** (3 pitch ideas):
  1. "[Topic matching their content + your expertise]"
  2. "[Topic 2]"
  3. "[Topic 3]"
- **Contact**: [Email or submission form]
- **Previous Guest Posts**: Yes/No
- **Difficulty**: LOW/MEDIUM/HIGH
- **Priority**: HIGH/MEDIUM

### Target 2: [Blog Name]
[Continue for 15-25 targets...]

---

## 6. Resource Page Targets (10-20 sites)

### Target 1: [Website Name]
- **URL**: [Specific resource page URL]
- **DR**: [Rating]
- **Page Title**: "[Page title]"
- **Why They'll Link**: [Relevance, local focus, comprehensive list]
- **Outreach Angle**: "Your resource lists 15 [businesses] but missing [your business]. We've been serving [area] for [X] years with [rating]..."
- **Contact**: [Email or form]
- **Difficulty**: LOW/MEDIUM/HIGH
- **Priority**: HIGH/MEDIUM

### Target 2: [Website Name]
[Continue for 10-20 targets...]

---

## 7. Outreach Email Templates (8 Templates)

### Template #1: Guest Post Pitch
**Subject**: Guest post idea: [Specific Topic] for [Their Website]

Hi [Name],

I've been following [Website] — particularly enjoyed your post on [specific article].

I'm [Your Name], [role] at [Business] in [Location]. I've been working in [industry] for [X] years and have helped [specific achievement].

I'd love to contribute a guest post. I'm thinking:

**"[Specific Article Title]"**

This would cover:
- [Key point 1 - value for their audience]
- [Key point 2]
- [Key point 3]

Would this be a good fit for your readers?

Best,
[Your Name]

---

### Template #5: Podcast Guest Pitch
**Subject**: Guest idea for [Podcast Name]

Hi [Host Name],

I've been listening to [Podcast] — loved your episode with [guest] on [topic].

I'm [Your Name], [role] at [Business]. I think I'd be great for your show because [specific reason].

**Potential episode topics**:
1. **"[Episode Title]"** - [What you'd cover]
2. **"[Episode Title 2]"** - [What you'd cover]

**What makes my story interesting**:
- [Unique angle 1]
- [Unique angle 2]
- [Unique angle 3]

Would this be a good fit?

Best,
[Your Name]

---

### Template #6: YouTube Collaboration Pitch
**Subject**: Video collaboration idea for [Channel Name]

Hi [Creator Name],

Big fan of [Channel] — subscribed since [timeframe].

I'm [Your Name], a [role] in [Location]. I have a video idea your audience would find interesting:

**"[Video Concept]"**

The idea: [3-4 sentence description]

**Why your audience would love it**:
- [Reason 1 - entertainment, problem-solving, unique angle]
- [Reason 2]

**What I'd provide**:
- [Access, expertise, behind-the-scenes, footage]
- [Promotion to my audience - X followers]

No fees — just think it'd make great content.

What do you think?

Best,
[Your Name]

---

[Continue for all 8 templates: Guest Post, Resource Page, Broken Link, Digital PR, Podcast, YouTube, HARO, Direct Journalist]

---

## 8. 30/60/90 Day Link Building Timeline

### Month 1: Foundation & Low-Hanging Fruit (Days 1-30)

**Week 1: Setup & Easy Wins**
- [ ] Submit to 5-10 industry directories (2-3 hours)
- [ ] Set up HARO/ResponseSource accounts (30 mins)
- [ ] Identify 20 resource page targets (2 hours)
- **Target**: 5-8 links acquired

**Week 2: Resource Page Outreach**
- [ ] Email 10 resource page targets (2 hours)
- [ ] Respond to 2-3 HARO queries (1 hour)
- [ ] Identify 15 broken link opportunities (2 hours)
- **Target**: 2-3 resource links confirmed

**Week 3: Broken Link Building**
- [ ] Email 10 broken link targets (2 hours)
- [ ] Follow up on Week 2 outreach (30 mins)
- [ ] Identify 20 guest posting targets (2 hours)
- **Target**: 2-3 broken links replaced

**Week 4: Guest Post Pitching**
- [ ] Pitch 10 guest post opportunities (3 hours)
- [ ] Respond to 2-3 HARO queries (1 hour)
- **Target**: 2-3 guest posts accepted

**Month 1 Target**: 12-17 links

---

### Month 2: Content & Outreach Scale (Days 31-60)

**Week 5: Podcast Outreach**
- [ ] Identify 15 podcast targets (2 hours)
- [ ] Pitch 5 podcasts (2 hours)
- [ ] Write 1st guest post (3-4 hours)
- **Target**: 1-2 podcast appearances booked

**Week 6: YouTube Collaboration**
- [ ] Identify 10 YouTube channels (2 hours)
- [ ] Pitch 5 channels (2 hours)
- [ ] Follow up on podcast pitches (30 mins)
- **Target**: 1 YouTube collaboration confirmed

**Week 7: Digital PR Campaign**
- [ ] Choose 1 story angle (30 mins)
- [ ] Create data/assets (3-4 hours)
- [ ] Pitch 15 journalists (2 hours)
- **Target**: 1-2 journalists interested

**Week 8: Consolidation**
- [ ] Follow up on all Month 2 outreach (2 hours)
- [ ] Record 1st podcast (1 hour)
- [ ] Finish guest posts (3-4 hours)
- **Target**: 3-5 guest posts published, 1 podcast live

**Month 2 Target**: 8-12 links

---

### Month 3: Amplification (Days 61-90)

**Week 9: Second PR Campaign**
- [ ] Launch 2nd story angle (4 hours)
- [ ] Record 2nd podcast (1 hour)
- [ ] Film YouTube collaboration (2-3 hours)
- **Target**: 2-3 media mentions

**Week 10: Relationship Nurturing**
- [ ] Follow up with journalists (1 hour)
- [ ] Connect with hosts on LinkedIn (30 mins)
- [ ] Thank resource page owners (30 mins)
- **Target**: Build relationships for future links

**Week 11-12: Scale What's Working**
- [ ] Double down on best-performing tactic (4 hours)
- [ ] Continue HARO responses (1 hour/week)
- [ ] Plan Month 4-6 strategy (2 hours)
- **Target**: 5-8 additional links

**Month 3 Target**: 10-14 links

---

## 90-Day Summary

**Total Target**: 30-43 high-quality backlinks
**Time Investment**: ~120 hours over 90 days (10-12 hours/week)
**Resource Options**:
- DIY: 10-12 hours/week (business owner or team member)
- Hire VA: 5-8 hours/week @ £15-25/hour = £300-800/month
- Link Building Agency: £1,000-2,500/month for 30-40 links

---

## Tracking Framework

**Weekly Metrics** (Track in Ahrefs):
- Total referring domains (target: +1-2/week)
- Domain Rating (target: +1 point every 2 months)
- Total backlinks acquired

**Monthly ROI by Tactic**:
- Guest posts: [X] hours → [Y] links = [Z] hours per link
- Podcasts: [X] hours → [Y] links + brand exposure
- Digital PR: [X] hours → [Y] links + media mentions

**Scale what works, drop what doesn't.**
```

**Quality Gate**:
- [ ] 50-100 specific link targets identified across all tactics
- [ ] 8 outreach templates provided (ready to copy-paste)
- [ ] 10-20 podcast targets with pitch angles
- [ ] 10-15 YouTube channels with collaboration ideas
- [ ] 10-15 digital PR story angles
- [ ] 30/60/90 timeline with weekly tasks and targets
- [ ] Tracking framework with metrics
- [ ] All tactics matched to risk tolerance (conservative = directories + guest posts, aggressive = PR + broken links)

**Integration with Other Stages**:
- **Feeds from Stage 3**: Competitor backlink gaps inform targets
- **Feeds from Stage 3.5**: Pages needing link authority prioritized
- **Feeds into Stage 8**: Link building tasks integrated into implementation plan

**See Full Enhancement**: `/AGENT_ENHANCEMENTS/stage_7.5_link_building_strategy.md` for complete framework with all templates and tactics

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
