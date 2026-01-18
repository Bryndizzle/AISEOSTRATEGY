# Prompt 9: Jobs to be Done Framework + Keyword Intent Mapping

## Purpose
Map customer jobs to search intent and create a comprehensive keyword strategy with 100-200 keywords organized by search intent, buyer journey stage, and the 4-layer growth model.

## Inputs Required
- Business fundamentals (from Prompt 1)
- Reddit research verbatim language (from Prompt 7)
- Ahrefs content gap analysis (from Prompt 6)
- HikeSEO keyword tracking data (from Prompt 5)
- Competitive analysis (from Prompt 4)
- Strategy document framework (from Prompt 8)

## Data Sources
- **HikeSEO**: Existing keyword tracking, search volume data
- **Ahrefs**: Keyword Explorer, competitor keyword rankings
- **Reddit**: Customer verbatim language, unmet needs
- **Intake form**: Target audience, commercial context

## Jobs to be Done Framework

### Customer Job Mapping
For each primary customer job, identify:

1. **Functional Job**: What practical task is the customer trying to accomplish?
2. **Emotional Job**: How does the customer want to feel?
3. **Social Job**: How does the customer want to be perceived?

### Search Intent Mapping
Map each job to search intent categories:

| Customer Job | Search Intent | Example Queries | Journey Stage |
|--------------|--------------|-----------------|---------------|
| [Job 1] | Informational | [Query 1], [Query 2] | Awareness |
| [Job 2] | Commercial | [Query 3], [Query 4] | Consideration |
| [Job 3] | Transactional | [Query 5], [Query 6] | Decision |

## Keyword Research & Intent Mapping

### Target: 100-200 Keywords

Organize keywords across 4 dimensions:

#### 1. By Search Intent
- **Informational** (40-50 keywords): "how to", "what is", "guide to"
- **Commercial** (30-40 keywords): "best", "vs", "review", "comparison"
- **Transactional** (20-30 keywords): "buy", "hire", "near me", service terms
- **Navigational** (10-15 keywords): Brand terms, location + service

#### 2. By 4-Layer Growth Model
- **Layer 1 - Foundation** (15-20 keywords): Core service terms, brand + location
- **Layer 2 - High-Intent** (30-40 keywords): Commercial intent, ready-to-buy
- **Layer 3 - Authority** (40-50 keywords): Thought leadership, expertise signals
- **Layer 4 - Awareness** (20-30 keywords): Top-of-funnel, educational

#### 3. By Customer Journey Stage
- **Awareness** (30-40%): Problem recognition, education
- **Consideration** (30-40%): Solution comparison, evaluation
- **Decision** (20-30%): Purchase intent, ready to convert

#### 4. By Priority (Impact vs Difficulty)
- **Quick Wins** (High impact, Low difficulty): Target first
- **Major Projects** (High impact, High difficulty): Strategic focus
- **Fill-ins** (Low impact, Low difficulty): Content padding
- **Time Sinks** (Low impact, High difficulty): Avoid

## Output Format

### 1. JTBD Summary Table
```
| Customer Segment | Functional Job | Emotional Job | Social Job | Primary Search Queries |
|------------------|----------------|---------------|------------|------------------------|
| [Segment 1] | [Job] | [Feeling] | [Perception] | [5-7 queries] |
```

### 2. Master Keyword Table
Export as table with columns:
- **Keyword**: Exact match phrase
- **Search Volume**: Monthly average (UK or specified geo)
- **Keyword Difficulty**: 0-100 score
- **Search Intent**: Info/Commercial/Transactional/Nav
- **JTBD**: Which customer job does this serve?
- **Journey Stage**: Awareness/Consideration/Decision
- **Layer**: Foundation/High-Intent/Authority/Awareness
- **Priority**: Quick Win/Major Project/Fill-in/Time Sink
- **Current Ranking**: Position if tracked
- **Competitor Ranking**: Best competitor position
- **Opportunity Score**: Custom scoring (volume × intent × winnability)

### 3. Keyword Clusters
Group keywords into topic clusters:

**Cluster Name**: [Topic]
- **Pillar Keyword**: [Main term]
- **Supporting Keywords** (8-12): [List]
- **Content Type**: Pillar page, blog series, landing page
- **Priority**: 1-5

### 4. Search Intent Distribution Chart
Visual breakdown:
- X% Informational
- X% Commercial
- X% Transactional
- X% Navigational

### 5. JTBD → Keyword Mapping
For each customer job:

**Job**: [Customer trying to accomplish X]
**Verbatim Language** (from Reddit): "[Exact customer quote]"
**Search Queries**:
- Informational: [5-7 queries]
- Commercial: [3-5 queries]
- Transactional: [2-3 queries]

**Content Needed**:
- [Content type 1]: Target "[keyword cluster]"
- [Content type 2]: Target "[keyword cluster]"

## Integration with Strategy Document

### Map to 4-Layer Model
Ensure keyword strategy aligns with Prompt 8 framework:
- **Layer 1 keywords** → On-site optimisation priorities
- **Layer 2 keywords** → Conversion-focused landing pages
- **Layer 3 keywords** → Authority content, thought leadership
- **Layer 4 keywords** → Top-of-funnel blog content

### AI Visibility Keywords
Flag keywords likely to trigger AI answer engines:
- Question-based queries → FAQ schema opportunities
- "Best" / "Top" lists → List schema opportunities
- Comparison queries → Structured data opportunities

## Success Criteria

This prompt is complete when you have:
- [x] Mapped 3-7 primary customer jobs to search intent
- [x] Identified 100-200 keywords with full metadata
- [x] Organized keywords by intent, journey stage, layer, priority
- [x] Created 8-15 keyword clusters with pillar + supporting terms
- [x] Connected JTBD to specific keyword groups
- [x] Flagged quick wins (high impact, low difficulty)
- [x] Identified content gaps where customer jobs lack keyword coverage
- [x] Provided verbatim customer language for each job (from Reddit)

## Assumptions to Label

- [ASSUMPTION: Search volume data is UK-based unless intake specifies different geography]
- [ASSUMPTION: Keyword difficulty from Ahrefs unless HikeSEO provides alternative]
- [ASSUMPTION: Priority based on business goal from intake - if goal is leads, prioritize transactional/commercial intent]
- [ASSUMPTION: If Reddit data unavailable, infer customer language from industry norms]

## Cross-References
- Use this keyword map in **Prompt 10** (Copy Examples & Content Titles)
- Feed priority keywords into **Prompt 12** (Implementation Task Breakdown)
- Validate keyword strategy supports challenge from **Intake Section 1**
