# Prompt 11: QA Validation & Quality Assurance

## Purpose
Comprehensive quality review of the complete AI SEO strategy document to ensure it addresses the business challenge, maintains consistency across all sections, and meets deliverable requirements. This is the final validation gate before delivery.

## When to Run
After all other prompts (1-10) are complete and the strategy document has been assembled.

## Inputs Required
- **Complete strategy document** (from Prompt 8, enhanced by all subsequent prompts)
- **Business challenge statement** (from Intake Section 1 or initial brief)
- **Success criteria** (from Intake Section 4)
- **All outputs from Prompts 1-10**
- **Intake form** (original client brief)

## QA Framework: 12 Validation Criteria

### 1. Challenge Alignment ⭐ CRITICAL
**Question**: Does the strategy document directly address the stated business challenge?

**Validation Checks**:
- [ ] Business challenge is explicitly referenced in Executive Summary
- [ ] Every major recommendation connects back to solving the challenge
- [ ] 30/60/90-day roadmap priorities align with challenge resolution
- [ ] Success metrics measure progress against the challenge
- [ ] No generic SEO advice that could apply to any business

**Evidence Required**:
- Quote where challenge is addressed in Executive Summary
- Map 5-7 key recommendations to challenge resolution
- Show how success metrics measure challenge progress

**Rating**: Pass / Needs Revision / Fail
**Notes**: [Specific issues or confirmations]

---

### 2. Data Foundation
**Question**: Are all recommendations grounded in actual data, not assumptions?

**Validation Checks**:
- [ ] Every major recommendation cites specific data source
- [ ] Ahrefs data is used correctly (DR, backlinks, content gaps, keyword gaps)
- [ ] HikeSEO data is used correctly (GSC metrics, on-site recommendations, AI visibility)
- [ ] Reddit research provides verbatim customer language
- [ ] LinkedIn research informs ICP understanding
- [ ] Competitive analysis uses real competitor data, not guesses
- [ ] Any assumptions are clearly labeled with [ASSUMPTION: ...]

**Data Source Check**:
- Ahrefs references: [Count]
- HikeSEO references: [Count]
- Reddit verbatim quotes: [Count]
- LinkedIn insights: [Count]
- Assumptions labeled: [Count]

**Rating**: Pass / Needs Revision / Fail
**Notes**: [Which recommendations lack data support?]

---

### 3. Specificity & Actionability
**Question**: Can the client implement recommendations without further clarification?

**Validation Checks**:
- [ ] NO vague recommendations like "improve content" or "build links"
- [ ] Every recommendation includes WHAT to do and HOW to do it
- [ ] Copy examples are actual copy, not templates or placeholders
- [ ] Page-level actions specify exact pages and exact changes
- [ ] Link building targets specific websites/publications
- [ ] Technical SEO recommendations include implementation steps
- [ ] Keyword targets are specific phrases with search volume data

**Red Flags** (must not appear):
- ❌ "Optimize your content"
- ❌ "Build high-quality backlinks"
- ❌ "Improve user experience"
- ❌ "Create better meta descriptions"
- ❌ "Target relevant keywords"
- ❌ Generic advice without specifics

**Green Flags** (should appear):
- ✅ "Add FAQ schema to /services/emergency-plumbing with these 7 questions: [list]"
- ✅ "Rewrite homepage H1 to: 'Emergency Plumber Manchester | 24/7 Response'"
- ✅ "Target Digital PR outreach to: The Guardian, BBC News, Manchester Evening News"
- ✅ "Create blog post: '7 Signs You Need Emergency Plumbing' targeting 'emergency plumbing signs' (480 monthly searches)"

**Rating**: Pass / Needs Revision / Fail
**Notes**: [Examples of vague vs specific recommendations]

---

### 4. Consistency Across Sections
**Question**: Do all sections of the strategy align and reinforce each other?

**Validation Checks**:
- [ ] Keywords from Prompt 9 appear in copy examples from Prompt 10
- [ ] Content titles (Prompt 10) target keyword clusters (Prompt 9)
- [ ] JTBD framework (Prompt 9) informs content strategy (Prompt 10)
- [ ] 30/60/90-day roadmap aligns with 4-layer growth model (Prompt 8)
- [ ] Implementation tasks (Prompt 12) match strategy recommendations (Prompt 8)
- [ ] Onpage/offpage split is maintained throughout
- [ ] Priority services from intake appear in strategy priorities
- [ ] Geographic targeting (UK/global/local) is consistent

**Cross-Reference Check**:
- Pick 5 keywords from Prompt 9 → Verify they appear in Prompt 10 copy examples
- Pick 3 customer jobs from Prompt 9 → Verify strategy addresses them
- Pick 5 priority recommendations → Verify they appear in 30/60/90 roadmap

**Rating**: Pass / Needs Revision / Fail
**Notes**: [Inconsistencies found]

---

### 5. Commercial Context Integration
**Question**: Does the strategy account for business model, deal size, sales cycle, and revenue goals?

**Validation Checks**:
- [ ] Recommendations align with primary goal (leads/revenue/visibility)
- [ ] If high deal size, strategy prioritizes quality over volume
- [ ] If long sales cycle, strategy includes nurture content
- [ ] If short sales cycle, strategy focuses on conversion optimization
- [ ] B2B strategies emphasize authority and expertise
- [ ] B2C strategies emphasize trust signals and reviews
- [ ] Local strategies emphasize GBP, reviews, map pack
- [ ] E-commerce strategies emphasize product pages and IA (if applicable)

**Commercial Alignment Check**:
- Primary goal from intake: [state goal]
- Top 3 recommendations: [list them]
- Do they directly support the goal? [Yes/No + reasoning]

**Rating**: Pass / Needs Revision / Fail
**Notes**: [Commercial disconnects]

---

### 6. Prioritization & Sequencing
**Question**: Are recommendations properly prioritized by impact/effort, and sequenced logically?

**Validation Checks**:
- [ ] 30/60/90-day roadmap shows clear progression
- [ ] Quick wins identified and scheduled early
- [ ] Foundation work (Layer 1) comes before awareness work (Layer 4)
- [ ] Technical fixes addressed before content creation
- [ ] High-impact, low-effort tasks prioritized
- [ ] Dependencies are clear (e.g., "do X before Y")
- [ ] Resource requirements match stated constraints (from intake)
- [ ] Timeline is realistic given available resources

**Prioritization Matrix Check**:
- Quick Wins (High Impact, Low Effort): [Count recommendations]
- Strategic Projects (High Impact, High Effort): [Count]
- Fill-ins (Low Impact, Low Effort): [Count]
- Avoid (Low Impact, High Effort): [Should be 0]

**Rating**: Pass / Needs Revision / Fail
**Notes**: [Sequencing issues]

---

### 7. Deliverable Completeness
**Question**: Are all required deliverables present and complete?

**Required Deliverables** (from intake form Section 4):
- [ ] **Executive Summary**: 2-3 pages, client-ready, jargon-free
- [ ] **Detailed SEO + AI Visibility Plan**: Complete strategy document (Prompt 8)
- [ ] **30/60/90-day Roadmap**: Specific actions per phase with owners and metrics
- [ ] **12-month Strategic Plan**: Quarterly themes, goals, resource allocation
- [ ] **Prioritised Backlog**: All recommendations in impact/effort matrix
- [ ] **Copy Examples**: Titles, meta descriptions, 50+ FAQs, social posts, page intros
- [ ] **Client-ready Version**: Business-focused, suitable for presentation

**Content Check**:
- Executive Summary word count: [X words - should be 600-900]
- Strategy document sections: [Count - should match Prompt 8 structure]
- Copy examples: [Count FAQs, titles, meta descriptions]
- Roadmap completeness: [Days 0-30, 31-60, 61-90 all populated?]

**Rating**: Pass / Needs Revision / Fail
**Notes**: [Missing deliverables]

---

### 8. Tone & Audience Appropriateness
**Question**: Is the tone appropriate for the intended audience?

**Validation Checks**:
- [ ] UK English throughout (organisation, optimise, colour)
- [ ] Technical sections use SEO terminology correctly
- [ ] Client-facing sections avoid jargon or explain it
- [ ] Tone matches intake preferences (direct/neutral/persuasive)
- [ ] No corporate waffle or buzzwords
- [ ] Active voice, clear sentences
- [ ] Practical focus, not theoretical

**Tone Audit**:
- Check Executive Summary for jargon: [List any found]
- Check for buzzwords: "synergy", "leverage", "optimise excellence" [Should be 0]
- Check for passive voice: [Should be minimal]

**Rating**: Pass / Needs Revision / Fail
**Notes**: [Tone issues]

---

### 9. E-E-A-T Signals
**Question**: Does the strategy demonstrate Experience, Expertise, Authoritativeness, and Trustworthiness?

**Validation Checks**:
- [ ] Recommendations show deep understanding of industry/niche
- [ ] Strategy references credible data sources (Ahrefs, HikeSEO, industry reports)
- [ ] Copy examples demonstrate expertise in subject matter
- [ ] No generic template language
- [ ] Specific examples show practical experience
- [ ] Recommendations account for industry-specific nuances
- [ ] Strategy acknowledges risks/limitations where appropriate

**E-E-A-T Evidence**:
- Industry-specific insights: [Count examples]
- Data citations: [Count]
- Practical examples: [Count]
- Generic template language: [Should be 0]

**Rating**: Pass / Needs Revision / Fail
**Notes**: [Where does strategy feel generic?]

---

### 10. AI Visibility Integration
**Question**: Does the strategy properly address AI answer engines (ChatGPT, Perplexity, Claude, Gemini)?

**Validation Checks**:
- [ ] AI visibility tactics are included (not just traditional SEO)
- [ ] FAQ schema recommendations for AI citation opportunities
- [ ] Question-based content for conversational queries
- [ ] Structured data strategy for AI parsing
- [ ] Authority-building for AI source credibility
- [ ] Specific AI visibility goals in success metrics
- [ ] AI answer engine optimization integrated throughout, not siloed

**AI Visibility Check**:
- FAQ schema recommendations: [Count]
- Question-based content titles: [Count from Prompt 10]
- Structured data types recommended: [List]
- AI visibility mentioned in 30/60/90 roadmap: [Yes/No]

**Rating**: Pass / Needs Revision / Fail
**Notes**: [AI visibility gaps]

---

### 11. Local SEO (If Applicable)
**Question**: If this is a local business, does the strategy properly address local SEO?

**Validation Checks** (skip if not local):
- [ ] Google Business Profile optimization included
- [ ] Map pack competitor analysis referenced
- [ ] Reviews strategy included (generation + management)
- [ ] LocalBusiness schema recommended
- [ ] Location-based keywords targeted
- [ ] NAP consistency mentioned
- [ ] Local link building tactics included
- [ ] Service area pages recommended (if multi-location)

**Local SEO Evidence**:
- GBP optimization tasks: [Count]
- Review strategy: [Present? Yes/No]
- Local schema: [Recommended? Yes/No]
- Location pages: [How many recommended?]

**Rating**: Pass / Needs Revision / Fail / Not Applicable
**Notes**: [Local SEO gaps]

---

### 12. Measurement Framework
**Question**: Can the client track progress and measure success?

**Validation Checks**:
- [ ] Success metrics defined (from intake Section 4)
- [ ] Baseline metrics stated (current performance)
- [ ] Target metrics with timeframes (30/60/90-day, 12-month)
- [ ] Tracking setup instructions (GSC, GA4, Ahrefs, HikeSEO)
- [ ] Reporting cadence recommended (weekly/monthly)
- [ ] KPIs mapped to 4-layer model
- [ ] Dashboard or reporting template suggested
- [ ] Attribution model for conversions addressed

**Measurement Check**:
- Primary metric: [From intake]
- Secondary metrics: [List]
- Baseline stated: [Yes/No]
- Targets with dates: [Yes/No]
- Reporting template: [Included? Yes/No]

**Rating**: Pass / Needs Revision / Fail
**Notes**: [Measurement gaps]

---

## Overall QA Summary

### Scoring
- **12/12 Pass**: Ready for delivery
- **10-11/12 Pass**: Minor revisions needed
- **8-9/12 Pass**: Moderate revisions needed
- **Below 8**: Major revisions required

### Critical Failures (Auto-Fail)
If ANY of these fail, entire document must be revised:
1. **Challenge Alignment** (Criterion 1) - MUST pass
2. **Specificity** (Criterion 3) - MUST pass
3. **Deliverable Completeness** (Criterion 7) - MUST pass

### Revision Priority
If revisions needed, address in this order:
1. Challenge alignment issues
2. Missing deliverables
3. Vague/non-actionable recommendations
4. Data gaps
5. Inconsistencies
6. Tone/audience issues
7. Other criteria

## Output Format

### QA Report Structure
```markdown
# QA Validation Report
**Date**: [Date]
**Strategy For**: [Client/Project Name]
**Business Challenge**: [State the challenge]

## Overall Score: X/12

### ✅ Criteria Passed (X/12)
[List passed criteria]

### ⚠️ Criteria Needing Revision (X/12)
[List criteria with issues]

### ❌ Critical Failures (X/12)
[List any critical failures]

## Detailed Findings

### 1. Challenge Alignment
**Rating**: [Pass/Needs Revision/Fail]
**Findings**: [Detailed notes]
**Action Required**: [Specific fixes needed]

[Repeat for all 12 criteria]

## Revision Checklist
- [ ] [Specific revision 1]
- [ ] [Specific revision 2]
- [ ] [Specific revision 3]

## Strengths
[What's working well in the strategy]

## Final Recommendation
- [ ] **Approve for Delivery** (12/12 or 10-11/12 with minor fixes)
- [ ] **Revise & Re-Review** (8-9/12)
- [ ] **Major Rework Required** (<8/12)
```

## Success Criteria

This QA validation is complete when:
- [x] All 12 criteria have been evaluated
- [x] Each criterion has a rating (Pass/Needs Revision/Fail)
- [x] Specific issues are documented with examples
- [x] Revision checklist is provided (if needed)
- [x] Overall recommendation is clear (Approve/Revise/Rework)
- [x] If approved, document is ready for client delivery
- [x] If revisions needed, specific action items are listed

## Post-QA Actions

### If Score is 12/12 or 10-11/12 (PASS):
1. Make any minor revisions noted
2. Final proofread for typos/formatting
3. Export client-ready version
4. Prepare executive summary as standalone document
5. Ready for delivery

### If Score is 8-9/12 (NEEDS REVISION):
1. Address revision checklist systematically
2. Re-run QA after revisions
3. Iterate until passing score achieved

### If Score is <8/12 (MAJOR REWORK):
1. Identify which prompts (1-10) need re-execution
2. Re-run those specific prompts with corrections
3. Reassemble strategy document
4. Re-run QA validation

## Integration Points

- **Validates all prompts**: 1-10 outputs are checked for quality
- **Feeds into delivery**: Only passing QA allows progression to client handoff
- **Informs iteration**: QA findings guide revisions before re-delivery
