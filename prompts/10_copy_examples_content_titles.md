# Prompt 10: Copy Examples & Content Titles Generator

## Purpose
Generate ready-to-implement copy examples and a comprehensive content titles list (50-100 topics) organized by keyword clusters, journey stages, and the 4-layer growth model. All copy must be specific, actionable, and aligned with customer jobs and search intent.

## Inputs Required
- Keyword strategy (from Prompt 9)
- JTBD framework (from Prompt 9)
- Business fundamentals (from Prompt 1)
- Reddit verbatim language (from Prompt 7)
- Brand voice/tone (from Intake Section 9)
- Content gaps (from Prompt 6)
- Strategy framework (from Prompt 8)

## Output Requirements

### 1. Page Titles & Meta Descriptions (15-25 examples)

For priority pages identified in strategy:

#### Homepage
**Title** (50-60 characters): [Exact title with primary keyword]
**Meta Description** (150-160 characters): [Compelling description with CTA]
**H1**: [Primary heading]
**Rationale**: Targets "[keyword]", addresses JTBD "[job]", optimized for CTR

#### Service Pages (5-10 pages)
**Page**: [Service name]
**URL**: /[slug]
**Title**: [Exact title]
**Meta Description**: [Exact description]
**H1**: [Primary heading]
**H2s** (4-6): [List of subheadings]
**Target Keywords**: [Primary], [Secondary 1], [Secondary 2]
**Search Intent**: [Transactional/Commercial]

#### Location Pages (if local business)
**Page**: [Service + Location]
**URL**: /[service]-[location]
**Title**: [Service] [Location] | [USP] | [Brand]
**Meta Description**: [Benefits + social proof + CTA + location]
**Schema**: LocalBusiness + Service

### 2. FAQ Examples (50+ Questions & Answers)

Organized by:
- **Layer/Intent**: Foundation, High-Intent, Authority, Awareness
- **Keyword Cluster**: Which topic cluster does this support?
- **Schema Ready**: Yes/No (can this go in FAQ schema?)

#### Format:
**Q: [Exact question using customer verbatim language]**
**A: [2-4 sentence answer, include target keyword naturally]**
**Target Keyword**: [keyword]
**Search Volume**: [monthly]
**Layer**: [1-4]
**Schema Ready**: Yes
**Where to Use**: [Service page X, Blog post Y, Homepage]

#### Example Categories:
- **Pricing FAQs** (8-12): "How much does X cost?", "Do you offer payment plans?"
- **Process FAQs** (8-12): "How long does X take?", "What's involved in Y?"
- **Qualification FAQs** (5-8): "Do I need X?", "Is this right for my situation?"
- **Trust FAQs** (5-8): "Are you licensed?", "What guarantees do you offer?"
- **Comparison FAQs** (5-8): "X vs Y - what's the difference?"
- **Objection-Handling FAQs** (8-12): Address specific objections from intake/Reddit

### 3. Content Titles List (50-100 Blog Topics)

Organized by:
1. **Keyword Cluster**
2. **4-Layer Model**
3. **Journey Stage**
4. **Content Format**
5. **Priority** (1-5)

#### Format:
**Title**: [Exact blog post title, SEO optimized]
**Slug**: /blog/[url-slug]
**Primary Keyword**: [keyword]
**Secondary Keywords**: [2-3 keywords]
**Search Volume**: [monthly]
**Intent**: Info/Commercial/Transactional
**Layer**: Foundation/High-Intent/Authority/Awareness
**Journey Stage**: Awareness/Consideration/Decision
**Content Format**: How-to guide, Listicle, Case study, Comparison, Ultimate guide
**Word Count**: [1500-3000]
**Priority**: 1-5 (1 = highest)
**Rationale**: [Why this topic matters - addresses which customer job/pain point]

#### Example Structure (50-100 topics):

**Layer 1 - Foundation** (10-15 topics):
1. **Title**: "What is [Core Service]? A Complete Guide for [Location]"
   - Primary Keyword: "what is [service]"
   - Intent: Informational
   - Priority: 2

**Layer 2 - High-Intent** (15-20 topics):
1. **Title**: "Best [Service] in [Location]: 2026 Buyer's Guide"
   - Primary Keyword: "best [service] [location]"
   - Intent: Commercial
   - Priority: 1

**Layer 3 - Authority** (15-20 topics):
1. **Title**: "The Future of [Industry]: [Expert Take on Trend]"
   - Primary Keyword: "[trend] [industry]"
   - Intent: Informational
   - Priority: 3

**Layer 4 - Awareness** (10-15 topics):
1. **Title**: "7 Signs You Need [Solution] (And What to Do Next)"
   - Primary Keyword: "signs you need [solution]"
   - Intent: Informational
   - Priority: 4

### 4. Social Media Post Templates (10-15 examples)

**LinkedIn Posts** (5-7):
- **Hook**: [Attention-grabbing first line]
- **Body**: [3-4 lines with insight/story]
- **CTA**: [Clear next step]
- **Content Angle**: [What makes this interesting]
- **Supports**: [Which blog post/service page]

**Twitter/X Threads** (3-5):
- **Tweet 1 (Hook)**: [Compelling opening]
- **Tweet 2-4 (Value)**: [Key points]
- **Tweet 5 (CTA)**: [Link to content]

### 5. Email Subject Lines (15-20 examples)

Organized by campaign type:
- **Newsletter** (5): "[Specific value proposition]"
- **Nurture Sequence** (5): Day 1-5 subjects
- **Promotional** (5): "[Offer] + [Urgency]"

### 6. Page Introduction Examples (8-12)

For key landing pages, provide first 100-150 words:

**Page**: [Service Page Name]
**Introduction**:
```
[First paragraph that:
- Addresses customer job/pain point
- Includes primary keyword naturally
- Establishes E-E-A-T (Experience, Expertise)
- Sets up page structure
- Uses verbatim customer language from Reddit]
```
**Keywords Targeted**: [List]
**JTBD Addressed**: [Which customer job]

### 7. Call-to-Action Variations (10-15 examples)

For different contexts:
- **High-intent pages**: "[Action-oriented CTA]"
- **Informational content**: "[Soft CTA]"
- **Retargeting**: "[Urgency-based CTA]"
- **Local**: "[Location-specific CTA]"

### 8. Schema Markup Copy

**FAQPage Schema** - Ready-to-implement:
```json
{
  "@context": "https://schema.org",
  "@type": "FAQPage",
  "mainEntity": [{
    "@type": "Question",
    "name": "[FAQ question 1]",
    "acceptedAnswer": {
      "@type": "Answer",
      "text": "[FAQ answer 1]"
    }
  }]
}
```

Provide 10-15 FAQ Q&A pairs ready for schema implementation.

**LocalBusiness Schema** (if local):
Include specific business details with rich snippets opportunities.

**Service Schema**:
For each priority service page.

## Organization & Delivery

### Master Content Titles Spreadsheet
Columns:
- Title
- URL Slug
- Primary Keyword
- Secondary Keywords (2-3)
- Search Volume
- Keyword Difficulty
- Search Intent
- Layer (1-4)
- Journey Stage
- Content Format
- Word Count Target
- Priority (1-5)
- Supporting FAQs (reference FAQ numbers)
- Internal Link Targets (which pages to link to)
- External Link Opportunities
- Schema Markup Needed
- Rationale (why this topic)

### Copy Examples Document Structure
```
## 1. Page Titles & Meta Descriptions
   1.1 Homepage
   1.2 Service Pages
   1.3 Location Pages
   1.4 About/Team Pages

## 2. FAQs (Organized by Layer)
   2.1 Layer 1 - Foundation (15-20 FAQs)
   2.2 Layer 2 - High-Intent (15-20 FAQs)
   2.3 Layer 3 - Authority (10-15 FAQs)
   2.4 Layer 4 - Awareness (10-15 FAQs)

## 3. Blog Post Titles (50-100)
   [Organized by layer, with full metadata]

## 4. Social Media Templates
   4.1 LinkedIn
   4.2 Twitter/X
   4.3 Facebook (if relevant)

## 5. Email Subject Lines
   5.1 Newsletter
   5.2 Nurture
   5.3 Promotional

## 6. Page Introductions
   [Full copy for 8-12 priority pages]

## 7. CTAs
   [15 variations for different contexts]

## 8. Schema Markup
   [Ready-to-implement JSON-LD]
```

## Quality Standards

All copy must be:
- **Specific**: No generic phrases like "industry-leading" or "cutting-edge"
- **Customer Language**: Use verbatim phrases from Reddit research
- **SEO Optimized**: Include target keywords naturally
- **Action-Oriented**: Clear next steps
- **Brand-Aligned**: Match tone from intake form
- **UK English**: Optimise, organisation, colour, etc.
- **Schema-Ready**: Where applicable, format for structured data
- **E-E-A-T Signals**: Include experience, expertise, authoritativeness, trust markers

## Success Criteria

This prompt is complete when you have:
- [x] 15-25 page title & meta description examples
- [x] 50+ FAQ questions with answers, organized by layer
- [x] 50-100 blog post titles with full metadata (keyword, intent, priority)
- [x] 10-15 social media post templates
- [x] 15-20 email subject lines
- [x] 8-12 page introduction copy examples
- [x] 10-15 CTA variations
- [x] Schema markup ready to implement (FAQ, Local, Service)
- [x] All copy uses customer verbatim language from Reddit
- [x] All copy targets specific keywords from Prompt 9
- [x] All copy addresses specific JTBD from Prompt 9
- [x] Master spreadsheet with 50-100 content titles fully populated

## Assumptions to Label

- [ASSUMPTION: Brand voice is professional but conversational based on intake, adjust if specific tone guidelines provided]
- [ASSUMPTION: Word counts based on competitor analysis - adjust if specific requirements]
- [ASSUMPTION: UK English unless intake specifies different geography]
- [ASSUMPTION: Schema markup follows latest schema.org guidelines as of 2026]
- [ASSUMPTION: If local business, prioritize location-based copy; if B2B, prioritize expertise/authority]

## Integration Points

- **Feed into Prompt 12**: Use copy examples for page-level action mapping
- **Support Prompt 8**: Ensure copy aligns with strategy document framework
- **Validate with Prompt 11**: QA checks that copy addresses business challenge
- **Cross-reference Prompt 9**: Every piece of copy targets specific keyword cluster and JTBD

## Content Title Categories to Cover

Ensure 50-100 titles span:
- **How-to Guides** (15-20): Practical, actionable
- **Listicles** (10-15): "X Ways to...", "Top X..."
- **Ultimate Guides** (5-8): Comprehensive pillar content
- **Comparisons** (8-12): "X vs Y", "Best X for Y"
- **Case Studies** (5-8): Real examples, results
- **Industry Insights** (8-12): Trends, predictions, expert takes
- **Problem-Solution** (8-12): "How to Fix X", "Solutions for Y"
- **Local Content** (5-10): Location-specific if applicable
- **FAQ-Style** (5-8): "What is...", "Why does..."
- **Seasonal/Timely** (3-5): "2026 Guide to...", "New Changes to..."
