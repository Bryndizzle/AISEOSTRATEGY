# Agent Enhancement: Full Page Draft Generator

**Enhancement Type**: Auto-Generation Capability
**Integration Stage**: Stage 5 (Implementation Planning) + Stage 6 (Content Specifications)
**Purpose**: Automatically generate complete, publication-ready page drafts for critical and high-priority pages
**Status**: ✅ Active Enhancement
**Created**: 19 January 2026

---

## Problem This Solves

**Current State**: Agent recommends pages in Stage 3.5 and provides content specifications in Stage 6, but doesn't create full page drafts.

**Gap**: Business owners and content writers need complete page examples showing:
- Full H1/H2 structure pulled from customer insights
- Internal linking with specific anchor text and target URLs
- FAQ sections with schema-ready markup
- Comparison tables
- Complete content (not just specifications)

**Solution**: Automatically generate 3-5 complete page drafts for CRITICAL pages (high impact + high priority) as part of the strategy deliverables.

---

## When to Auto-Generate Full Page Drafts

**Trigger Conditions** (agent should automatically create drafts when):

1. **Page is marked as CRITICAL PRIORITY** in Stage 3.5 Page Backlog
   - Impact: HIGH or CRITICAL
   - Priority: 1-5 in the Page Backlog
   - Effort: LOW or MEDIUM (quick wins)

2. **Page targets "The Big One" keyword** from Stage 2.5
   - The single highest-impact keyword opportunity
   - Example: "Spare Keys for Car" (36,200 monthly searches, position #5)

3. **Page closes major customer objection** from Reddit research
   - Decision-making page (e.g., "Dealer vs Locksmith")
   - Cost transparency page
   - Quality/trust page ("Are locksmith keys as good as dealer?")

4. **Page has clear customer insights available** from Stage 1
   - Reddit quotes showing pain points
   - Specific objections to address
   - Customer language to incorporate

**Recommended Quantity**: 3-5 full page drafts per strategy run
- At minimum: Draft "The Big One" page
- Ideally: Draft top 3-5 priority pages from Page Backlog

---

## What to Include in Full Page Drafts

Each full page draft must include:

### 1. **Complete SEO Package**
```markdown
**Target Keywords**:
- Primary: [keyword] ([volume] searches/month)
- Secondary: [keyword 2], [keyword 3], [keyword 4]

**Title Tag** (50-60 characters):
[Title optimized for primary keyword]

**Meta Description** (150-160 characters):
[Compelling description with soft CTA]

**URL Slug**: /[slug-from-stage-3.5]/
```

### 2. **Full Content with Customer Insight Headers**

**H1**: [Primary keyword + benefit, pulling from customer pain points]
- Example: "Spare Car Keys Essex: Get a £99 Spare Before It's a £400 Emergency"

**Introduction** (150-200 words):
- Direct answer to primary query (40-60 words for AI citation)
- Address main pain point from Reddit research
- Include primary keyword in first 100 words
- Soft CTA

**H2 Structure** (5-8 H2s):
Pull H2s from customer insights, NOT generic SEO headers.

❌ Generic: "Our Services", "Why Choose Us", "Contact Us"
✅ Customer Insight-Led:
- "Why You Need A Spare Car Key (Before It's Too Late)"
- "How Much Does a Spare Car Key Cost? (Locksmith vs Dealer)"
- "What Happens If You Lose Your Only Car Key?"
- "Can Locksmiths Program Transponder Keys?"

**Body Content** (2,000-2,500 words for service pages, 1,500-2,000 for location pages):
- Use customer language from Reddit quotes
- Address objections directly
- Include specific examples and scenarios
- No filler, every paragraph adds value

### 3. **Internal Linking** (3-5 links minimum)

**Format**:
```markdown
**Related Services (Internal Links)**:
- Link to: /[target-page-slug]/
  Anchor: "[Keyword-rich anchor text]"
  Context: [Where in content to place link]

- Link to: /[target-page-slug]/
  Anchor: "[Keyword-rich anchor text]"
  Context: [Where in content to place link]

[Continue for 3-5 links]
```

**Guidelines**:
- Link to related service pages
- Link to comparison pages when mentioning alternatives
- Link to location pages when mentioning areas
- Link to make/model pages when mentioning vehicles
- Use natural, keyword-rich anchor text (not "click here")

### 4. **FAQ Section** (5-15 questions)

**Format**:
```markdown
## Frequently Asked Questions

### [Question 1 in customer language]?
[Direct answer, 40-80 words, schema-ready]

### [Question 2]?
[Direct answer]

[Continue for 5-15 FAQs]
```

**FAQ Selection Criteria**:
- Pull questions from Reddit threads (actual customer questions)
- Include decision-making questions ("Should I...", "Is it worth...")
- Include cost questions ("How much...", "What does it cost...")
- Include objection-handling questions ("Can locksmiths really...", "Are they as good as...")
- Include process questions ("What happens if...", "How long does...")

### 5. **Comparison Table** (if applicable)

Include if page covers:
- Service comparison (locksmith vs dealer)
- Cost comparison (spare key vs lost key emergency)
- Make/model comparison (BMW vs VW vs Ford pricing)
- Location comparison (response times by area)

**Format**:
```markdown
| Factor | Locksmith | Dealership |
|--------|-----------|------------|
| Cost | £99-£150 | £180-£280 |
| Time | 30-45 mins | 3-7 days |
| Mobile Service | ✅ Yes | ❌ No |
| Warranty | 12 months | 12 months |
```

### 6. **Schema Markup Recommendations**

```markdown
**Recommended Schema**:
- Service schema (for service pages)
- LocalBusiness schema (for location pages)
- FAQPage schema (for FAQ section)
- HowTo schema (if step-by-step process included)
- Product schema (if pricing specific products)

**Schema Implementation Notes**:
[Provide JSON-LD examples or note where developer should implement]
```

### 7. **Content Completion Checklist**

**MANDATORY**: At end of every draft, include checklist of placeholders/assumptions:

```markdown
---

## Content Completion Checklist

Before publishing, review and complete the following:

**Pricing Information**:
- [ ] Line [X]: [Specific placeholder/assumption to verify]
- [ ] Line [X]: [Specific placeholder/assumption to verify]

**Testimonials**:
- [ ] Line [X]: [Specific placeholder/assumption to verify]

**Business Details**:
- [ ] Line [X]: [Specific placeholder/assumption to verify]

**Assumptions to Verify**:
- [ ] Line [X]: [Specific assumption with source cited]

**Total Placeholders**: [count]
**Total Assumptions**: [count]
```

---

## Execution Process for Agent

When auto-generating full page drafts, follow this sequence:

### Step 1: Select Pages to Draft (Automatic)

From Stage 3.5 Page Backlog, identify:
1. "The Big One" page (from Stage 2.5) - ALWAYS draft this
2. Pages with Priority 1-3 that have:
   - Impact: HIGH or CRITICAL
   - Effort: LOW or MEDIUM
   - Clear customer insights available
3. Pages that close major objections

**Output**: "I will draft [X] complete pages: [list page names and reasons]"

### Step 2: Gather Inputs (From Previous Stages)

For each page to draft, collect:
- **From Stage 1**: Customer pain points, Reddit quotes, objections, scenarios
- **From Stage 2.5**: Primary and secondary keywords, search volume, current position
- **From Stage 3.5**: URL slug, page type, target intent, AI visibility tactics
- **From Stage 6** (if exists): Content specifications, word count, structure requirements

### Step 3: Draft Complete Page

Follow this template structure:

```markdown
# [Page Name] - FULL PAGE DRAFT

**Page Type**: [Service/Location/Comparison/Guide]
**Priority**: [from Stage 3.5]
**Target Keywords**: [from Stage 2.5]
**Word Count**: [actual count]

---

## SEO Package

**Title Tag** (50-60 characters):
[Title]

**Meta Description** (150-160 characters):
[Description]

**URL Slug**: /[slug]/

**Primary Keyword**: [keyword] ([volume]/month, position #[X])
**Secondary Keywords**: [list]

---

## Full Page Content

### [H1: Primary keyword + customer benefit]

[Introduction: 150-200 words]
- Direct answer in first 40-60 words
- Primary keyword in first 100 words
- Address main pain point
- Soft CTA

---

### [H2: Customer insight-driven header]

[Content: 250-400 words]
- Address specific pain point
- Use customer language
- Include examples/scenarios
- [INTERNAL LINK: anchor text → /target-page/]

---

### [H2: Customer insight-driven header]

[Content: 250-400 words]

[Continue for 5-8 H2 sections...]

---

## [Comparison Table Title]

| [Column 1] | [Column 2] | [Column 3] |
|------------|------------|------------|
| [Data]     | [Data]     | [Data]     |

---

## Frequently Asked Questions

### [Question 1 in customer language]?
[Direct answer, 40-80 words]

### [Question 2]?
[Direct answer]

[Continue for 5-15 FAQs...]

---

## Call to Action

[Strong CTA with outcome focus]
[Phone number or contact method]
[Operating hours / response time]

---

## Related Services (Internal Links)

- Link to: /[target-page]/
  Anchor: "[Keyword-rich anchor text]"
  Context: [Where to place in content]

[Continue for 3-5 links]

---

## Schema Markup Recommendations

**Recommended Schema Types**:
- [Schema type 1]
- [Schema type 2]
- [Schema type 3]

**Implementation Notes**:
[Guidance for developer]

---

## Content Completion Checklist

Before publishing, complete the following:

**Placeholders**:
- [ ] Line [X]: [Specific item to verify/add]

**Assumptions**:
- [ ] Line [X]: [Assumption with source - verify]

**Total Placeholders**: [count]
**Total Assumptions**: [count]
```

### Step 4: Self-Review (Quality Control)

Before outputting draft, verify:
- [ ] Primary keyword appears in H1, first 100 words, 1-2 H2s
- [ ] H2s are customer insight-driven (not generic)
- [ ] 3-5 internal links with specific anchor text and target URLs
- [ ] 5+ FAQ questions with direct answers
- [ ] At least one comparison table (if applicable)
- [ ] Zero filler sentences (every paragraph adds value)
- [ ] Customer language used (Reddit quotes where relevant)
- [ ] All placeholders use standardized format: **[PLACEHOLDER: CATEGORY - instruction]**
- [ ] All assumptions flagged: [ASSUMPTION: detail - source year]
- [ ] Content Completion Checklist included at end with accurate counts

### Step 5: Output Draft

Output each draft as a separate markdown file:

**File Structure**:
```
speedy_keys_fresh_strategy/
└── FULL_PAGE_DRAFTS/
    ├── 01_[page-name]_DRAFT.md
    ├── 02_[page-name]_DRAFT.md
    ├── 03_[page-name]_DRAFT.md
    └── [continue...]
```

**Naming Convention**:
- `01_` = Priority order (matches Stage 3.5 Page Backlog priority)
- `[page-name]` = Descriptive name matching page recommendation
- `_DRAFT.md` = Clearly marks as draft content

---

## Integration with Workflow Stages

### **Stage 3.5: Page-Level Recommendations**
- Identify which pages should get full drafts
- Flag them: "🎯 FULL DRAFT WILL BE PROVIDED"

### **Stage 6: Content Specifications**
- For pages WITHOUT full drafts, provide specifications only
- For pages WITH full drafts, reference: "See FULL_PAGE_DRAFTS/01_[name]_DRAFT.md for complete page"

### **Stage 7: Implementation Tasks**
- Include task: "Review and publish draft pages from FULL_PAGE_DRAFTS/ folder"
- Specify which placeholders need completing before publish

---

## Quality Standards

Every full page draft must meet these standards:

### Content Quality
- ✅ 2,000-2,500 words for service pages, 1,500-2,000 for location pages
- ✅ Customer insight-driven H2s (not generic)
- ✅ Direct answer in first 40-60 words (AI citation optimization)
- ✅ No filler - every paragraph adds new information
- ✅ Customer language from Reddit research incorporated naturally

### SEO Optimization
- ✅ Primary keyword in H1, first 100 words, 1-2 H2s
- ✅ 2-4 secondary keywords naturally incorporated
- ✅ Title tag and meta description optimized
- ✅ 3-5 internal links with keyword-rich anchor text
- ✅ FAQ section with 5-15 questions

### AI Visibility
- ✅ Opening answer (40-60 words) directly addresses primary query
- ✅ Question-format H2s ("Can locksmiths..." not "Locksmith Capabilities")
- ✅ At least one comparison table with specific data
- ✅ Schema recommendations provided

### Accuracy & Transparency
- ✅ All missing pricing uses **[PLACEHOLDER: PRICING - instruction]**
- ✅ All testimonials use **[PLACEHOLDER: TESTIMONIAL - instruction]**
- ✅ All assumptions flagged: [ASSUMPTION: detail - source year]
- ✅ Content Completion Checklist included with accurate counts
- ✅ No silent guessing - everything verifiable or flagged

---

## Example Output (Reference)

See: `/speedy_keys_fresh_strategy/FULL_PAGE_DRAFTS/01_spare_keys_page_DRAFT.md`

This exemplar shows:
- Complete 2,547-word page draft
- Customer insight-driven H2s: "Why You Need A Spare Car Key (Before It's Too Late)"
- 11 internal links with specific anchor text
- 15 FAQ questions with schema-ready answers
- Comparison table (Locksmith vs Dealer)
- Service + FAQ schema recommendations
- Content Completion Checklist with 1 placeholder and 1 assumption

**This is the gold standard for all full page drafts.**

---

## Execution Checklist for Agent

When user requests a full AISEO strategy, after completing Stage 3.5:

- [ ] **Identify 3-5 pages for full drafts** (The Big One + top priority pages)
- [ ] **Announce which pages will get full drafts**: "I will create complete page drafts for: [list]"
- [ ] **Gather inputs** from Stages 1, 2.5, and 3.5 for each page
- [ ] **Draft each page** following the template structure above
- [ ] **Run self-review checklist** on each draft before output
- [ ] **Create separate files** in FULL_PAGE_DRAFTS/ folder with priority numbering
- [ ] **Reference drafts** in Stage 6 and Stage 7 deliverables
- [ ] **Include in final deliverable summary**: "✅ [X] complete page drafts provided in FULL_PAGE_DRAFTS/ folder"

---

## Benefits of This Enhancement

**For Business Owners**:
- See exactly what final pages will look like (no guesswork)
- Clear what needs completing (placeholders/assumptions flagged)
- Can implement immediately (copy-paste ready, minus placeholders)

**For Content Writers**:
- Complete template showing structure, headers, internal links
- Customer language examples throughout
- FAQ questions already written in customer voice

**For SEO Implementation**:
- All technical elements specified (schema, title tags, meta descriptions)
- Internal linking structure mapped out
- Keyword optimization already done

**For Project Success**:
- Faster implementation (drafts vs specifications)
- Higher quality output (example-driven)
- Reduced back-and-forth (fewer questions about "what should this look like?")

---

**END OF ENHANCEMENT: FULL PAGE DRAFT GENERATOR**
