# Agent Enhancement: Stage 2.5 - Keyword Priority Analysis

## Integration Point

**Insert AFTER Stage 2 (Framework Definition) and BEFORE Stage 3 (Content Architecture)**

Current flow:
- Stage 0: Intake & Validation
- Stage 1: Strategic Analysis
- Stage 2: Framework Definition
- **→ NEW: Stage 2.5: Keyword Priority Analysis**
- Stage 3: Content Architecture
- Stage 3.5: Page-Level Recommendations
- Stage 4: Detailed Planning
- etc.

---

## Stage 2.5: Keyword Priority Analysis

### Purpose
Identify and prioritize the top 20-30 keywords that will drive 80% of results, map them to specific pages, and create a tracking framework.

### Inputs Required
1. **Current keyword rankings** (from Hike SEO, Google Search Console, or Ahrefs)
2. **Search volumes** (from Ahrefs, keyword tool, or brief)
3. **Competitor keyword gaps** (from Ahrefs content gap analysis)
4. **Existing pages** (from site crawl or brief)

### Mandatory Outputs

#### 1. Top 20 Keyword Priority Table
Format as table with these columns:
- Priority rank (1-20)
- Keyword
- Monthly search volume
- Current position (or "Not ranking")
- Target position
- Gap (positions to move)
- Page URL (which page targets this keyword)
- Action required (optimize existing / create new / maintain)
- Timeline (which week to address)

#### 2. "The Big One" Identification
Identify the single highest-impact keyword or keyword cluster:
- Highest volume currently ranking positions 4-10 (winnable)
- Calculate potential traffic gain if moved to position 1-3
- Calculate potential lead and revenue gain
- Mark as CRITICAL PRIORITY

Example format:
```
THE BIG ONE: Spare Keys Keywords
- Volume: 37,500 monthly searches
- Current position: #5-8
- Potential gain: +15,000-22,500 clicks/month
- Lead gain: +1,500-3,375 leads/month
- Action: Rewrite /spare-keys/ page Week 2
```

#### 3. Keyword-to-Page Mapping
For each priority page (from Stage 3.5 or existing), list:
- Primary keyword (1-2 keywords, highest volume)
- Secondary keywords (2-5 keywords, related)
- Combined search volume
- Current vs potential traffic

Example:
```
Page: /spare-car-keys/
- Primary: Spare Keys For Car (18,100), Spare Keys For Cars (18,100)
- Secondary: Spare Car Keys (1,300), Get Spare Key Made
- Combined volume: 37,500
- Current traffic: ~1,875 clicks/month (5% CTR at #5)
- Potential traffic: 16,875-24,375 clicks/month (45-65% CTR at #1-3)
- Gain: +15,000-22,500 clicks/month
```

#### 4. Top 5 Quick Reference
Distill to the absolute top 5 keywords (80/20 rule):
- These 5 should represent 60-80% of total opportunity
- Typically: 2-3 high-volume low-competition + 2-3 already ranking (move up)
- Clear action for each
- Timeline for each

#### 5. Keyword Priority by Week
Organize keywords by week they should be addressed:
- Week 1: Homepage keywords (foundation)
- Week 2: The Big One
- Week 3: Next highest priority cluster
- Week 4-8: Make/model, location keywords
- Week 9-12: Long-tail, informational keywords

#### 6. Tracking Framework
Specify:
- How to track (Google Search Console filter / Hike / Ahrefs)
- What metrics to check weekly (position changes, clicks from keywords)
- Success targets by timeframe (Week 4: X keywords in top 10, Week 8: Y in top 3)
- Template for weekly keyword report

---

## Instructions for Agent

### When to Execute Stage 2.5

Execute AFTER:
- Stage 1 (Strategic Analysis) - you understand the market and competitors
- Stage 2 (Framework Definition) - you know the strategic approach

Execute BEFORE:
- Stage 3 (Content Architecture) - page structure decisions informed by keyword mapping
- Stage 3.5 (Page-Level Recommendations) - each page recommendation should reference specific keywords

### How to Execute Stage 2.5

**Step 1: Analyze Keyword Data**

From intake form or brief, extract:
- Current ranking keywords with positions (from Hike or GSC data)
- Competitor gap keywords (from Ahrefs content gap analysis)
- Search volumes for all keywords

**Step 2: Calculate Opportunity Score**

For each keyword, calculate opportunity score based on:
- Search volume (higher = better)
- Current position (4-10 = high opportunity, 11-50 = medium, 50+ or not ranking = lower)
- Keyword difficulty (lower = easier win)
- Commercial intent (transactional > commercial > informational)

Formula example:
```
Opportunity Score = (Volume / 100) × Position Factor × Intent Multiplier

Position Factor:
- Position 4-10: 10 points (low-hanging fruit)
- Position 11-20: 5 points
- Position 21-50: 2 points
- Not ranking but competitor ranks: 3 points
- Not ranking, no competitor: 1 point

Intent Multiplier:
- Transactional (buy, get, near me): 1.5x
- Commercial (cost, vs, best): 1.2x
- Informational (how, why, what): 1.0x
```

**Step 3: Identify "The Big One"**

Find the keyword or keyword cluster that:
- Has highest volume (typically 5,000-50,000 searches/month)
- Currently ranks position 4-10 (winnable with optimization)
- Maps to a single page (not split across multiple)

Calculate potential traffic gain:
- Position 5 gets ~5% CTR
- Position 1-3 gets 45-65% CTR
- Traffic gain = (Target CTR - Current CTR) × Volume

**Step 4: Map Keywords to Pages**

For each page in Stage 3.5 recommendations (or existing pages):
- Assign 1-2 primary keywords (highest volume, best fit)
- Assign 2-5 secondary keywords (related, lower volume)
- Calculate combined volume
- Estimate traffic gain if page ranks well

Ensure:
- No keyword cannibalization (same keyword on multiple pages)
- Each page has clear primary focus
- Related keywords cluster logically

**Step 5: Create Priority Rankings**

Rank top 20-30 keywords by:
1. Opportunity score (calculated in Step 2)
2. Strategic importance (does it address customer pain point?)
3. Resource efficiency (can we win this with available effort?)

Group into tiers:
- Priority 1 (Top 5): CRITICAL - highest ROI, focus here first
- Priority 2 (6-10): HIGH - do these Week 3-6
- Priority 3 (11-20): MEDIUM - do these Week 7-12
- Priority 4 (21-30): LOW - nice-to-have, Month 4+

**Step 6: Create Weekly Timeline**

Organize keywords by week based on:
- Stage 3.5 page creation schedule
- Strategic logic (homepage first, then high-value pages, then breadth)
- Resource constraints (don't overload any single week)

Example:
```
Week 1: Homepage keywords (foundation)
- Auto Locksmith Essex (2,500 vol)
- Car Locksmith Essex (1,800 vol)
- Mobile Locksmith Essex (900 vol)

Week 2: The Big One
- Spare Keys For Car (18,100 vol) - CRITICAL
- Spare Keys For Cars (18,100 vol) - CRITICAL

Week 3: Repair cluster
- Car Key Repair (1,600 vol)
- Key Repair For Car (1,600 vol)
- Automotive Key Repair (1,600 vol)
```

**Step 7: Create Tracking Framework**

Specify tools and metrics:
```
Primary Tracking Tool: [Google Search Console / Hike SEO / Ahrefs]

Weekly Metrics to Check:
- Position changes for top 20 keywords
- Click volume from top 20 keywords
- Impressions (visibility)
- CTR trends

Success Targets:
- Week 4: 5+ keywords in top 10
- Week 8: 8+ keywords in top 10, 3+ in top 3
- Week 12: 15+ keywords in top 10, 8+ in top 3

Monthly Review Questions:
- Which keywords moved up? Why?
- Which keywords didn't move? What can we do differently?
- Are we seeing traffic gains proportional to position improvements?
- Should we adjust priorities based on what's working?
```

---

## Output Format Template

Use this template structure for Stage 2.5 output:

```markdown
# Stage 2.5: Keyword Priority Analysis
## [Business Name] - Top Keywords to Win

**Date**: [Date]
**Purpose**: Prioritize highest-impact keywords and map to pages
**Impact**: Top 20 keywords = X monthly searches, potential for Y-Z clicks/month

---

## THE BIG ONE: [Keyword or Cluster Name]

[If one keyword/cluster dominates opportunity]

| Keyword | Volume | Current Position | Target Position | Page |
|---------|--------|------------------|-----------------|------|
| [Keyword 1] | [Vol] | #[Pos] | #1-3 | [URL] |
| [Keyword 2] | [Vol] | #[Pos] | #1-3 | [URL] |

**Total Volume:** X monthly searches
**Current Traffic:** ~X clicks/month (X% CTR at position #X)
**Potential Traffic:** X-Y clicks/month (45-65% CTR at position #1-3)
**Traffic Gain:** +X-Y clicks/month
**Lead Gain:** +X-Y leads/month (at 10-15% conversion)
**Revenue Gain:** £X-Y/month (at £X average job)

**Action Required:**
- [Specific action, e.g., "Rewrite spare keys page to 2,500 words"]
- [Timeline, e.g., "Week 2"]

**This is your #1 priority.**

---

## Top 20 Keywords by Priority

### Priority 1: Keywords You Already Rank For (Optimize Existing)

[Table with 5-10 keywords currently ranking positions 4-20]

| # | Keyword | Volume | Current Pos | Target Pos | Page | Action |
|---|---------|--------|-------------|------------|------|--------|
| 1 | [Keyword] | [Vol] | #[Pos] | #1-3 | [URL] | [Action] |
| 2 | [Keyword] | [Vol] | #[Pos] | #1-3 | [URL] | [Action] |

**Combined Volume:** X searches/month
**Current Est. Traffic:** ~X clicks/month
**Potential Traffic:** ~X-Y clicks/month
**Traffic Gain:** +X-Y clicks/month

---

### Priority 2: High-Volume Keywords You DON'T Rank For (Content Gap)

[Table with 5-10 keywords not ranking or ranking 50+]

| # | Keyword | Volume | Current Pos | Target Pos | Page Needed | Action |
|---|---------|--------|-------------|------------|-------------|--------|
| [N] | [Keyword] | [Vol] | Not ranking | #1-10 | [URL] | [Action] |

**Combined Volume:** X searches/month
**Current Traffic:** 0 clicks/month
**Potential Traffic:** X-Y clicks/month
**Traffic Gain:** +X-Y clicks/month

---

### Priority 3: Make/Model or Niche Keywords (Medium Priority, High Value)

[If applicable - specialty keywords with lower volume but higher value customers]

---

### Priority 4: Location Keywords (Local Priority)

[If local business - location-based keywords]

---

## Keyword Mapping to Pages (Summary)

### Homepage (/) - Target Keywords:
- Primary: [Keyword 1], [Keyword 2]
- Secondary: [Keyword 3], [Keyword 4], [Keyword 5]
- Combined Volume: [X]
- Potential Traffic: [X-Y] clicks/month

### [Page 2 Name] ([URL]) - Target Keywords:
- Primary: [Keyword 1], [Keyword 2]
- Secondary: [Keyword 3], [Keyword 4]
- Combined Volume: [X]
- Potential Traffic: [X-Y] clicks/month

[Repeat for all priority pages]

---

## Keyword Priority by Week

### Week 1: [Theme, e.g., "Homepage/Foundation Keywords"]
- [Keyword 1] ([Vol])
- [Keyword 2] ([Vol])
**Action:** [What to do]

### Week 2: [Theme, e.g., "The Big One"]
- [Keyword 1] ([Vol])
- [Keyword 2] ([Vol])
**Action:** [What to do]

[Continue for 12 weeks]

---

## Quick Reference: Top 5 Keywords to Win

If you only focus on 5 keywords, make it these:

| Priority | Keyword | Volume | Current | Target | Page | Why Critical |
|----------|---------|--------|---------|--------|------|--------------|
| 🔴 #1 | [Keyword] | [Vol] | #[Pos] | #1-3 | [URL] | [Reason] |
| 🔴 #2 | [Keyword] | [Vol] | #[Pos] | #1-3 | [URL] | [Reason] |
| 🟠 #3 | [Keyword] | [Vol] | #[Pos] | #1-3 | [URL] | [Reason] |
| 🟠 #4 | [Keyword] | [Vol] | #[Pos] | #1-3 | [URL] | [Reason] |
| 🟠 #5 | [Keyword] | [Vol] | #[Pos] | #1-3 | [URL] | [Reason] |

**Total Volume:** X searches/month (X% of total top 20 volume)
**Current Traffic:** ~X clicks/month
**Potential Traffic:** ~X-Y clicks/month
**Traffic Gain:** +X-Y clicks/month

**Focus on these 5 and you'll achieve 80% of the results.**

---

## Tracking Progress

### Metrics to Monitor Weekly:

**Primary Tool:** [Google Search Console / Hike SEO / Ahrefs]

**Weekly Check:**
- Track these 20 keywords specifically
- Monitor position changes
- Check clicks from these keywords
- Note any new keywords appearing

**Target Positions by Timeline:**

| Timeframe | Keywords in Top 3 | Keywords in Top 10 | Total Traffic from Top 20 |
|-----------|-------------------|-------------------|---------------------------|
| Week 0 (Now) | [X] | [Y] | ~[Z] clicks/month |
| Week 4 | [X] | [Y] | ~[Z] clicks/month |
| Week 8 | [X] | [Y] | ~[Z] clicks/month |
| Week 12 | [X] | [Y] | ~[Z] clicks/month |

---

## Summary: The Numbers

**Top 20 Keywords Total:**
- **Total Volume:** X searches/month
- **Current Traffic:** ~X clicks/month (X% of potential)
- **Potential Traffic:** X-Y clicks/month (if all rank top 3-10)
- **Traffic Gain:** +X-Y clicks/month
- **Lead Gain:** +X-Y leads/month (at 10-15% conversion)
- **Revenue Gain:** £X-Y/month (at £X average job)

**The Big [N] Keywords Alone:**
- **Total Volume:** X searches/month
- **Potential Traffic:** X-Y clicks/month
- **X% of total impact from Y% of keywords**

**Prioritization = Everything. Focus on the top 5 first.**

---

## Where This Goes

### For Business Owner:
- Include in Executive Report (Page 3)
- Reference in progress meetings
- Use to explain page creation priorities

### For Content Writer:
- Review before writing each page
- Optimize content for primary + secondary keywords
- Include primary keyword in H1, first 100 words, 2-3 H2s

### For Technical SEO:
- Use for title tag optimization
- Use for meta description writing
- Use for internal linking anchor text

### For Tracking:
- Set up rank tracking for all keywords
- Create weekly keyword report
- Monitor movement and adjust strategy

---

**END OF STAGE 2.5 OUTPUT**
```

---

## Integration with Other Stages

### Stage 3 (Content Architecture) - Uses Stage 2.5 Output:
- Site structure informed by keyword clusters
- Hub/spoke model based on primary vs secondary keywords
- Internal linking strategy uses keyword mapping

### Stage 3.5 (Page-Level Recommendations) - Uses Stage 2.5 Output:
- Each page recommendation references specific keywords from Stage 2.5
- Decision rationales include keyword opportunity data
- Priority ranking influenced by keyword potential traffic

Example integration in Stage 3.5:
```markdown
### Page 1: Spare Keys Page Optimization

**Decision Rationale:**
- **Keyword opportunity (Stage 2.5):** Currently ranks #5 for "Spare Keys For Car" (18,100 vol) + "Spare Keys For Cars" (18,100 vol) = 36,200 combined monthly searches
- **Traffic potential:** Position #5 → #1-3 = +15,000-22,500 clicks/month
- **Lead potential:** +1,500-3,375 leads/month
- [Rest of rationale...]
```

### Stage 4 (30/60/90 Roadmap) - Uses Stage 2.5 Output:
- Week-by-week plan organized around keyword priorities
- Success metrics tied to keyword position improvements

---

## Quality Checks for Agent

Before finalizing Stage 2.5 output, verify:

- [ ] "The Big One" is clearly identified (highest-impact opportunity)
- [ ] Top 20 keywords represent at least 80% of realistic opportunity
- [ ] Each keyword is mapped to exactly ONE primary page (no cannibalization)
- [ ] Keywords organized by week align with page creation schedule (Stage 4)
- [ ] Top 5 Quick Reference truly captures 60-80% of impact
- [ ] Tracking framework is specific (not generic "monitor rankings")
- [ ] Potential traffic numbers are realistic (use CTR benchmarks by position)
- [ ] Revenue projections use client's actual average job value

---

## Agent Prompt Addition

Add to `agent_system_prompt.md` in the Workflow section:

```markdown
### Stage 2.5: Keyword Priority Analysis (MANDATORY)

**Purpose:** Identify top 20-30 keywords that drive 80% of results, map to pages, create tracking framework

**Inputs:** Current rankings, search volumes, competitor gaps, existing pages

**Outputs:**
1. Top 20 keyword priority table (with volumes, positions, pages, actions)
2. "The Big One" identification (highest-impact single opportunity)
3. Keyword-to-page mapping (which page targets which keywords)
4. Top 5 quick reference (80/20 rule)
5. Keyword priority by week (timeline)
6. Tracking framework (tools, metrics, targets)

**Execute AFTER:** Stage 2 (Framework Definition)
**Execute BEFORE:** Stage 3 (Content Architecture)

**Why critical:** Without clear keyword priorities, page creation is unfocused. This stage ensures every page targets specific, high-value keywords with realistic traffic projections.

**Quality gate:** Must identify "The Big One" (highest single opportunity) and Top 5 keywords (80% of impact).
```

---

## Example Usage in Next Strategy Run

**User provides:**
- "I have 61 keywords ranking from Hike"
- "Ahrefs shows 1,625 keyword gap"
- "Current traffic: 159 clicks/month"

**Agent executes:**
- Stage 0: Validates data
- Stage 1: Analyzes competitors
- Stage 2: Defines framework
- **Stage 2.5: Analyzes 61 + 1,625 keywords, identifies top 20, maps to pages, creates tracking framework**
- Stage 3: Designs site architecture (informed by keyword clusters)
- Stage 3.5: Recommends 25 pages (each referencing keywords from Stage 2.5)
- Stage 4: Creates 30/60/90 roadmap (organized by keyword priorities)

**Output includes:** KEYWORD_PRIORITIES_TOP_20.md automatically generated, integrated into all subsequent stages

---

**END OF AGENT ENHANCEMENT DOCUMENT**
