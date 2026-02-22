# EPTDESIGN: Strategic Analysis & Competitive Diagnostic

**Document Type:** Evidence Layer — Detailed Analysis
**Prepared for:** Alison Spicer / Internal Strategy Use
**Date:** February 2026
**Status:** Primary Reference Document

---

## Document Purpose

This document provides the full evidence base for EPTDESIGN's search and AI visibility strategy. It is structured as an audit-first analysis: each section establishes the current state with specific data, then draws strategic implications. Where data has been sourced from external tools (Ahrefs, Google Search, GBP audit) the source is noted. Where values are estimated or interpolated, they are marked **[ASSUMPTION: ...]**.

---

## Section 1: Current Visibility Audit

### 1.1 Brand vs Non-Brand vs Project Search Performance

The fundamental measure of a firm's digital visibility is whether it appears in searches conducted by people who do not already know its name. Brand searches (e.g., "EPT Design" or "EPTDESIGN Pasadena") test recall and direct navigation. Non-brand searches (e.g., "landscape architect Pasadena" or "landscape architecture firm Southern California") test discoverability — the ability to enter a buyer's consideration set for the first time.

**Brand Search Performance**

| Search Query | Current Result |
|---|---|
| "EPTDESIGN" | Website appears in position 1; LinkedIn, Yelp appear below |
| "EPT Design Pasadena" | Website appears; social profiles below |
| "EPT Design landscape architecture" | Website appears |
| "Bob Eriksson landscape architect" | Fragmented; no dedicated EPT page appears prominently |
| "Nord Eriksson FASLA" | **[ASSUMPTION: Limited results; no dedicated profile page on eptdesign.com indexed]** |
| "Scott Horsley landscape architect" | **[ASSUMPTION: No dedicated profile page; not appearing in search results]** |

Brand search performance is adequate for someone who already knows the firm exists. It does not extend to the firm's principals as named experts, which is a significant missed opportunity given Nord Eriksson's national press coverage.

**Non-Brand Search Performance**

| Search Query | Current EPTDESIGN Result | Who Ranks Instead |
|---|---|---|
| "landscape architect Pasadena" | Not ranking | June Scott Design, Ecocentrix, Wild Bloom |
| "landscape architect Irvine CA" | Not ranking | Local generalist firms |
| "landscape architecture firm Southern California" | Not ranking | Sasaki, SWA Group, MLA |
| "landscape architect Los Angeles estate" | Not ranking | **[ASSUMPTION: Boutique residential firms; AHBE]** |
| "landscape architect healthcare California" | Not ranking | **[ASSUMPTION: AHBE, MIG, national healthcare-specialist firms]** |
| "LEED landscape architect California" | Not ranking | **[ASSUMPTION: General results; no EPT presence]** |
| "landscape architecture firm Claremont" | Not ranking | **[ASSUMPTION: No dedicated firm pages in this geography]** |
| "landscape architecture San Diego" | Not ranking | Local San Diego firms |
| "landscape architecture Santa Barbara" | Not ranking | Local Santa Barbara firms |

EPTDESIGN achieves zero non-brand ranking. This is the core visibility problem. The firm cannot enter a client's consideration set through search at any phase of the research process.

**Project Search Performance**

| Search Query | Current Result |
|---|---|
| "Cedars-Sinai landscape design" | AHBE Landscape Architects ranks; EPTDESIGN does not appear |
| "UCLA landscape architecture" | UCLA itself, academic results; no EPT attribution |
| "Google Venice campus landscape" | General press coverage; EPT not attributed |
| "Kaiser Permanente landscape design" | **[ASSUMPTION: Kaiser internal pages, general results; no EPT]** |
| "Pomona College landscape" | Pomona College website; no EPT attribution |
| "Trammell Crow landscape California" | **[ASSUMPTION: Developer-focused results; no EPT attribution]** |

The Cedars-Sinai attribution loss to AHBE is the most acute example of competitive project displacement. EPTDESIGN completed work for Cedars-Sinai; another firm now appears in search results associated with that project name. This is not a minor inconvenience — it represents direct competitor benefit from EPTDESIGN's own project portfolio.

**Summary Metrics**

| Metric | Value | Source |
|---|---|---|
| Domain Rating | 29 | Ahrefs |
| Organic Keywords (ranking) | 0 | Ahrefs |
| Estimated Organic Traffic | 0 | Ahrefs |
| Referring Domains | **[ASSUMPTION: Low; <50 quality referring domains]** | Ahrefs estimate |
| Indexed Pages | 87 project pages + core site pages | Site audit |
| Last Project Page Update | July 2021 | Site audit |

---

## Section 2: The Three Root Causes of Zero Organic Visibility

### 2.1 Root Cause One — AI Crawlers Are Actively Blocked

This is the most structurally significant finding in the audit. EPTDESIGN's Cloudflare configuration blocks every major AI crawler via the robots.txt file. This is almost certainly a default Cloudflare security setting that was never reviewed or intentionally configured. The effect is total: no AI system is permitted to read the website.

**Blocked Crawlers Confirmed**

| Crawler | Platform Affected | Impact |
|---|---|---|
| GPTBot | ChatGPT (OpenAI) | Zero citations in ChatGPT responses |
| ClaudeBot | Claude / Anthropic | Zero citations in Claude responses |
| Google-Extended | Google AI Overviews, Gemini | Zero citations in Google AI features |
| Applebot-Extended | Apple Intelligence | Zero citations in Apple AI |
| meta-externalagent | Meta AI | Zero citations in Meta AI products |
| CCBot | Common Crawl (used by multiple AI systems) | Excluded from training data pipelines |
| Bytespider | ByteDance AI products | Zero citations in those platforms |

This configuration does not affect traditional Google Search crawling (Googlebot is separate and is not blocked). It exclusively affects AI systems. The practical consequence is that no matter how good EPTDESIGN's website content becomes, no AI assistant will reference the firm based on website content alone.

**What Unblocking Achieves**

When AI crawlers are permitted access, they index the firm's content and incorporate it into citation models. For a firm with EPTDESIGN's credentials — FASLA designation, LEED Platinum, named institutional clients, 64-year history — the underlying content is strong enough to generate citations once crawlers can read it. The blocker is not quality; it is access.

The fix is a single change to the robots.txt configuration. It can be implemented in hours. It is the prerequisite for all AI visibility work.

**Recommended robots.txt Change**

The current configuration contains explicit `Disallow: /` rules for each AI crawler user-agent. These lines must be removed or changed to `Allow: /`. The remainder of the robots.txt can remain unchanged. This change should be reviewed by the web development team to confirm no other Cloudflare security rules replicate the block at a different layer.

### 2.2 Root Cause Two — No Service Pages Exist

EPTDESIGN's website presents its work through a filtered portfolio view at `/work/`. The five sectors — Residences, Commercial/Retail, Education/Healthcare, Housing/Mixed Use, Parks/Civic — exist as filtering categories. There are no dedicated pages for any sector, any geography, or any service type.

**Why This Matters for Search**

Search engines rank pages, not websites. When Google determines which firm to show for "landscape architecture healthcare California," it looks for a page that makes the case for that specific query — one that explains the firm's work in healthcare landscapes, names relevant projects, cites credentials, and demonstrates geographic relevance. A filtered project portfolio provides none of this. It provides images and project names. That is not indexable content in the structured sense that search engines require.

**Why This Matters for AI**

AI citation systems work similarly. When ChatGPT or Perplexity generates a recommendation for "landscape architects specialising in university campus design," it draws on indexed content that explicitly establishes expertise in that area. A firm without a "Higher Education" or "University Campuses" page cannot be cited for that category, regardless of how many university projects it has completed.

**The Structural Gap**

| Content Type | Should Exist | Currently Exists |
|---|---|---|
| Sector landing page: Residences (Estate) | Yes | No |
| Sector landing page: Commercial/Retail | Yes | No |
| Sector landing page: Education/Healthcare | Yes | No |
| Sector landing page: Housing/Mixed Use | Yes | No |
| Sector landing page: Parks/Civic | Yes | No |
| Location page: Pasadena studio | Yes | No |
| Location page: Irvine studio | Yes | No |
| Location page: Claremont studio | Yes | No |
| Location page: Santa Barbara studio | Yes | No |
| Location page: San Diego studio | Yes | No |
| Principal profile: Scott Horsley | Yes | No |
| Principal profile: Nord Eriksson FASLA | Yes | No |
| Principal profile: Stephen Carroll ASLA LEED AP | Yes | No |
| Principal profile: Dan Hoon | Yes | No |
| Principal profile: Ross Woodley | Yes | No |
| Firm history/lineage page | Yes | No |
| Awards page with structured data | Yes | No |

Fifteen to twenty pages of structured content that should exist do not. Each absent page is an absent ranking opportunity and an absent AI citation pathway.

### 2.3 Root Cause Three — Entity Fragmentation

In the language of search and AI systems, an "entity" is the structured identity model that a platform builds for an organisation. It is assembled from every consistent data signal across the web: the name, address, phone number, description, founding year, principal names, sector affiliations, geographic footprint, and third-party mentions. The more consistent and reinforced these signals are, the higher the entity's confidence score — and the more readily it surfaces in search and AI.

EPTDESIGN's entity is fragmented. Multiple conflicting data points are in circulation, which suppresses the firm's confidence score across all platforms.

**Documented Fragmentation Issues**

| Data Point | Issue |
|---|---|
| Pasadena address | Three different addresses in active circulation across directories and listings |
| Website address | Does not match the address most commonly listed elsewhere |
| Studio locations | Solana Beach listed (not a current studio location; current studios are Pasadena, Irvine, Claremont, Santa Barbara, San Diego) |
| Firm description | Inconsistent or absent across GBP, LinkedIn, Yelp, Houzz |
| Founding year | Not consistently cited; 1962 not anchored in metadata |
| ESOP status | Not mentioned in any indexable location |
| FASLA credential (Nord Eriksson) | Not surfaced in entity data |

**The Compounding Effect**

Each inconsistency is a signal that reduces the entity's authority score. Google's knowledge graph, and the data models used by AI citation systems, penalise conflicting signals because they indicate the entity is either poorly managed or genuinely ambiguous. A firm with three addresses is treated with less certainty than a firm with one consistent address replicated across 30+ directories. The SEO impact of NAP fragmentation is well-documented and disproportionately large relative to the effort required to fix it.

---

## Section 3: Competitor Benchmark

### 3.1 Sasaki — The Anatomy of AI-Visible Authority

Sasaki is the correct benchmark for EPTDESIGN's ambitions. They are not the same type of firm — Sasaki operates at larger institutional scale with an international footprint — but they represent what a landscape architecture and planning firm looks like when it has made the structural digital investments that EPTDESIGN has not yet made.

**Comparative Metrics**

| Metric | EPTDESIGN | Sasaki |
|---|---|---|
| Domain Rating | 29 | 70 |
| Organic Keywords | 0 | Significant (estimated 500+) |
| AI Citations | 0 | 88 |
| Dedicated Sector Pages | 0 | Full architecture |
| People/Principal Pages | 0 | Full directory |
| Geographic Coverage Pages | 0 | Multiple |
| GBP Reviews | 5 (5 locations) | N/A |

**Sasaki's Sector Page Architecture**

Sasaki's website features dedicated sector pages that function as standalone landing pages for each practice area. Each page includes:

- A clear positioning statement for the sector
- Named methodology or approach
- Representative projects with descriptions
- Principal or team lead attribution
- Credential and award callouts relevant to that sector
- Geographic scope statements

These pages rank for sector + geography queries. They are the mechanism by which Sasaki appears when an institutional client searches for "landscape architect healthcare" or "campus planning firm." They are also the mechanism by which AI systems can cite Sasaki for sector-specific queries — because the content explicitly establishes expertise in a crawlable, structured format.

**Sasaki's People Pages**

Every principal at Sasaki has a dedicated profile page. These pages include biography, sector specialisations, credentials (FASLA, ASLA, LEED, etc.), named projects, and publications or press mentions. Principal pages serve two functions:

1. They rank for named-expert searches (e.g., a client who heard of a specific designer)
2. They establish the entity's authority signals by connecting the firm's name to credential terms (FASLA, LEED Platinum) and project names that AI systems can cross-reference

EPTDESIGN has no principal profile pages. Nord Eriksson FASLA — who has been featured in Veranda and Martha Stewart Living — has no indexed profile on eptdesign.com. This is a significant suppression of a genuine authority signal.

**What 88 AI Citations Means in Practice**

When a client uses ChatGPT, Perplexity, Gemini, or Google's AI Overview to ask a landscape architecture question — "who are the best landscape architecture firms for university campuses on the East Coast," "which firms specialise in healthcare landscape design," "what landscape firms work with major developers" — Sasaki's name appears in the generated response 88 times across these platforms.

Each citation is an impression in front of a high-intent buyer in their research phase. EPTDESIGN receives zero such impressions. Over a year, across thousands of queries, this represents a structural advantage in mental availability that compounds over time.

### 3.2 Studio-MLA — Social Authority Benchmark

Studio-MLA is relevant as a benchmark for LinkedIn visibility and social authority, particularly for the Los Angeles landscape architecture market.

| Metric | EPTDESIGN | Studio-MLA |
|---|---|---|
| LinkedIn Followers | 2,354 | 4,663 |
| Posting Frequency | **[ASSUMPTION: Low; irregular]** | Regular |
| Content Type | **[ASSUMPTION: Project images]** | Projects + thought leadership |

The follower gap (2,354 vs 4,663) is notable less as a vanity metric and more as an indicator of the firm's reach into the professional and client networks that use LinkedIn as a research tool. Commercial real estate developers, university facilities directors, and healthcare system administrators who are evaluating landscape architecture firms frequently check LinkedIn to assess firm credibility, size, and recent work. A follower count of 2,354 relative to peers reduces perceived scale.

### 3.3 AHBE Landscape Architects — Project Attribution Displacement

AHBE Landscape Architects is ranking for search queries associated with EPTDESIGN's Cedars-Sinai project. This is not a direct citation error (AHBE did not claim the project); it is a consequence of EPTDESIGN's project content being invisible to search engines while AHBE's content is indexed and optimised.

The mechanism: when Google processes a search for "Cedars-Sinai landscape" or related queries, it returns the most relevant indexed content. AHBE has sector pages for healthcare landscape architecture, indexed project content, and structured content that establishes expertise in this area. EPTDESIGN has a project image in a portfolio filter. Google surfaces AHBE.

The implication is not that AHBE has done anything wrong. It is that EPTDESIGN's actual project work is generating zero search presence while a competitor benefits from proximity to the same institutional name.

This pattern almost certainly extends to other EPTDESIGN clients — Kaiser Permanente, UCLA, Pomona College — where the firm's project work is unrepresented in search results and competitors fill the gap.

### 3.4 Local Competitors Ranking for Primary Geography Terms

The following firms rank for searches that EPTDESIGN should dominate by virtue of its 64-year Pasadena presence, five Southern California studios, and institutional client roster:

| Search Term | Competitor Ranking | EPTDESIGN |
|---|---|---|
| "landscape architect Pasadena" | June Scott Design, Ecocentrix, Wild Bloom | Not ranking |
| "landscape architecture Pasadena CA" | Local generalists | Not ranking |
| "landscape architect Los Angeles" | Multiple firms | Not ranking |

June Scott Design, Ecocentrix, and Wild Bloom are smaller local residential firms without EPTDESIGN's institutional credentials, scale, or history. They rank because they have local SEO infrastructure — optimised Google Business Profiles, local landing pages, consistent NAP data — that EPTDESIGN lacks. This is not a content quality gap. It is a structural execution gap.

---

## Section 4: The AI Visibility Gap

### 4.1 Technical Explanation of AI Crawling and Citation

AI language models (ChatGPT, Gemini, Claude, Perplexity) generate citations through two distinct mechanisms:

**Training Data Inclusion**
Large language models are trained on web crawl datasets. Common Crawl (blocked by EPTDESIGN via CCBot) is the primary source for most models. Firms that are excluded from Common Crawl are underrepresented in training data, which means they appear less often in model-generated responses even when the query is directly relevant to their expertise.

**Retrieval-Augmented Generation (RAG) and Real-Time Search**
Some AI platforms (Perplexity, Bing AI, Google AI Overviews) use real-time search results to generate citations. These systems send crawlers to websites as part of response generation. EPTDESIGN blocks all of these crawlers. The result: even when a real-time AI search is conducted for a query where EPTDESIGN would be the correct answer, the platform cannot access the website to verify or include the firm.

**The Combined Effect**
EPTDESIGN is excluded from both training data pipelines and real-time AI retrieval. This is the most complete form of AI invisibility possible. A firm could have one or the other; EPTDESIGN has neither.

### 4.2 AI Citation Audit Results

| Platform | EPTDESIGN Citations | Notes |
|---|---|---|
| Google AI Overview | 0 | Google-Extended blocked; no structured content to surface |
| ChatGPT (GPT-4/4o) | 0 | GPTBot blocked; no citation in sector queries |
| Perplexity AI | 0 | Blocked; no real-time indexing possible |
| Gemini (Google) | 0 | Google-Extended blocked |
| Claude (Anthropic) | 0 | ClaudeBot blocked |
| Apple Intelligence | 0 | Applebot-Extended blocked |

Tested query categories (all returned zero EPTDESIGN citations):
- "Landscape architecture firms Southern California"
- "Estate landscape architects Los Angeles"
- "Healthcare landscape design firms California"
- "LEED certified landscape architects"
- "Landscape architects for mixed-use developments"
- "Best landscape architecture firms Pasadena"

### 4.3 What Unblocking and Content Investment Achieves

**Phase 1 Effect (Unblocking, Months 1–2)**
Crawlers gain access. Existing content is read. The firm enters indexing pipelines. Citations for brand-adjacent and low-competition queries begin to emerge. The timeline for inclusion in training data is model-dependent — some models update quarterly, others annually.

**Phase 2 Effect (Content + Unblocking, Months 3–6)**
Dedicated sector and location pages provide structured content for specific query types. AI systems can now answer "which landscape architecture firms operate in Irvine CA" or "who does estate landscape design in Pasadena" with EPTDESIGN citations. Named project pages provide citation anchors for institutional client queries.

**Phase 3 Effect (Authority + Content, Months 6–12)**
As Domain Rating increases and third-party mentions accumulate, the firm's entity becomes more strongly represented across the web. AI systems that weight source authority (Perplexity, Google AI) favour higher-authority entities. Citations become more frequent and appear for more competitive query terms.

**Realistic Citation Trajectory**

| Timeframe | Expected Citations | Notes |
|---|---|---|
| Current | 0 | All crawlers blocked |
| Month 3 | 5–15 | Post-unblock; brand and low-competition queries |
| Month 6 | 20–35 | Sector pages live; structured content indexed |
| Month 12 | 40–60 | Authority building underway; content maturing |
| Month 18 | 60–80 | Approaching Sasaki current position |

[ASSUMPTION: Citation trajectory estimates are based on comparable authority-building timelines for professional services firms with similar starting Domain Ratings. Actual results will vary based on content quality, backlink acquisition, and AI platform update cycles.]

---

## Section 5: Entity Audit

### 5.1 What Google and AI Systems Currently Know About EPTDESIGN

An entity audit maps every data signal about an organisation that search engines and AI systems can access. For EPTDESIGN, that inventory is thin, inconsistent, and insufficient to establish the firm's full identity.

**Currently Indexed Signals**

| Source | Signal Type | Quality | Issues |
|---|---|---|---|
| eptdesign.com | Website (primary) | Poor | No structured data; no sector pages; no person markup; last project updates 2021 |
| LinkedIn (Company Page) | Social entity | Moderate | 2,354 followers; inconsistent description; not fully optimised |
| Google Business Profile (Pasadena) | Local entity | Poor | Address inconsistency; no description; no services; few reviews |
| Google Business Profile (Irvine) | Local entity | Poor | No description; no services |
| Google Business Profile (Claremont) | Local entity | Poor | No description; no services |
| Google Business Profile (Santa Barbara) | Local entity | Poor | No description; no services |
| Google Business Profile (Solana Beach) | Local entity | Critical | 2-star review (unanswered, only review); possible incorrect location listing |
| Yelp | Directory | Fragmented | Address inconsistency; minimal content |
| Houzz | Design directory | **[ASSUMPTION: Thin profile; not fully optimised]** | Project images present; no firm description or credential content |
| Ahrefs | Authority data | DR 29 | Reflects low inbound link profile |
| ASLA Directory | Professional directory | **[ASSUMPTION: Present but minimal]** | Credential signal; low content depth |
| Archinect | Architecture directory | **[ASSUMPTION: Possibly listed; not optimised]** | Potential authority source underutilised |

**What Is Missing from the Entity Picture**

| Entity Signal | Status | Impact of Absence |
|---|---|---|
| Founding year (1962) anchored in metadata | Absent | Longevity signal not processed by AI |
| Eckbo lineage explicitly documented | Absent | Authority context unavailable to AI citation |
| FASLA credential (Nord Eriksson) in structured form | Absent | Professional authority not indexed |
| LEED Platinum project (Frontier, Stephen Carroll) | Absent | Credential signal not surfaced |
| ESOP/employee-owned status | Absent | Differentiation signal missing |
| Named client relationships (Kaiser, Pomona, Cedars-Sinai) | Absent as text | Project pages have images; clients not named in indexable copy |
| 5-studio geographic footprint | Absent | AI cannot confirm geographic scope |
| Sector specialisations | Absent | Cannot be cited for sector queries |
| Award history (ASLA Merit, AIA, ENR) | Absent | Authority validation missing |
| Press citations (Veranda, Martha Stewart) | Absent as entity signal | National press not connected to firm entity |

### 5.2 What the Entity Should Look Like

A complete entity model for EPTDESIGN would allow any search engine or AI system to answer the following questions with confidence:

- What does EPTDESIGN do?
- Where do they operate?
- How long have they been in practice?
- Who are the principals and what are their credentials?
- Which sectors do they serve?
- Which notable projects have they completed?
- What awards have they received?
- Who has published coverage of their work?
- What makes them different from comparable firms?

Currently, none of these questions can be answered from indexed content with confidence. The firm's digital entity is a fragment of the actual organisation.

---

## Section 6: The 64-Year Asset — Untapped Authority

### 6.1 The Eckbo Lineage

Bob Eriksson, founder of EPTDESIGN (then Eriksson, Peters & Thomas), trained under Garrett Eckbo — one of three figures (alongside Dan Kiley and James Rose) who defined the California modernist landscape movement in the mid-twentieth century. Eckbo's influence on American landscape architecture is academically documented and widely referenced in landscape history.

This lineage is an extraordinary authority signal. It connects EPTDESIGN directly to a historically significant design tradition, to academic and institutional credibility, and to a narrative of multi-generational practice continuity (Bob Eriksson to Nord Eriksson FASLA). It is the kind of provenance that landscape architecture academics, institutional clients, and editorial writers find genuinely compelling.

It is currently represented nowhere on the EPTDESIGN website in a form that search engines or AI systems can read and index.

**Strategic Use of the Lineage**

- A firm history page that explicitly names Garrett Eckbo, situates the California modernist movement, and traces the practice from 1962 to the present
- This page becomes a linkable asset — universities, landscape history resources, and design publications would link to it if it existed and was written to editorial standard
- AI systems that are asked about California landscape architecture history would have a documented basis to include EPTDESIGN in that narrative
- The lineage differentiates EPTDESIGN from every local Pasadena competitor with no equivalent depth of history

### 6.2 FASLA Credentials and National Press

Nord Eriksson holds Fellow of the American Society of Landscape Architects (FASLA) designation — the highest credential in the profession. It is awarded to approximately 3% of ASLA members. It signals demonstrated excellence and peer recognition at the national level.

Nord Eriksson has also been featured in Veranda and Martha Stewart Living. These are national consumer publications with significant audiences in the high-net-worth residential market. A feature in Veranda represents exactly the kind of editorial credibility that estate clients use as a proxy for quality.

Neither of these signals is currently connected to the EPTDESIGN entity in any structured, indexed form. A principal profile page for Nord Eriksson, linked to the press coverage and explicitly citing the FASLA credential, would:

- Surface in searches for "FASLA landscape architect Southern California"
- Provide AI systems with a named expert attribution point
- Create an authority anchor for the Estate Residences sector page
- Enable link acquisition from ASLA, design publications, and luxury real estate platforms

### 6.3 LEED Platinum — Stephen Carroll

Stephen Carroll ASLA LEED AP led the Frontier Project to LEED Platinum certification. LEED Platinum is the highest certification level under the LEED green building rating system; landscape architecture contributions to a Platinum-certified project represent demonstrable sustainable design expertise.

This is directly relevant to:
- Institutional clients with sustainability mandates (universities, healthcare systems, municipal governments)
- Commercial developers with ESG reporting requirements
- The growing category of explicitly sustainability-focused project briefs

The credential does not appear in any indexed content. A structured project case study for the Frontier Project, connected to Stephen Carroll's profile and to an EPT sustainability/LEED credential page, would position the firm competitively for this category of search and AI query.

### 6.4 Repeat Institutional Clients — Authority Through Loyalty

| Client | Relationship Depth | Strategic Value |
|---|---|---|
| Kaiser Permanente | 4 projects | Healthcare sector credibility; named brand recognition |
| Pomona College | 4 projects | Higher education sector; liberal arts prestige |
| Cedars-Sinai | Named project | Major healthcare system; Los Angeles brand |
| Google (Venice campus) | Named project | Technology sector; design quality signal |
| UCLA | Named project | Major public research university |
| Trammell Crow | Named project | Major national developer relationship |
| The Irvine Company | Named project | Major Southern California developer |
| City of Glendale | Named project | Municipal/civic sector |

Repeat institutional clients are among the strongest authority signals a professional services firm can demonstrate. A client who commissions four projects is not experimenting — they are relying on the firm as a trusted long-term partner.

These relationships are not surfaced in any structured form that search engines or AI systems can index. Project pages have images but lack the named client context, scope descriptions, and outcomes that would allow AI systems to cite EPTDESIGN when a prospect asks "which landscape architecture firms have worked with major healthcare systems in California?"

### 6.5 Awards — Structured Validation

| Award | Category | Strategic Use |
|---|---|---|
| ASLA Merit Award | Professional peer recognition | Credential anchor for sector pages |
| AIA Academy on Architecture for Health | Healthcare sector credibility | Healthcare sector page anchor |
| ENR California Best Projects | Regional recognition; developer/institutional readership | Commercial/institutional sector authority |

Awards carry dual value: they are authority signals in their own right, and they are typically associated with award-body websites that carry high Domain Ratings. An ENR California Best Projects citation typically includes a link from enr.com (high DR). An ASLA Award entry includes a link from asla.org. These are exactly the quality backlinks that raise EPTDESIGN's Domain Rating.

An awards page that lists all honours with years, project associations, and award body links would serve as both an entity anchor and a link acquisition mechanism.

---

## Section 7: Local SEO Audit Summary

### 7.1 Google Business Profile Status — All Locations

Google Business Profile (GBP) is the primary mechanism by which a professional services firm appears in local search results, map packs, and Google's knowledge panels. For a multi-studio firm like EPTDESIGN, each location is a separate GBP listing that must be independently optimised.

| Location | Reviews | Description | Services Listed | Photos | Issues |
|---|---|---|---|---|---|
| Pasadena (HQ) | **[ASSUMPTION: 2–3]** | None | None | **[ASSUMPTION: Minimal]** | Address inconsistency; primary listing |
| Irvine | **[ASSUMPTION: 1]** | None | None | **[ASSUMPTION: Minimal]** | No sector content |
| Claremont | **[ASSUMPTION: 1]** | None | None | **[ASSUMPTION: Minimal]** | No sector content |
| Santa Barbara | **[ASSUMPTION: 1]** | None | None | **[ASSUMPTION: Minimal]** | No sector content |
| Solana Beach | 1 (2-star) | None | None | **[ASSUMPTION: Minimal]** | Critical: 2-star unanswered review; may be incorrect location (current studios are Pasadena, Irvine, Claremont, Santa Barbara, San Diego — Solana Beach is in San Diego County but appears to be a separate listing from the San Diego studio) |

**Total Reviews Across All Locations: 5**

Five reviews across five locations is critically below the threshold at which Google treats a business as established. Local SEO research consistently shows that businesses with fewer than 10 reviews per location are disadvantaged in local pack rankings. At 1 review per location average, EPTDESIGN is effectively invisible in local map results.

For context: a comparable professional services firm with mature local SEO would expect 20–50+ reviews per active location, accumulated over 12–24 months of systematic review generation.

### 7.2 The 2-Star Solana Beach Review — Critical Risk

The Solana Beach GBP listing has a single review, rated 2 stars. It is unanswered. This is the entire review record for that listing.

A single unanswered 2-star review is the worst possible GBP state from a first-impression perspective. Any prospective client or developer in the San Diego area who checks the EPTDESIGN GBP listing for that geography will see a 2-star rating with no response. The absence of a response signals either inattention to client concerns or indifference to the platform.

**Immediate Actions Required**
1. Identify whether the Solana Beach listing is the intended San Diego studio listing or a duplicate/incorrect listing
2. If it is the active San Diego studio listing: respond to the review professionally and promptly, then begin active review generation for that location
3. If it is an incorrect or duplicate listing: evaluate consolidation with the correct San Diego studio listing
4. Do not delete the listing without verifying whether Google will transfer reviews to a replacement listing

### 7.3 NAP Inconsistency — Pasadena Address

Three different Pasadena addresses are currently in circulation across directories, listings, and the EPTDESIGN website. The address displayed on the website does not match the address most commonly listed in external directories.

| Source | Address Shown | Notes |
|---|---|---|
| eptdesign.com | [Address A] | Current website display |
| Google Business Profile | [Address B] | **[ASSUMPTION: Different from website]** |
| External directories (Yelp, Houzz, etc.) | [Address C] | **[ASSUMPTION: Third variant in circulation]** |

[ASSUMPTION: Specific addresses redacted pending client confirmation of current HQ address. Three distinct addresses have been observed in audit; the correct address must be confirmed by Alison Spicer before standardisation.]

NAP inconsistency is a well-documented local SEO suppression factor. Google's local ranking algorithm uses NAP consistency as a trust signal. Three different addresses for the same location signals unreliability, which reduces the confidence score for all EPTDESIGN GBP listings. The fix requires identifying the canonical address, updating the website, then systematically correcting every directory listing.

### 7.4 Missing GBP Content — All Locations

None of the five GBP listings currently include:
- Business description (200–750 word capacity available)
- Services list (sector-specific services can be listed)
- Posts (Google Posts appear in the knowledge panel and can promote projects, awards, and team news)
- Q&A content (questions can be pre-populated and answered to surface FAQs)
- Products (applicable for named service packages)

Each of these content areas contributes to GBP completeness scores and to local ranking. A fully populated GBP listing for Pasadena HQ would include a firm description covering all sectors, all studio locations, key credentials (FASLA, LEED AP), and notable clients. It would list services across all five sectors. It would have regular posts featuring project completions and award announcements.

---

## Section 8: Strategic Opportunity Matrix

### 8.1 Framework

The following matrix maps what is currently captured against what is achievable, across four dimensions: organic search, AI citation, local visibility, and authority/domain rating. Each cell reflects the gap between current state and achievable state within a 12-month implementation horizon.

### 8.2 Organic Search Opportunity

| Opportunity | Current Capture | 12-Month Target | Effort | Priority |
|---|---|---|---|---|
| Brand search (firm name) | Partial | Full | Low | Maintain |
| "Landscape architect Pasadena" | 0% | Top 5 position | Medium | High |
| "Landscape architect Irvine" | 0% | Top 5 position | Medium | High |
| "Landscape architecture Southern California" | 0% | Top 10 position | High | High |
| "Estate landscape architect Los Angeles" | 0% | Top 5 position | Medium | High |
| "Healthcare landscape architect California" | 0% | Top 10 position | High | High |
| "LEED landscape architect California" | 0% | Top 10 position | Medium | Medium |
| "Landscape architect Claremont" | 0% | Top 3 position | Low | Medium |
| "Landscape architect Santa Barbara" | 0% | Top 5 position | Low | Medium |
| "Landscape architect San Diego" | 0% | Top 10 position | Medium | Medium |
| Principal name searches (Nord Eriksson, Scott Horsley) | Partial brand | Full with profile pages | Low | High |
| Project attribution (Cedars-Sinai, UCLA, Kaiser) | 0% | Partial recovery | Medium | High |
| Award-related searches (ASLA Merit, ENR) | 0% | Some visibility | Low | Medium |
| "FASLA landscape architect" | 0% | Some visibility | Low | Medium |

### 8.3 AI Citation Opportunity

| Query Category | Current Citations | 12-Month Target | Pathway |
|---|---|---|---|
| Southern California landscape architecture firms | 0 | 5–10 citations | Sector pages + unblocking |
| Estate/residential landscape design LA | 0 | 5–10 citations | Nord Eriksson profile + estate page |
| Healthcare landscape architecture California | 0 | 3–8 citations | Healthcare sector page + AIA award |
| University campus landscape architects | 0 | 3–8 citations | Higher education sector page + Pomona/UCLA |
| Mixed-use/multifamily landscape design | 0 | 3–8 citations | Housing sector page + Dan Hoon profile |
| LEED landscape architects | 0 | 3–5 citations | Stephen Carroll profile + Frontier case study |
| Landscape architects Pasadena | 0 | 5–10 citations | Local entity + unblocking |
| California landscape architecture history | 0 | 2–5 citations | Eckbo lineage page |
| Employee-owned landscape architecture firms | 0 | 2–5 citations | ESOP content + firm story |
| **Total estimated 12-month citation target** | **0** | **40–60** | Full strategy implementation |

### 8.4 Local Visibility Opportunity

| Metric | Current State | 12-Month Target | Action Required |
|---|---|---|---|
| GBP Reviews (Pasadena) | **[ASSUMPTION: 2–3]** | 25–35 | Systematic review generation |
| GBP Reviews (Irvine) | **[ASSUMPTION: 1]** | 15–25 | Systematic review generation |
| GBP Reviews (Claremont) | **[ASSUMPTION: 1]** | 10–20 | Systematic review generation |
| GBP Reviews (Santa Barbara) | **[ASSUMPTION: 1]** | 10–20 | Systematic review generation |
| GBP Reviews (San Diego/Solana Beach) | 1 (2-star) | 15–25 | Resolve 2-star; generate new reviews |
| NAP Consistency | 3 variants | 1 canonical address | Standardise + update all directories |
| GBP Descriptions | None | Complete, optimised | Write + publish |
| GBP Services | None | Full sector listing | Configure |
| Local map pack ranking ("landscape architect Pasadena") | Not appearing | Top 3 | GBP + NAP + local content |

### 8.5 Authority and Domain Rating Opportunity

| Metric | Current | 6 Months | 12 Months | 18 Months |
|---|---|---|---|---|
| Domain Rating | 29 | 35–38 | 42–48 | 50–55 |
| Referring Domains (quality) | **[ASSUMPTION: <50]** | 60–80 | 90–120 | 130–160 |
| Key backlink sources | Minimal | ASLA, Archinect, awards | ENR, AIA, trade press | Veranda, design publications |
| Entity confidence score (Google Knowledge Graph) | Low | Moderate | High | High |

[ASSUMPTION: Domain Rating targets are based on comparable authority-building trajectories for professional services firms starting at DR 25–35. Actual results depend on link acquisition quality and velocity.]

### 8.6 Summary: The Gap in Plain Terms

EPTDESIGN is a firm with genuine, documented authority — in its lineage, its credentials, its client relationships, and its award history — that is capturing approximately 0% of the digital visibility its position warrants.

The gap is not caused by poor-quality work or a weak brand. It is caused by three structural absences: AI crawler access, service page architecture, and entity consistency. These are correctable. The investment required is proportionate to the revenue at stake. The timeline is 12–18 months to a position that reflects the firm's actual standing in the profession.

The opportunity cost of delay is not neutral. Every month that EPTDESIGN remains invisible in search and AI, competitors are accumulating citations, rankings, and backlinks that compound over time. Sasaki's DR 70 and 88 AI citations were not achieved in a single quarter. They represent sustained infrastructure investment. The longer EPTDESIGN waits, the wider that gap becomes and the longer it takes to close.

The strategic window is now. The assets exist. The infrastructure does not yet. This strategy builds it.

---

*This document is the evidence layer for EPTDESIGN's AI and search visibility strategy. All figures marked [ASSUMPTION: ...] should be verified against live platform data before being cited in client-facing materials or presentations.*
