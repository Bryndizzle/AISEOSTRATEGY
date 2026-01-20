# Stage 6.5: E-E-A-T Quality Assurance (MANDATORY)

**Stage Type**: Quality Gate / Content Validation
**Integration Point**: AFTER Stage 6 (Content Specifications) or after Full Page Drafts, BEFORE Stage 7 (Validation & Testing)
**Purpose**: Ensure all content meets Google's E-E-A-T (Experience, Expertise, Authoritativeness, Trustworthiness) standards
**Status**: ✅ Active Enhancement
**Created**: 19 January 2026
**Reference**: [Google's Helpful Content Guidelines](https://developers.google.com/search/docs/fundamentals/creating-helpful-content)

---

## Problem This Solves

**Current State**: Agent creates content but doesn't systematically validate against Google's E-E-A-T guidelines.

**Risk**: Content that violates "helpful content" principles can:
- Fail to rank despite technical optimization
- Trigger algorithmic penalties (especially for YMYL topics)
- Waste resources creating "search engine-first" content that Google explicitly devalues
- Lack trust signals that modern Google algorithms prioritize

**Solution**: Mandatory E-E-A-T quality gate that ALL content must pass before publication.

---

## When to Execute Stage 6.5

**Trigger**: ALWAYS execute for:
- All full page drafts (from Full Page Draft Generator)
- All blog post drafts
- Any content created in Drafting Mode
- Service pages, location pages, comparison pages, guides

**Input Required**:
- Drafted content (from Stage 5 or Full Page Draft Generator)
- Business context (from Stage 1)
- Target audience (from Stage 1)
- Industry type (YMYL vs non-YMYL)

**Output**: Pass/Fail score + specific remediation steps for failures

---

## E-E-A-T Quality Assurance Framework

### Quality Gate System

**ALL content must score 80%+ to pass.**

**Scoring**:
- ✅ **PASS** (Meets criterion): 1 point
- ⚠️ **PARTIAL** (Partially meets, needs improvement): 0.5 points
- ❌ **FAIL** (Does not meet criterion): 0 points

**Total Questions**: 30 questions across 5 categories
**Pass Threshold**: 24/30 points (80%)
**YMYL Content**: Must score 27/30 (90%) - higher bar for health/finance/safety topics

---

## Category 1: Content Quality & Originality (8 Questions)

### Q1: Does the content provide original information, reporting, research, or analysis?

**What Google Wants**:
- Unique insights, not just rephrased competitor content
- Original research, data, case studies, or testing
- First-hand experience or reporting

**How to Evaluate**:
- ✅ **PASS**: Content includes original insights, data, or first-hand experience not found elsewhere
- ⚠️ **PARTIAL**: Content is mostly original but lacks unique insights
- ❌ **FAIL**: Content is rewritten from competitors with no new information

**How to Fix if FAIL**:
1. Add unique data: "We analyzed 500 [service] jobs and found..."
2. Add first-hand experience: "After 10 years as a [profession], I've noticed..."
3. Add original research: Survey customers, analyze industry trends, test products
4. Add case studies: "Real example: When Sarah lost her car keys at 2am..."

**Example (Locksmith Content)**:
- ❌ **FAIL**: "Car key replacement is important. Locksmiths can help you."
- ⚠️ **PARTIAL**: "Car key replacement costs £180-£250. Locksmiths are cheaper than dealerships."
- ✅ **PASS**: "We analyzed 500 car key replacement jobs in Essex (2024-2025) and found dealerships charge an average of £427 vs locksmiths at £189 - a 56% markup. The biggest price gaps were for German vehicles (BMW, Mercedes), where dealerships charged up to £650 vs £220 for locksmiths."

---

### Q2: Does the content provide substantial, complete, or comprehensive description of the topic?

**What Google Wants**:
- All relevant aspects covered
- No critical information missing
- Depth appropriate to the topic

**How to Evaluate**:
- ✅ **PASS**: Topic covered comprehensively - no obvious gaps
- ⚠️ **PARTIAL**: Topic covered but missing some relevant aspects
- ❌ **FAIL**: Shallow, incomplete, or missing critical information

**How to Fix if FAIL**:
1. Add FAQ section answering common questions (5-15 questions)
2. Add "What to expect" section (process, timeline, costs)
3. Add comparison section (options, pros/cons)
4. Add "Common mistakes" or "What people get wrong" section
5. Target word count: 2,000-2,500 for service pages, 1,500-2,000 for location pages

**Missing Critical Information Checklist**:
For service pages, must include:
- [ ] What the service is (definition)
- [ ] When you need it (scenarios/use cases)
- [ ] How it works (process/steps)
- [ ] How much it costs (pricing or price ranges)
- [ ] How long it takes (timeframe)
- [ ] What's included (scope)
- [ ] What's NOT included (exclusions)
- [ ] Alternatives (other options)
- [ ] Common questions (FAQ)

---

### Q3: Does the content provide insightful analysis or interesting information beyond the obvious?

**What Google Wants**:
- Goes beyond surface-level information
- Provides "aha moments" or non-obvious insights
- Explains the "why" behind the "what"

**How to Evaluate**:
- ✅ **PASS**: Content provides insights, explanations, or information that's not obvious
- ⚠️ **PARTIAL**: Content is accurate but states only obvious information
- ❌ **FAIL**: Content is generic, surface-level, could apply to any business

**How to Fix if FAIL**:
1. Add "Why this matters" explanations
2. Add "What most people don't know" section
3. Add counterintuitive insights: "You'd think X, but actually Y"
4. Add expert tips: "Pro tip from 10 years in the industry..."
5. Explain common misconceptions

**Example (Locksmith Content)**:
- ❌ **FAIL**: "You should get a spare car key."
- ⚠️ **PARTIAL**: "Spare keys cost less than emergency replacements."
- ✅ **PASS**: "The biggest mistake we see: people wait until they've lost their only key to get a spare. A £99 spare key becomes a £350-£450 emergency replacement because dealerships charge 'programming from VIN' fees when there's no working key to clone. The key itself costs the same - you're paying £250-£350 extra for the programming method. Get a spare while you still have a working key and you'll save that entire fee."

---

### Q4: If content draws on other sources, does it avoid simply copying or rewriting, and provide substantial additional value?

**What Google Wants**:
- Original synthesis, not paraphrasing
- Add your own insights, experience, or analysis
- Cite sources properly

**How to Evaluate**:
- ✅ **PASS**: Sources cited, substantial original analysis added
- ⚠️ **PARTIAL**: Sources cited but limited original value added
- ❌ **FAIL**: Content is rewritten from sources with no new value

**How to Fix if FAIL**:
1. After citing data, add your interpretation: "What this means for Essex drivers is..."
2. Add your own experience: "In our experience serving 5,000+ customers..."
3. Add local context: "While national averages show X, in Essex we see Y because..."
4. Add comparative analysis: "While [Source 1] says X and [Source 2] says Y, our data suggests Z"
5. Cite sources properly: "According to Which? (2026), transponder key replacement costs..."

---

### Q5: Does the main heading or page title provide a descriptive, helpful summary?

**What Google Wants**:
- Clear, accurate description of content
- No clickbait, no exaggeration

**How to Evaluate**:
- ✅ **PASS**: Heading accurately describes content, helpful, not sensational
- ⚠️ **PARTIAL**: Heading is accurate but could be more descriptive
- ❌ **FAIL**: Heading is clickbait, exaggerated, or doesn't match content

**How to Fix if FAIL**:
1. Make heading descriptive: Include what, where, who
2. Remove superlatives: "Best", "Ultimate", "Perfect"
3. Remove sensationalism: "You Won't Believe...", "Shocking..."
4. Add specifics: "Car Key Replacement Essex" better than "Key Services"

**Examples**:
- ❌ **FAIL**: "The Ultimate Guide to Car Keys That Will Change Your Life"
- ⚠️ **PARTIAL**: "Car Key Information"
- ✅ **PASS**: "Car Key Replacement Essex: Cost, Process & Same-Day Service"

---

### Q6: Is this content you'd bookmark, share with a friend, or recommend?

**What Google Wants**:
- Genuinely useful, high-quality content
- Something you'd return to

**How to Evaluate**:
- ✅ **PASS**: Yes, I would bookmark/share this
- ⚠️ **PARTIAL**: Maybe, depending on context
- ❌ **FAIL**: No, this is generic filler

**Self-Test**:
- Would you text this page to a friend who asked for [service] recommendations?
- Would you bookmark this to reference later?
- Does this content solve a real problem?
- Is it better than what competitors offer?

**How to Fix if FAIL**:
1. Add actionable takeaways
2. Add specific, helpful details (pricing, timelines, process)
3. Remove filler and generic statements
4. Add useful tools: Cost calculators, checklists, comparison tables
5. Make it genuinely helpful, not just SEO-optimized

---

### Q7: Would you expect to see this content in a printed magazine, encyclopedia, or book?

**What Google Wants**:
- Professional quality, well-researched
- Deserves permanent publication

**How to Evaluate**:
- ✅ **PASS**: Yes, this meets editorial standards
- ⚠️ **PARTIAL**: Close, but needs polish
- ❌ **FAIL**: No, this is clearly low-quality web filler

**How to Fix if FAIL**:
1. Improve writing quality: Remove typos, fix grammar, improve flow
2. Add structure: Clear sections, subheadings, logical flow
3. Add depth: Research, data, examples, case studies
4. Remove fluff: Cut generic statements, obvious information
5. Raise bar to "publication quality"

---

### Q8: Does content provide substantial value compared to other pages in search results?

**What Google Wants**:
- Better than competitors
- Unique value proposition

**How to Evaluate**:
- ✅ **PASS**: This content is better than top 3 ranking competitors
- ⚠️ **PARTIAL**: Similar quality to competitors
- ❌ **FAIL**: Worse than or same as competitors

**Competitive Analysis**:
1. Search target keyword
2. Read top 3 ranking pages
3. Ask: What does MY content have that THEIRS doesn't?
   - More specific pricing?
   - Better process explanation?
   - More comprehensive FAQ?
   - Original data/research?
   - First-hand experience?
   - Local context?

**How to Fix if FAIL**:
1. Identify competitor gaps and fill them
2. Add something competitors don't have (data, tools, local insights)
3. Go deeper on key topics
4. Add more specific, actionable information

---

## Category 2: Expertise & Experience (7 Questions)

### Q9: Does content present information in a way that makes you trust it?

**What Google Wants**:
- Clear sourcing
- Evidence of expertise
- Professional presentation

**How to Evaluate**:
- ✅ **PASS**: Content clearly demonstrates expertise and trustworthiness
- ⚠️ **PARTIAL**: Some trust signals but incomplete
- ❌ **FAIL**: No trust signals, questionable credibility

**Trust Signal Checklist**:
- [ ] Author byline present (who wrote this)
- [ ] Author credentials stated (years of experience, certifications)
- [ ] Sources cited for data/statistics
- [ ] First-hand experience demonstrated
- [ ] Business credentials mentioned (years in business, certifications, reviews)
- [ ] Contact information clearly visible
- [ ] Professional presentation (no typos, good formatting)

**How to Fix if FAIL**:
1. Add author byline: "Written by [Name], [Credentials]"
2. Add credentials: "John Smith has been an Auto Locksmith Association certified locksmith for 12 years, completing 5,000+ emergency callouts across Essex."
3. Add business credentials: "Speedy Keys: Serving Essex since 2010, 4.9★ Checkatrade rating (187 reviews)"
4. Cite sources for all statistics
5. Add "About the Author" section at end of page

---

### Q10: Is there background about the author or site available?

**What Google Wants**:
- Author page or bio
- Site About page
- Clear identity

**How to Evaluate**:
- ✅ **PASS**: Author bio AND site About page present
- ⚠️ **PARTIAL**: One but not both present
- ❌ **FAIL**: No author info, no About page

**How to Fix if FAIL**:
1. Create author bio at end of content:
   ```markdown
   ## About the Author

   [Author Name] is a [credentials/role] with [X] years of experience in [industry]. [They have/He has/She has] [specific achievements or qualifications]. [Author Name] specializes in [specific expertise] and has helped [number] customers with [specific services].
   ```

2. Link to site About page: "Learn more about [Business Name] on our [About page](/about/)."

3. Include business story: "Founded in [year] by [founder name], [Business] has served [location] for [X] years."

---

### Q11: If someone researched the site, would they find it's well-trusted or recognized as an authority?

**What Google Wants**:
- Established reputation
- Industry recognition
- Positive reviews

**How to Evaluate**:
- ✅ **PASS**: Clear evidence of authority (reviews, certifications, industry recognition)
- ⚠️ **PARTIAL**: Some authority signals but limited
- ❌ **FAIL**: No authority signals

**Authority Signal Checklist**:
- [ ] High review rating (4.5★+) with substantial review count (50+)
- [ ] Industry certifications mentioned (trade associations, accreditations)
- [ ] Years in business stated
- [ ] Customer count or jobs completed stated
- [ ] Industry awards or recognition
- [ ] Media mentions or features
- [ ] Professional memberships

**How to Fix if FAIL**:
1. Add review stats: "Rated 4.8★ on Checkatrade based on 187 verified reviews"
2. Add certifications: "Auto Locksmith Association approved", "Which? Trusted Trader"
3. Add years in business: "Serving Essex since 2010 (14 years)"
4. Add customer count: "5,000+ emergency callouts completed"
5. Add industry recognition: "Featured in Essex Chronicle (2024)"

---

### Q12: Is content written or reviewed by an expert who demonstrably knows the topic well?

**What Google Wants**:
- Clear demonstration of expertise
- Not generic outsourced content

**How to Evaluate**:
- ✅ **PASS**: Content clearly written by subject matter expert
- ⚠️ **PARTIAL**: Some expertise demonstrated but not clear
- ❌ **FAIL**: Generic content that could be written by anyone

**Expertise Demonstration**:
- Uses industry-specific terminology correctly
- Provides technical details only an expert would know
- Shares first-hand experiences: "In my 10 years as a locksmith, I've seen..."
- Explains the "why" behind processes, not just the "what"
- Addresses nuances and edge cases
- Corrects common misconceptions

**How to Fix if FAIL**:
1. Add first-hand experiences: "After 5,000+ callouts, the most common issue we see is..."
2. Add technical depth: "Modern transponder keys use RFID frequencies between 125-134 kHz..."
3. Add insider knowledge: "What most people don't realize is..."
4. Add troubleshooting: "If X happens, it usually means Y because Z"
5. Sign content with expert name and credentials

---

### Q13: Does content have any easily-verified factual errors?

**What Google Wants**:
- Factual accuracy
- No misinformation

**How to Evaluate**:
- ✅ **PASS**: All facts verified, no errors
- ⚠️ **PARTIAL**: Minor errors or unverified claims
- ❌ **FAIL**: Factual errors present

**How to Check**:
1. Verify all statistics against sources
2. Check industry-specific facts with trade bodies
3. Verify pricing against current market rates
4. Check technical specifications
5. Verify legal/regulatory information

**How to Fix if FAIL**:
1. Fact-check all statistics
2. Update outdated information
3. Remove unverified claims
4. Add sources for all data
5. Verify industry-specific details with expert review

---

### Q14: Does content demonstrate first-hand expertise?

**What Google Wants**:
- Evidence you've actually done this work/used this product
- Not just desk research

**How to Evaluate**:
- ✅ **PASS**: Clear first-hand experience demonstrated throughout
- ⚠️ **PARTIAL**: Some first-hand mentions but mostly generic
- ❌ **FAIL**: No evidence of first-hand experience

**First-Hand Experience Indicators**:
- "In our experience serving [X] customers..."
- "We've noticed that..."
- "The most common issue we encounter is..."
- "After testing [X] products..."
- Specific examples: "Last month, a customer called us at 2am..."
- Photos of actual work (if applicable)
- Case studies from real customers
- Specific details only someone doing the work would know

**How to Fix if FAIL**:
1. Add customer examples (anonymized if necessary)
2. Add "We've found that..." statements based on real experience
3. Add photos of your actual work/products/services
4. Add case studies: "Real Example: When Sarah from Colchester..."
5. Add process details only an expert would know

---

### Q15: Is it clear WHO created the content?

**What Google Wants**:
- Clear authorship
- Accountability

**How to Evaluate**:
- ✅ **PASS**: Author clearly identified with credentials
- ⚠️ **PARTIAL**: Author identified but no credentials
- ❌ **FAIL**: No author identified

**Byline Requirements**:
```markdown
**Written by**: [Author Name], [Title/Credentials]
**Last Updated**: [Date]
**Reviewed by**: [Name, Credentials] (if applicable)
```

**Example**:
```markdown
**Written by**: John Smith, Auto Locksmith Association Certified Technician
**Last Updated**: 19 January 2026
**Experience**: 12 years serving Essex, 5,000+ emergency callouts completed
```

**How to Fix if FAIL**:
1. Add author byline at top of content
2. Add author bio at end of content
3. Add credentials/experience
4. Add last updated date
5. Link to author page if available

---

## Category 3: "How" - Content Creation Process (4 Questions)

### Q16: Is it self-evident HOW the content was created?

**What Google Wants**:
- Transparency about creation process
- Especially for AI-generated content

**How to Evaluate**:
- ✅ **PASS**: Clear disclosure of creation process (human-written, AI-assisted, etc.)
- ⚠️ **PARTIAL**: Somewhat clear but could be more explicit
- ❌ **FAIL**: No information about how content was created

**Disclosure Requirements**:

**For AI-Assisted Content**:
```markdown
## How This Content Was Created

This guide was written by [Author Name], a certified [profession] with [X] years of experience. AI tools were used to assist with research and initial structuring, but all information has been verified based on our first-hand experience serving [number] customers and reflects current industry standards as of [date].
```

**For Human-Written Content**:
```markdown
## About This Guide

This guide was written by [Author Name] based on [X] years of hands-on experience as a [profession] serving [location]. All pricing, process information, and recommendations reflect real-world experience from [number] jobs completed.
```

**How to Fix if FAIL**:
1. Add "How This Content Was Created" section
2. Disclose AI assistance if used (but emphasize human expertise)
3. Explain research process: "Based on analysis of 500 jobs..."
4. Explain testing/verification process if applicable

---

### Q17: Is there background about the research/testing process?

**What Google Wants**:
- Evidence of work involved
- Transparency about methodology

**How to Evaluate**:
- ✅ **PASS**: Clear explanation of research/testing methodology
- ⚠️ **PARTIAL**: Some methodology mentioned but vague
- ❌ **FAIL**: No explanation of how conclusions were reached

**Methodology Disclosure Examples**:

**For Service Content**:
```markdown
## Our Research

This pricing guide is based on analysis of 500 car key replacement jobs completed across Essex between January 2024 and December 2025. Prices reflect actual charges for standard transponder keys, high-security keys, and smart key fobs across 15 different vehicle makes.
```

**For Product Reviews**:
```markdown
## Testing Process

We tested 12 different [products] over 6 months, evaluating [specific criteria]. Each product was tested in [conditions], with results measured by [specific metrics].

[Include photos of actual testing if possible]
```

**How to Fix if FAIL**:
1. Add methodology section explaining how you reached conclusions
2. Add sample size if analyzing data: "Based on 500 jobs..."
3. Add timeframe: "Over 12 months, we..."
4. Add testing criteria: "We evaluated based on X, Y, Z"
5. Add photos/evidence if applicable

---

### Q18: If AI was used, is that disclosed appropriately?

**What Google Wants**:
- Clear disclosure if AI significantly contributed
- Explanation of why AI was useful
- Emphasis on human expertise/review

**How to Evaluate**:
- ✅ **PASS**: AI use disclosed clearly (if used), human expertise emphasized
- ⚠️ **PARTIAL**: Vague about AI involvement
- ❌ **FAIL**: AI-generated content not disclosed OR content is entirely AI without human review

**AI Disclosure Template** (if AI was used):
```markdown
## Content Creation & AI Transparency

This guide was created with AI assistance to help structure information and ensure comprehensive coverage. However, all facts, pricing, recommendations, and insights are based on [Author Name]'s [X] years of first-hand experience as a [profession]. All information has been reviewed for accuracy and reflects current industry standards as of [date].

**Why we used AI**: To ensure no important topics were overlooked while organizing [X] years of hands-on knowledge into a comprehensive guide.

**Human verification**: All pricing verified against 2025-2026 job data. All technical specifications verified against manufacturer standards. All recommendations based on real customer outcomes.
```

**How to Fix if FAIL**:
1. Add AI disclosure if AI was used substantially
2. Emphasize human expertise and review
3. Explain WHY AI was useful (efficiency, organization)
4. Clarify what AI did vs what human expert did
5. Never hide AI use - transparency builds trust

---

### Q19: Is content well-produced, or does it appear sloppy?

**What Google Wants**:
- Professional quality
- Attention to detail

**How to Evaluate**:
- ✅ **PASS**: No typos, good formatting, professional presentation
- ⚠️ **PARTIAL**: Minor issues but overall acceptable
- ❌ **FAIL**: Typos, poor formatting, appears rushed

**Quality Checklist**:
- [ ] No spelling errors
- [ ] No grammar errors
- [ ] Consistent formatting (headings, bullets, spacing)
- [ ] Working internal links
- [ ] Properly formatted tables
- [ ] Images have alt text
- [ ] Paragraphs are readable length (3-5 sentences)
- [ ] Headings follow logical hierarchy (H1 → H2 → H3)
- [ ] Lists use parallel structure
- [ ] Professional tone consistent throughout

**How to Fix if FAIL**:
1. Run spell check
2. Grammar check with Grammarly or similar
3. Review formatting consistency
4. Check all internal links work
5. Have someone else proofread

---

## Category 4: "Why" - Purpose of Content (6 Questions)

### Q20: Is content created primarily to help people (not manipulate rankings)?

**What Google Wants**:
- People-first content
- Genuine utility

**How to Evaluate**:
- ✅ **PASS**: Content clearly helpful, would be useful if someone came directly to site
- ⚠️ **PARTIAL**: Somewhat helpful but overly SEO-optimized
- ❌ **FAIL**: Clearly created just to rank, not to help people

**People-First Content Indicators**:
- Solves a real problem
- Answers actual questions people ask
- Would be useful even without search engine traffic
- Written in natural language, not keyword-stuffed
- Provides actionable information
- Helps people make decisions or take action

**Search Engine-First Warning Signs**:
- Keyword stuffing (keyword appears unnaturally often)
- Awkward phrasing to include keywords
- Content exists only because keyword has search volume
- No unique value - just targets ranking opportunity
- Written to hit word count, not to be helpful
- Lots of similar pages targeting slight keyword variations

**How to Fix if FAIL**:
1. Ask: "Would this help someone who called me directly?"
2. Remove keyword stuffing
3. Rewrite in natural language
4. Add genuine utility (actionable steps, specific information)
5. Focus on solving the user's problem, not ranking

---

### Q21: Do you have an existing audience that would find this content useful?

**What Google Wants**:
- Content for your actual customers
- Not just chasing search traffic

**How to Evaluate**:
- ✅ **PASS**: Yes, our customers would find this useful
- ⚠️ **PARTIAL**: Maybe useful but tangential to core business
- ❌ **FAIL**: Not relevant to our actual customers

**Test**: Would you send this page to an existing customer who asked about this topic?

**How to Fix if FAIL**:
1. Align content with customer needs (not just keyword opportunities)
2. Focus on topics customers actually ask about
3. Remove content created just for traffic (if not relevant to business)

---

### Q22: Does content demonstrate depth of knowledge/first-hand expertise?

**What Google Wants**:
- Expertise from actually doing the work
- Not desk research

**How to Evaluate**:
- ✅ **PASS**: Clear evidence of hands-on experience
- ⚠️ **PARTIAL**: Some experience demonstrated
- ❌ **FAIL**: Generic content anyone could write

**Duplicate of Q14 but worth re-checking in "Why" context.**

**How to Fix if FAIL**: See Q14 remediation steps

---

### Q23: Does your site have a primary purpose or focus?

**What Google Wants**:
- Clear niche/specialization
- Not trying to cover everything

**How to Evaluate**:
- ✅ **PASS**: Site has clear focus matching content topic
- ⚠️ **PARTIAL**: Content somewhat related but stretching focus
- ❌ **FAIL**: Content completely off-topic for site

**Example**:
- ✅ Locksmith site writing about car key replacement
- ⚠️ Locksmith site writing about general car maintenance
- ❌ Locksmith site writing about healthy recipes (off-topic)

**How to Fix if FAIL**:
1. Remove off-topic content
2. Focus on your core expertise
3. Only create content directly related to services you offer

---

### Q24: After reading, will someone have learned enough to achieve their goal?

**What Google Wants**:
- Complete, actionable information
- No need to search again

**How to Evaluate**:
- ✅ **PASS**: Content fully answers question/solves problem
- ⚠️ **PARTIAL**: Helpful but incomplete
- ❌ **FAIL**: Leaves reader needing to search elsewhere

**Completeness Test**:
- Does it answer "How much does it cost?"
- Does it answer "How long does it take?"
- Does it answer "What's the process?"
- Does it answer "What do I need to do?"
- Does it address common concerns/objections?

**How to Fix if FAIL**:
1. Add FAQ section covering all common questions
2. Add complete pricing information (ranges if not fixed)
3. Add process/timeline information
4. Add "What to expect" section
5. Add "Next steps" or clear call to action

---

### Q25: Will someone leave feeling they've had a satisfying experience?

**What Google Wants**:
- Positive user experience
- Problem solved, not frustrated

**How to Evaluate**:
- ✅ **PASS**: Content is helpful, easy to navigate, satisfying
- ⚠️ **PARTIAL**: Helpful but could be better organized
- ❌ **FAIL**: Frustrating, hard to find info, unsatisfying

**User Experience Checklist**:
- [ ] Clear headings make content scannable
- [ ] Important information easy to find
- [ ] No overwhelming walls of text
- [ ] FAQ section for quick answers
- [ ] Clear call to action
- [ ] Mobile-friendly formatting
- [ ] Fast page load
- [ ] No intrusive popups/ads

**How to Fix if FAIL**:
1. Break up long paragraphs
2. Add clear subheadings
3. Use bullet points for scanability
4. Add table of contents for long content
5. Put most important info near top
6. Add FAQ for quick answers

---

## Category 5: Search Engine-First Warning Signs (5 Questions)

**These are RED FLAGS. Answering YES to these questions = FAIL.**

### Q26: Is content primarily made to attract search engine visits (not help people)?

**Google Explicitly States This Is Bad**:
Content created primarily for rankings, not users, violates guidelines.

**How to Evaluate**:
- ✅ **PASS** (good): No, content is genuinely helpful
- ❌ **FAIL** (bad): Yes, content exists only because keyword has search volume

**Red Flags**:
- Content wouldn't exist without keyword research
- Keyword stuffing
- Unnatural keyword placement
- Content created to hit word count
- Multiple thin pages targeting keyword variations

**How to Fix if FAIL**:
1. Consolidate thin pages targeting similar keywords
2. Remove keyword stuffing
3. Rewrite to focus on helping people, not ranking
4. Add genuine utility and expertise

---

### Q27: Are you producing lots of content on many topics hoping some ranks?

**Google Explicitly States This Is Bad**:
Mass content production across topics = low quality signal.

**How to Evaluate**:
- ✅ **PASS** (good): No, content is focused on our core expertise
- ❌ **FAIL** (bad): Yes, we're creating content on many unrelated topics

**Red Flags**:
- Content covers topics outside your expertise
- High volume content production (100+ pages on tangentially related topics)
- Covering topics just because they have search volume

**How to Fix if FAIL**:
1. Focus on your niche
2. Remove off-topic content
3. Quality over quantity
4. Only create content where you have genuine expertise

---

### Q28: Are you mainly summarizing what others say without adding value?

**Google Explicitly States This Is Bad**:
Rewriting competitors = no value.

**How to Evaluate**:
- ✅ **PASS** (good): No, content adds original insights
- ❌ **FAIL** (bad): Yes, content is mostly rewritten from competitors

**Red Flags**:
- No original information
- Just paraphrasing top ranking pages
- No first-hand experience
- No unique data or insights

**How to Fix if FAIL**:
1. Add original research/data
2. Add first-hand experience
3. Add unique insights
4. Don't just rewrite competitors - add something they don't have

---

### Q29: Are you writing to a particular word count because you think Google prefers it?

**Google Explicitly States**: "Are you writing to a particular word count because you've heard or read that Google has a preferred word count? **(No, we don't.)**"

**How to Evaluate**:
- ✅ **PASS** (good): No, content is as long as needed to be helpful
- ❌ **FAIL** (bad): Yes, we're hitting 2,000+ words just because "long content ranks"

**Red Flags**:
- Content padded with filler to hit word count
- Unnecessary repetition
- Generic information added just to make content longer

**How to Fix if FAIL**:
1. Remove filler content
2. Keep content as long as needed - no more, no less
3. Every paragraph should add value
4. Quality > length

---

### Q30: Did you enter a topic area without expertise, just for search traffic?

**Google Explicitly States This Is Bad**:
Creating content in areas you have no expertise = low quality.

**How to Evaluate**:
- ✅ **PASS** (good): No, this is our area of expertise
- ❌ **FAIL** (bad): Yes, we created content outside our expertise for traffic

**Example of FAIL**:
- Locksmith writing about "Best Bluetooth Speakers" (no expertise, just traffic opportunity)
- Plumber writing about "How to Invest in Stocks" (no expertise, off-topic)

**How to Fix if FAIL**:
1. Remove content outside your expertise
2. Focus on your core services
3. Only create content where you have genuine experience

---

## E-E-A-T Scoring & Pass/Fail System

### Scoring Summary

**Category 1: Content Quality & Originality** (8 questions)
- Total possible: 8 points
- Questions: Q1-Q8

**Category 2: Expertise & Experience** (7 questions)
- Total possible: 7 points
- Questions: Q9-Q15

**Category 3: "How" - Content Creation** (4 questions)
- Total possible: 4 points
- Questions: Q16-Q19

**Category 4: "Why" - Purpose** (6 questions)
- Total possible: 6 points
- Questions: Q20-Q25

**Category 5: Search Engine-First Red Flags** (5 questions)
- Total possible: 5 points
- **NOTE**: These are INVERSE scored - YES = 0 points, NO = 1 point
- Questions: Q26-Q30

---

### Pass/Fail Thresholds

**Standard Content** (non-YMYL):
- **PASS**: 24/30 points (80%)
- **NEEDS IMPROVEMENT**: 18-23 points (60-79%)
- **FAIL**: <18 points (<60%)

**YMYL Content** (Your Money or Your Life - health, finance, safety):
- **PASS**: 27/30 points (90%)
- **NEEDS IMPROVEMENT**: 24-26 points (80-89%)
- **FAIL**: <24 points (<80%)

**YMYL Topics Include**:
- Health services, medical advice, medications
- Financial services, investment advice, insurance
- Legal services, contracts, regulations
- Safety services (home security, emergency services, car safety)
- Child safety, parenting advice

---

### E-E-A-T Audit Output Format

```markdown
## E-E-A-T Quality Assurance Audit

**Content**: [Page title/URL]
**Audit Date**: [Date]
**Content Type**: [Service page / Blog post / Location page / Guide]
**YMYL Status**: [Yes/No - is this YMYL content?]

---

### Scoring Summary

| Category | Score | Total Possible | Percentage | Status |
|----------|-------|----------------|------------|--------|
| Content Quality & Originality | [X]/8 | 8 | [X]% | ✅ PASS / ⚠️ PARTIAL / ❌ FAIL |
| Expertise & Experience | [X]/7 | 7 | [X]% | ✅ PASS / ⚠️ PARTIAL / ❌ FAIL |
| Content Creation Process | [X]/4 | 4 | [X]% | ✅ PASS / ⚠️ PARTIAL / ❌ FAIL |
| Content Purpose | [X]/6 | 6 | [X]% | ✅ PASS / ⚠️ PARTIAL / ❌ FAIL |
| Search Engine-First (Red Flags) | [X]/5 | 5 | [X]% | ✅ PASS / ⚠️ PARTIAL / ❌ FAIL |

**TOTAL SCORE**: [X]/30 ([X]%)

**OVERALL STATUS**:
- ✅ **PASS** - Ready to publish
- ⚠️ **NEEDS IMPROVEMENT** - Fix issues before publishing
- ❌ **FAIL** - Major revisions required

---

### Detailed Results

#### Category 1: Content Quality & Originality

**Q1: Original information, research, analysis?**
- Score: [✅ 1.0 / ⚠️ 0.5 / ❌ 0.0]
- Issue: [If FAIL/PARTIAL: describe issue]
- Fix: [If FAIL/PARTIAL: specific remediation steps]

**Q2: Substantial, complete, comprehensive?**
- Score: [✅ 1.0 / ⚠️ 0.5 / ❌ 0.0]
- Issue: [If FAIL/PARTIAL: describe issue]
- Fix: [If FAIL/PARTIAL: specific remediation steps]

[Continue for all 8 questions in category...]

---

#### Category 2: Expertise & Experience

[Continue for all 7 questions...]

---

#### Category 3: "How" - Content Creation

[Continue for all 4 questions...]

---

#### Category 4: "Why" - Purpose

[Continue for all 6 questions...]

---

#### Category 5: Search Engine-First Red Flags

**Q26: Content primarily for search engines?**
- Score: [✅ 1.0 NO / ❌ 0.0 YES]
- Issue: [If YES: describe issue]
- Fix: [If YES: specific remediation steps]

[Continue for all 5 red flag questions...]

---

### Critical Issues (Must Fix Before Publishing)

**CRITICAL** (Score 0.0 on any question):
1. [Issue from Q#]: [Description]
   - **Fix**: [Specific remediation steps]
   - **Priority**: 🔴 CRITICAL
   - **Time to Fix**: [Estimate]

2. [Continue for all critical issues...]

---

### Improvement Opportunities (Partial Scores)

**MEDIUM PRIORITY** (Score 0.5 on questions):
1. [Issue from Q#]: [Description]
   - **Fix**: [Specific remediation steps]
   - **Priority**: 🟠 MEDIUM
   - **Time to Fix**: [Estimate]

2. [Continue for all partial scores...]

---

### Strengths (What's Working Well)

✅ [List questions that scored 1.0]
✅ [What this content does well]
✅ [Trust signals present]
✅ [Expertise demonstrated]

---

### Remediation Priority List

**Fix in this order**:

**Priority 1 (MUST FIX BEFORE PUBLISHING)**:
- [ ] [Critical issue 1] - [Time estimate]
- [ ] [Critical issue 2] - [Time estimate]

**Priority 2 (SHOULD FIX)**:
- [ ] [Medium issue 1] - [Time estimate]
- [ ] [Medium issue 2] - [Time estimate]

**Priority 3 (NICE TO HAVE)**:
- [ ] [Minor issue 1] - [Time estimate]

**Total Time to Fix Critical Issues**: [X] hours
**Total Time to Fix All Issues**: [Y] hours

---

### Recommendation

**IF PASS (24+/30 for standard, 27+/30 for YMYL)**:
✅ **APPROVED FOR PUBLISHING**
- Content meets E-E-A-T standards
- [Optional improvements listed above can be implemented later]

**IF NEEDS IMPROVEMENT (18-23/30 for standard, 24-26/30 for YMYL)**:
⚠️ **REVISIONS REQUIRED BEFORE PUBLISHING**
- Fix Priority 1 issues (critical)
- Consider fixing Priority 2 issues (recommended)
- Estimated time to pass: [X] hours

**IF FAIL (<18/30 for standard, <24/30 for YMYL)**:
❌ **MAJOR REVISIONS REQUIRED - DO NOT PUBLISH**
- Content does not meet Google's helpful content standards
- High risk of algorithmic penalty or poor rankings
- Estimated time to pass: [Y] hours
- Consider: Is this content worth creating? Does it align with business expertise?

---

### Sign-Off

**Audited by**: [Name]
**Date**: [Date]
**Next Review**: [If approved with minor issues - review date]
```

---

## Integration with Workflow Stages

### **Where Stage 6.5 Fits**:

**AFTER**:
- Stage 5: Core Content Creation
- Stage 6: Content Specifications
- Full Page Draft Generator (if used)

**BEFORE**:
- Stage 7: Validation & Testing
- Publishing/implementation

### **Process Flow**:

1. **Content Draft Created** (Stage 5 or Full Page Draft Generator)
2. **E-E-A-T Audit Run** (Stage 6.5) ⬅️ **YOU ARE HERE**
3. **IF PASS**: Proceed to Stage 7
4. **IF FAIL**: Return to drafting, fix issues, re-audit
5. **Only after passing E-E-A-T audit**: Move to implementation

---

## Quality Gate Enforcement

### **Mandatory Rule**:
**NO CONTENT PUBLISHED WITHOUT PASSING E-E-A-T AUDIT**

### **Exception Process**:
If content fails audit but business wants to publish anyway:
1. Document reasons for override
2. Flag content as "High Risk - May Not Rank"
3. Plan re-audit and revision within 30 days
4. Monitor rankings closely

### **Re-Audit Triggers**:
Run E-E-A-T audit again if:
- Content significantly updated
- Every 12 months (content freshness)
- After algorithm updates
- If rankings drop significantly

---

## Agent Execution Instructions

When agent creates content (Drafting Mode, Full Page Draft Generator), it must:

1. **Create content draft**
2. **Self-audit against E-E-A-T framework** (all 30 questions)
3. **Score content** (X/30)
4. **IF SCORE <24 (or <27 for YMYL)**: Identify issues and fix before outputting
5. **Output content WITH E-E-A-T audit results**:
   ```markdown
   [Content here]

   ---

   ## E-E-A-T Quality Assurance

   **Score**: [X]/30 ([X]%)
   **Status**: ✅ PASS / ⚠️ NEEDS IMPROVEMENT / ❌ FAIL

   **Issues Fixed During Drafting**:
   - [Issue 1] → [How it was fixed]
   - [Issue 2] → [How it was fixed]

   **Remaining Issues** (if any):
   - [Issue] → [Recommended fix]

   **Ready to Publish**: [Yes/No]
   ```

6. **Quality Gate**: Do not mark content as "ready to publish" unless it passes E-E-A-T audit

---

## YMYL Content Special Requirements

### **What Qualifies as YMYL**:

**Health & Safety**:
- Medical services, medications, treatments
- Emergency services (locksmith, plumber, electrician if safety-related)
- Home security, child safety
- Nutritional advice, fitness advice

**Financial**:
- Financial services, investment advice
- Insurance, mortgages, loans
- Tax advice, accounting services
- Retirement planning

**Legal**:
- Legal services, legal advice
- Contract services
- Immigration services

**Other**:
- Parenting advice
- Major life decisions (education, career, housing)

### **YMYL Content Requirements** (Higher Bar):

1. **Must Score 27+/30** (90%+) to pass
2. **Must have clear expert authorship**: Full credentials, certifications, qualifications
3. **Must cite medical/financial/legal sources**: Cannot rely on anecdotal evidence alone
4. **Must include disclaimers** if giving advice:
   ```markdown
   **Disclaimer**: This information is for educational purposes only and does not constitute [medical/financial/legal] advice. Consult a qualified [professional] for advice specific to your situation.
   ```
5. **Must be reviewed by qualified professional** (ideally) before publishing
6. **Must be kept up-to-date**: Review every 6 months minimum

### **YMYL Red Flags** (Automatic Fail):

❌ Giving medical advice without medical credentials
❌ Giving financial advice without financial credentials
❌ Giving legal advice without legal credentials
❌ Making health/safety claims without citing sources
❌ Recommending products/services without disclosure of affiliations

---

## E-E-A-T Quick Reference Checklist

**Use this for fast content review**:

### **Trust Signals** (Must Have):
- [ ] Author byline with credentials
- [ ] Author bio or link to about page
- [ ] Business credentials (years in business, certifications, reviews)
- [ ] Sources cited for all data/statistics
- [ ] Contact information visible
- [ ] Professional presentation (no typos, good formatting)

### **Expertise Signals** (Must Have):
- [ ] First-hand experience demonstrated
- [ ] Technical details only expert would know
- [ ] Industry-specific terminology used correctly
- [ ] Common misconceptions corrected
- [ ] Nuances and edge cases addressed

### **Originality** (Must Have):
- [ ] Original insights, not just rewritten from competitors
- [ ] Unique data, research, or case studies
- [ ] "Aha moments" or non-obvious information
- [ ] Substantial value compared to ranking competitors

### **People-First** (Must Have):
- [ ] Genuinely helpful (not just keyword-optimized)
- [ ] Solves real problem
- [ ] Natural language (not keyword stuffed)
- [ ] Complete information (no need to search again)

### **Red Flags** (Must NOT Have):
- [ ] NO keyword stuffing
- [ ] NO content created just for rankings
- [ ] NO mass content production across unrelated topics
- [ ] NO summarizing others without adding value
- [ ] NO writing to hit word count

**Pass Threshold**: All Trust + Expertise + Originality + People-First boxes checked, AND zero Red Flags.

---

**END OF ENHANCEMENT: STAGE 6.5 E-E-A-T QUALITY ASSURANCE**
