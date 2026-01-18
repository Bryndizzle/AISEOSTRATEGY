# Conditional Prompt: CRO & Conversion Funnel Analysis

## When to Run This Prompt
This is a **conditional prompt** - only execute if:
- Primary goal includes "leads", "revenue", "conversions", or "sales" (from Intake Section 1)
- OR business model is B2B with stated deal size (from Intake Section 2)
- OR business model is e-commerce
- OR user explicitly requests conversion optimization

**Skip this prompt if**:
- Goal is purely "SEO visibility" or "AI visibility authority" without commercial objective
- Business is purely informational (publishing, media) with no conversion funnel

---

## Purpose
Analyze the complete conversion funnel from traffic acquisition to conversion, identify friction points, and provide specific CRO (Conversion Rate Optimization) recommendations integrated with the SEO strategy.

## Inputs Required
- Website URL (from Intake Section 1)
- Business model and sales cycle (from Intake Section 2)
- Primary goal (from Intake Section 1)
- Average deal size (from Intake Section 2)
- Traffic & analytics data (from Prompt 5)
- Customer pain points and objections (from Prompt 7 - Reddit research)
- Existing content and messaging (from site audit)

## Conversion Funnel Framework

### 5-Stage Funnel Analysis

#### Stage 1: Traffic Acquisition
**Current State**:
- Traffic sources: Organic, Direct, Referral, Social, Paid (from Prompt 5)
- Traffic volume by source
- Traffic quality (bounce rate, time on site by source)

**Analysis**:
- Which traffic sources convert best?
- Are we attracting the right audience (match with ICP from Intake Section 3)?
- Traffic intent alignment (informational vs commercial vs transactional)

**Optimization Opportunities**:
- [List specific recommendations]

---

#### Stage 2: Landing & Engagement
**Current State**:
- Top landing pages (from Prompt 5)
- Average time on page
- Bounce rate per landing page
- Scroll depth (if available)

**Friction Points**:
- [ ] Slow page load (>3 seconds)
- [ ] Unclear value proposition
- [ ] Poor mobile experience
- [ ] Mismatch between search intent and page content
- [ ] Weak or missing headline
- [ ] No clear next step
- [ ] Trust signals missing (reviews, certifications, social proof)

**Optimization Opportunities**:
1. **Above-the-fold optimization**:
   - Headline: "[Specific recommendation]"
   - Subheadline: "[Specific recommendation]"
   - Hero image/video: [Specification]
   - Primary CTA: "[Exact copy and placement]"

2. **Trust signals**:
   - Add: [Reviews, certifications, client logos, case study stats]
   - Placement: [Specific location]

3. **Value proposition clarity**:
   - Current: [What it says now]
   - Improved: "[Clearer statement addressing customer job from Prompt 9]"

---

#### Stage 3: Consideration & Education
**Current State**:
- Pages visited per session
- Navigation patterns (most common paths)
- Content engagement (which pages hold attention)
- Resources accessed (downloads, videos watched)

**Customer Questions to Answer** (from Prompt 7 - Reddit):
- [List verbatim customer questions/objections from Reddit research]
- Are these addressed on the website?
- Where are they addressed?
- How clearly are they addressed?

**Friction Points**:
- [ ] Missing key information (pricing, process, timeline)
- [ ] Objections not addressed
- [ ] Unclear differentiation from competitors
- [ ] No proof/evidence (case studies, testimonials)
- [ ] Hard to find information (poor navigation/IA)

**Optimization Opportunities**:
1. **Add FAQ section** (use FAQs from Prompt 10):
   - Address top [X] objections from Reddit research
   - Placement: [Service pages, homepage, dedicated FAQ page]
   - Implementation: FAQ schema for AI visibility

2. **Improve navigation**:
   - Current navigation: [Assess clarity]
   - Recommended structure: [Specific changes]

3. **Add proof elements**:
   - Case studies: [X examples with specific results]
   - Testimonials: [Placement and format]
   - Stats/numbers: "[X customers served, Y% success rate]"

---

#### Stage 4: Conversion Action
**Current State**:
- Conversion goals: [List - form submission, phone call, purchase, booking]
- Conversion rate: [X%] (if known from analytics)
- Forms: [List forms and their fields]
- CTAs: [List current CTAs and placement]

**Friction Points**:
- [ ] Form too long (>5 fields)
- [ ] CTA not prominent or clear
- [ ] Multiple competing CTAs causing decision paralysis
- [ ] No urgency or reason to act now
- [ ] Unclear what happens after submission
- [ ] Missing trust signals at point of conversion

**CTA Analysis**:
| Current CTA | Location | Issues | Improved CTA | Rationale |
|-------------|----------|--------|--------------|-----------|
| [Current text] | [Page/placement] | [What's wrong] | "[Better copy from Prompt 10]" | [Why better] |

**Form Optimization**:
For each conversion form:

**Form**: [Name/Purpose]
**Current fields**: [List all]
**Conversion rate**: [X%] (if known)

**Recommendations**:
- Remove fields: [Which ones and why]
- Add fields: [Which ones and why]
- Optimal field count: [3-5 for lead gen, vary by context]
- Progressive disclosure: [For long forms, break into steps]
- Trust signals: [Add privacy statement, security badges]
- Button copy: Change from "[Current]" to "[Improved]"

**Multi-step form option** (if form is long):
- Step 1: [Fields 1-3]
- Step 2: [Fields 4-6]
- Step 3: [Confirmation]
- Progress indicator: Yes
- Expected impact: [+X% conversion based on industry benchmarks]

---

#### Stage 5: Post-Conversion & Nurture
**Current State**:
- Lead nurture sequence: [Exists? What does it include?]
- Email follow-up: [Timing and content]
- Retargeting: [Active? What audiences?]

**Friction Points**:
- [ ] No immediate confirmation or next steps
- [ ] Long response time to leads
- [ ] No nurture sequence for consideration stage
- [ ] Leads go cold due to long sales cycle

**Optimization Opportunities**:
1. **Immediate confirmation**:
   - Thank you page: [Specific content]
   - Confirmation email: [Subject line and key content]
   - Next steps clarity: "[What to expect, timeline]"

2. **Nurture sequence** (especially for long sales cycle B2B):
   - Day 0: Confirmation + resource
   - Day 3: Education content (link to blog from Prompt 10)
   - Day 7: Case study/proof
   - Day 14: Check-in + offer to talk
   - [Continue for full sequence]

3. **Retargeting strategy**:
   - Audience 1: Visited [high-intent pages] but didn't convert
   - Audience 2: Converted but haven't purchased/booked (if multi-step)
   - Creative: [Messaging angles]

---

## Conversion Rate Benchmarks & Targets

### Current Performance (if available from Prompt 5):
- Overall site conversion rate: [X%]
- Top converting pages: [List]
- Worst converting pages: [List]
- Conversion rate by traffic source: [Breakdown]

### Industry Benchmarks:
- [Industry] average conversion rate: [X%] (cite source)
- Top performers: [Y%]
- Our target: [Z%] (justify based on current + optimization potential)

### Projected Impact:
If current CR is [X%] and we implement:
1. [Optimization 1] → +[Y%] improvement
2. [Optimization 2] → +[Y%] improvement
3. [Optimization 3] → +[Y%] improvement

**Total projected improvement**: [X%] → [Z%] (+[%] increase)

**Revenue impact** (if deal size known):
- Current: [Traffic × CR × Deal Size = £X/month]
- After optimization: [Traffic × New CR × Deal Size = £Y/month]
- **Incremental gain**: £[Y-X]/month = £[Annual] annually

---

## Specific CRO Recommendations

### Priority 1: Quick Wins (High Impact, Low Effort)
1. **[Recommendation 1]**
   - Current state: [What's wrong]
   - Fix: [Specific action]
   - Expected impact: [+X% conversion]
   - Time to implement: [Hours]
   - Responsible: [Role]

[List 5-10 quick wins]

### Priority 2: Strategic Projects (High Impact, High Effort)
1. **[Recommendation 1]**
   - Current state: [What's wrong]
   - Fix: [Specific action]
   - Expected impact: [+X% conversion]
   - Time to implement: [Days/weeks]
   - Responsible: [Role]

[List 3-5 strategic projects]

### Priority 3: Continuous Optimization
1. **[Ongoing activity 1]**
   - Activity: [What to do]
   - Frequency: [Weekly/monthly]
   - Owner: [Role]

[List 3-5 ongoing activities]

---

## Page-Specific CRO Actions

For each high-traffic or high-intent page:

### Page: [Name]
**Traffic**: [X visitors/month]
**Current CR**: [Y%]
**Target CR**: [Z%]
**Revenue Opportunity**: £[X] annual

**Above-the-Fold**:
- Headline: "[Current]" → "[Improved]"
- Subheadline: "[Current]" → "[Improved]"
- CTA: "[Current]" → "[Improved from Prompt 10]"
- Hero image: [Current] → [Improved specification]

**Trust Signals to Add**:
- [Review stars/count]
- [Client logos]
- [Certification badges]
- [Social proof: "Join X happy customers"]
- [Guarantee statement]

**Objections to Address**:
From Reddit research (Prompt 7):
- Objection 1: "[Customer concern]"
  - Where to address: [Section/placement]
  - How to address: "[Copy/approach]"
- [List all objections for this page]

**Form Optimization**:
- Current fields: [X]
- Optimal fields: [Y]
- Remove: [Fields to remove]
- Button text: "[Current]" → "[Improved]"

**Expected Impact**:
- Current: [X visitors × Y% CR = Z conversions/month]
- After optimization: [X visitors × New CR = N conversions/month]
- Gain: [+X conversions/month]

---

## A/B Testing Roadmap

### Tests to Run (prioritized):

#### Test 1: Homepage Headline
- **Hypothesis**: Clearer value proposition will increase engagement and conversions
- **Variation A (Control)**: "[Current headline]"
- **Variation B**: "[New headline addressing customer job from Prompt 9]"
- **Success Metric**: Conversion rate to [primary CTA]
- **Sample size needed**: [X visitors per variation]
- **Expected runtime**: [X weeks]
- **Predicted winner**: Variation B (+[X%] improvement)

[List 5-10 priority A/B tests]

---

## Mobile Conversion Optimization

### Mobile-Specific Issues:
- Mobile traffic: [X%] of total
- Mobile conversion rate: [Y%]
- Desktop conversion rate: [Z%]
- Gap: [Z-Y percentage points]

**Mobile Friction Points**:
- [ ] Forms difficult on mobile (too many fields, small targets)
- [ ] CTAs not thumb-friendly
- [ ] Page speed slow on mobile
- [ ] Navigation unclear
- [ ] Pop-ups block content
- [ ] Phone number not click-to-call

**Mobile CRO Actions**:
1. [Specific mobile fix 1]
2. [Specific mobile fix 2]
3. [Specific mobile fix 3]

---

## Integration with SEO Strategy

### How CRO Enhances SEO:
1. **Better engagement metrics** → Google ranking signal
   - Lower bounce rate
   - Higher time on site
   - More pages per session

2. **Improved UX** → Core Web Vitals
   - Faster pages
   - Less layout shift
   - Better mobile experience

3. **More conversions** → More reviews → Better local SEO
   - Request reviews from converted customers
   - Reviews improve trust signals
   - Reviews appear in map pack

### SEO Actions That Support CRO:
1. **FAQ schema** (from Prompt 10) → Answers objections → Reduces friction
2. **Faster page speed** (technical SEO) → Better mobile experience → More mobile conversions
3. **Better content** (from Prompt 10) → Addresses customer jobs → Warmer leads

---

## Measurement & Tracking

### Conversion Tracking Setup:
- [ ] GA4 conversion events configured:
  - Event 1: [Form submission]
  - Event 2: [Phone call click]
  - Event 3: [Chat initiated]
  - Event 4: [Purchase/booking]

- [ ] Goal funnels set up:
  - Step 1: [Landing page]
  - Step 2: [Consideration page]
  - Step 3: [Conversion page]

- [ ] Heat mapping tool installed:
  - Tool: [Hotjar / Crazy Egg / etc.]
  - Pages to track: [List priority pages]

- [ ] Session recording:
  - Record sessions from [high-intent pages]
  - Review monthly for UX issues

### CRO Dashboard (Monthly Report):
| Metric | Current | Target | Status |
|--------|---------|--------|--------|
| Overall CR | [X%] | [Y%] | [Red/Amber/Green] |
| Form CR | [X%] | [Y%] | [Red/Amber/Green] |
| Mobile CR | [X%] | [Y%] | [Red/Amber/Green] |
| Avg. time on site | [X min] | [Y min] | [Red/Amber/Green] |
| Bounce rate | [X%] | [Y%] | [Red/Amber/Green] |
| Pages/session | [X] | [Y] | [Red/Amber/Green] |

---

## Success Criteria

This CRO analysis is complete when:
- [x] All 5 funnel stages analyzed with current state documented
- [x] Friction points identified for each stage
- [x] Specific recommendations provided (not generic "improve UX")
- [x] Priority 1, 2, 3 recommendations categorized by impact/effort
- [x] Page-specific CRO actions for top 5-10 pages
- [x] Expected conversion rate improvements quantified
- [x] Revenue impact calculated (if deal size available)
- [x] A/B testing roadmap with 5-10 prioritized tests
- [x] Mobile-specific optimizations included
- [x] Integration with SEO strategy explained
- [x] Measurement framework and tracking setup defined

---

## Assumptions to Label

- [ASSUMPTION: If conversion rate not available from analytics, estimate based on [industry benchmark] for [business type]]
- [ASSUMPTION: If deal size not provided, estimate impact in percentage terms only]
- [ASSUMPTION: A/B test duration assumes [X] visitors per week to reach statistical significance]
- [ASSUMPTION: Mobile vs desktop split is [X%]/[Y%] based on industry norms for [business type]]

---

## Deliverable Format

### CRO Analysis Document Structure:
```markdown
# Conversion Rate Optimization Analysis
**For**: [Client Name]
**Business Model**: [B2B/B2C/E-commerce]
**Primary Goal**: [From Intake]

## Executive Summary
- Current conversion rate: [X%]
- Target conversion rate: [Y%]
- Expected revenue impact: £[X] annually
- Top 3 priorities: [List]

## Funnel Analysis
[5 stages with current state, friction points, recommendations]

## Priority Recommendations
[Organized by quick wins, strategic projects, continuous optimization]

## Page-Specific Actions
[Top 5-10 pages with specific CRO tasks]

## A/B Testing Roadmap
[Prioritized list of tests to run]

## Measurement Framework
[Tracking setup, dashboard, reporting]

## Integration with SEO Strategy
[How CRO and SEO reinforce each other]
```

---

## Cross-References
- **Integrates with Prompt 9**: JTBD informs messaging and objection handling
- **Integrates with Prompt 10**: Uses copy examples for CTA optimization
- **Integrates with Prompt 12**: CRO actions become implementation tasks
- **Validated by Prompt 11**: QA ensures CRO recommendations support business challenge
