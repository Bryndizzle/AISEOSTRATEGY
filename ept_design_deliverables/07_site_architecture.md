# EPTDESIGN Recommended Site Architecture
### Deliverable 07 — Information Hierarchy & URL Structure
**Prepared for:** Alison Spicer, Marketing Director, EPTDESIGN
**Date:** February 2026
**Classification:** Internal Strategy Document

---

## Overview

This document defines the complete recommended site architecture for EPTDESIGN.com — what pages need to exist, what they should contain, how they should be structured, and in what order they should be built. It is the structural implementation of the strategic framework established in Deliverable 06.

**Current state summary:** EPTDESIGN's site has five navigation sections (WORK, ABOUT, PEOPLE, OUR STORIES, CONTACT) and 87 project pages. It has no service pages, no location pages, and no structured history or award consolidation. The site cannot rank for non-branded queries because there is no page architecture to support topical authority in any service category.

**Recommended state:** A site with approximately 125–135 pages across eight primary sections, with clear entity signals, service coverage, location coverage, and interconnected internal linking.

---

## 1. Current State Analysis

### The Five-Section Navigation: What Each Section Does and Doesn't Do

| Current Section | URL Pattern | What It Does | What It Fails to Do |
|---|---|---|---|
| WORK | /work/ | Displays 87 project thumbnails; filterable by sector | No service context; filters are not indexable pages; projects are not discoverable by search; no schema |
| ABOUT | /about/ | Brief firm description | No history, no awards, no ownership story, no lineage — virtually no entity signals |
| PEOPLE | /people/ | Lists principals with short bios | Bios are thin; no credential depth; no project associations; minimal Person schema |
| OUR STORIES | /our-stories/ | Blog / editorial content | Last substantive update July 2021; no strategic topic ownership; no schema |
| CONTACT | /contact/ | Five studio addresses | No location-specific pages; no GBP integration; no local keyword targeting |

### The Structural Gaps

Five critical structural gaps prevent organic search visibility:

**Gap 1: No Service Pages**
Every search query that begins with a service category — "landscape architect," "estate garden design," "healthcare landscape design," "campus landscape architecture" — has no corresponding page on the EPTDESIGN site to land on. The firm's portfolio demonstrates capability in all of these areas. The site architecture does not.

**Gap 2: No Location Pages**
A firm with five studio locations and zero location-specific landing pages cannot compete in local search. When a developer in Irvine searches "landscape architect Irvine CA," there is no page optimized for that geography.

**Gap 3: No History Page**
64 years of practice, a documented design lineage, ESOP conversion, and studio expansion are entity-defining facts that appear nowhere on the site in structured, crawlable form.

**Gap 4: No Awards Page**
ASLA Merit awards, AIA Academy on Architecture for Health recognition, and ENR California Best Projects wins are credibility anchors. They are not consolidated anywhere on the site.

**Gap 5: No Schema Markup**
Without structured data, search engines must infer everything about the firm's identity, services, locations, and people from unstructured text. Schema markup is not optional — it is the difference between being classified correctly and being invisible.

### The 87 Project Pages: Potential vs. Reality

EPTDESIGN has 87 project pages. Each one represents a potential ranking asset. Currently, most are:
- Short (under 300 words)
- Photo-heavy, text-light
- Missing schema markup
- Missing principal attribution
- Missing awards or certifications
- Missing service category associations
- Last updated July 2021

With content expansion and schema, these 87 pages can become a significant organic traffic asset. Without it, they remain a gallery that only existing clients can navigate.

---

## 2. Recommended Site Architecture

### Architecture Overview

The recommended site architecture adds three new primary sections (/services/, /locations/, and expanded /about/ subsections) and restructures the existing sections to support topical authority and entity clarity.

```
EPTDESIGN.COM
│
├── / (Homepage)
│
├── /services/ ── NEW SECTION ─────────────────────────────────────
│   ├── /services/landscape-architecture/
│   ├── /services/estate-residential-garden-design/
│   ├── /services/campus-landscape-architecture/
│   ├── /services/healthcare-landscape-design/
│   ├── /services/multifamily-housing-landscape/
│   ├── /services/parks-civic-design/
│   ├── /services/urban-design-planning/
│   ├── /services/master-planning/
│   └── /services/sustainable-landscape-leed/
│
├── /locations/ ── NEW SECTION ────────────────────────────────────
│   ├── /locations/pasadena/
│   ├── /locations/irvine/
│   ├── /locations/claremont/
│   ├── /locations/santa-barbara/
│   └── /locations/san-diego/
│
├── /work/ ── EXISTING (expand and refresh) ──────────────────────
│   └── /work/[project-slug]/ (87 existing + ongoing)
│
├── /about/ ── EXISTING (expand with subsections) ───────────────
│   ├── /about/history/  ← NEW
│   ├── /about/awards/   ← NEW
│   └── /about/employee-owned/  ← NEW
│
├── /people/ ── EXISTING (expand individual pages) ──────────────
│   ├── /people/scott-horsley/
│   ├── /people/nord-eriksson/
│   ├── /people/stephen-carroll/
│   ├── /people/dan-hoon/
│   ├── /people/ross-woodley/
│   ├── /people/matthew-lysne/
│   └── /people/alison-spicer/
│
├── /our-stories/ ── EXISTING (reposition as thought leadership) ─
│   └── /our-stories/[article-slug]/
│
└── /contact/ ── EXISTING (redirect to /locations/) ─────────────
```

---

### Section A: /services/ — The Missing Foundation

The /services/ section does not exist. It is the single highest-priority build in the entire site architecture. Without it, no service-category keyword can be targeted, no topical authority can be established, and AI systems have no structured content to cite when describing what EPTDESIGN does.

#### /services/ (Hub Page)

**URL:** `eptdesign.com/services/`
**Purpose:** Introduce all service capabilities; link to all nine service pages; establish topical authority as a comprehensive landscape architecture and urban design practice
**Target queries:** "landscape architecture services," "landscape architecture firm Southern California," "eptdesign services"
**Content requirements:**
- 600–800 words introducing EPT's practice philosophy and breadth
- Grid or card layout linking to all nine service pages
- Short description (2–3 sentences) for each service
- Notable client logos across sectors
- CTA linking to /contact/ or specific principal contacts

**Schema:** `Service` (aggregated), `Organization`

---

#### /services/landscape-architecture/

**Purpose:** Top-of-funnel awareness page for the broadest service category; captures "landscape architecture" broad-match queries
**Target queries:** "landscape architecture firm Pasadena," "landscape architecture company Southern California," "landscape architects Los Angeles"
**Content requirements:**
- 900–1,100 words on EPTDESIGN's overall landscape architecture practice
- Founded 1962 anchor statement
- Five studio locations referenced
- Brief introduction to each specialist service with links
- 3–4 featured projects across different sectors
- Principal team overview with photo links to /people/ pages
- Awards callout block (ASLA, AIA, ENR)
**Schema:** `Service`, `Organization`, `BreadcrumbList`

---

#### /services/estate-residential-garden-design/

**Purpose:** Highest-margin service; connects Nord Eriksson's expertise and editorial recognition to estate/HNW residential search queries
**Target queries:** "estate landscape architect," "private garden design Pasadena," "luxury landscape design Southern California," "estate garden designer California"
**Content requirements:**
- 1,000–1,200 words on EPTDESIGN's estate residential design philosophy
- Nord Eriksson featured prominently with FASLA designation
- Reference to Veranda and Martha Stewart Living coverage (with links if available)
- Garrett Eckbo / California modernist design lineage connection
- 4–5 estate project examples with links to /work/ pages
- Client profile description (HNW homeowners, estate managers, architects of record)
- Geographic areas served (Pasadena, San Marino, Santa Barbara, Montecito, La Jolla)
- FAQ schema: "What is estate landscape design?", "How long does an estate garden design take?", "What does a FASLA designation mean?"
**Schema:** `Service`, `Person` (Nord Eriksson), `FAQPage`, `BreadcrumbList`
**Note:** This page should be linked from any future Veranda / AD press coverage as the canonical landing page for estate residential inquiries.

---

#### /services/campus-landscape-architecture/

**Purpose:** Target university, college, and K–12 institutional buyers in the facilities/planning function
**Target queries:** "university campus landscape architect," "college campus landscape design," "campus master plan landscape," "educational landscape architecture California"
**Content requirements:**
- 900–1,100 words on campus landscape architecture process and philosophy
- Pomona College four-project relationship featured (with permission)
- UCLA Botanical Garden and other higher education projects referenced
- Reference to Claremont Colleges geographic proximity and institutional familiarity
- Principals associated: Scott Horsley, relevant project leads
- Process description: phased campus planning, master plan integration, student experience design
- FAQ schema: "How does campus landscape architecture differ from commercial design?"
**Schema:** `Service`, `FAQPage`, `BreadcrumbList`

---

#### /services/healthcare-landscape-design/

**Purpose:** Target hospital administrators, healthcare REITs, and healthcare architecture firms (HOK, Gensler Health) in need of landscape architecture subconsultant
**Target queries:** "healthcare landscape design," "healing garden design," "hospital landscape architecture," "healthcare campus landscape architect"
**Content requirements:**
- 1,000–1,200 words on evidence-based healing garden design and healthcare landscape principles
- Stephen Carroll ASLA LEED AP featured as sector lead
- Kaiser Permanente four-project relationship featured (with permission)
- Cedars-Sinai AHSP project featured (AIA Academy on Architecture for Health award)
- Reference to evidence-based design principles (Ulrich research, CABE guidance)
- Client types: health systems, hospital construction divisions, healthcare REIT development teams, medical campus planners
- AIA Academy on Architecture for Health award highlighted
**Schema:** `Service`, `Person` (Stephen Carroll), `FAQPage`, `BreadcrumbList`

---

#### /services/multifamily-housing-landscape/

**Purpose:** Target multifamily developers, property management companies, and affordable housing developers across the Western US
**Target queries:** "multifamily landscape architecture," "apartment community landscape design," "multifamily outdoor amenity design," "residential landscape architecture developer"
**Content requirements:**
- 900–1,100 words on multifamily community design philosophy
- Dan Hoon featured with 6-state licensure prominently noted (CA, AZ, NV, CO, WA, OR — confirm states)
- Village at Irvine Spectrum and other multifamily projects featured
- Irvine Company relationship referenced (with permission)
- Geographic range of practice highlighted as differentiator
- Amenity programming section: pool surrounds, courtyards, leasing entries, dog runs, community gardens
- Developer-friendly language: schedule, budget, permit facilitation
**Schema:** `Service`, `Person` (Dan Hoon), `FAQPage`, `BreadcrumbList`

---

#### /services/parks-civic-design/

**Purpose:** Target municipal parks departments, public works agencies, and civic-focused developers
**Target queries:** "park design firm California," "civic landscape architect," "municipal landscape design," "public park design company"
**Content requirements:**
- 900–1,100 words on public realm and civic landscape design
- Glendale Narrows Riverwalk featured as signature civic project
- City of Glendale relationship referenced
- ENR California Best Projects recognition highlighted
- Public process description: community engagement, ADA compliance, environmental review
- Client types: municipal parks and recreation departments, public works, county agencies, special districts
- Grant-eligible project experience (if applicable)
**Schema:** `Service`, `FAQPage`, `BreadcrumbList`

---

#### /services/urban-design-planning/

**Purpose:** Target planning agencies, master developers, and architecture firms seeking urban design subconsultant expertise
**Target queries:** "urban design firm Southern California," "urban design landscape architecture," "streetscape design firm," "public realm design consultant"
**Content requirements:**
- 800–1,000 words on urban design and planning integration
- Relevant projects featured (Google Venice Campus if urban in scope)
- Scale of work: streetscapes, plazas, transit corridors, mixed-use ground planes
- Collaboration model with architecture and planning firms
- Reference to Trammell Crow and commercial developer relationships
**Schema:** `Service`, `FAQPage`, `BreadcrumbList`

---

#### /services/master-planning/

**Purpose:** Target large institutional and multi-phase development clients needing long-horizon landscape strategy
**Target queries:** "landscape master planning," "site master plan landscape architect," "campus master plan consultant"
**Content requirements:**
- 800–1,000 words on master planning philosophy and process
- Long-duration client relationships as proof (Pomona College, Kaiser) — demonstrates the firm's master planning credibility through sustained relationships
- Phases of work: inventory, analysis, visioning, phased implementation
- Value of ESOP stability for multi-year engagements (clients work with same people throughout)
**Schema:** `Service`, `FAQPage`, `BreadcrumbList`

---

#### /services/sustainable-landscape-leed/

**Purpose:** Target sustainability-focused clients, public agencies with green building mandates, and LEED-seeking developers
**Target queries:** "LEED landscape architecture," "sustainable site design," "green landscape architect Southern California," "LEED certified landscape design"
**Content requirements:**
- 900–1,100 words on sustainable design philosophy and LEED expertise
- Stephen Carroll ASLA LEED AP as primary voice; LEED Platinum achievement named explicitly
- Specific LEED credits typically pursued in landscape scope (SSc, WEc, MRc)
- SITES rating system reference if applicable
- Native plant palette, water efficiency, urban heat island, stormwater management as topic threads
- FAQ schema: "What LEED credits apply to landscape architecture?", "What is LEED Platinum?", "How does sustainable landscape design reduce operating costs?"
**Schema:** `Service`, `Person` (Stephen Carroll), `FAQPage`, `BreadcrumbList`

---

### Section B: /locations/ — Geographic Presence That Doesn't Exist

All five location pages must be built. They serve dual purposes: local search ranking (appearing when buyers add a city modifier to their query) and entity clarity (confirming to Google's knowledge graph that EPTDESIGN operates in these markets).

#### /locations/pasadena/ — Primary Location

**URL:** `eptdesign.com/locations/pasadena/`
**Purpose:** Primary location page; headquarters; anchor for all Pasadena and greater LA Basin queries
**Target queries:** "landscape architect Pasadena," "landscape architecture Pasadena CA," "estate landscape design Pasadena," "landscape architect San Gabriel Valley"
**Content requirements:**
- 700–900 words on EPTDESIGN's Pasadena presence and regional expertise
- Full address, phone, hours
- Studio description (HQ, founding location)
- Local projects featured: Pomona College (Claremont), UCLA (Westwood), Glendale Narrows Riverwalk, Caltech if applicable
- Markets served from this location: LA Basin, San Gabriel Valley, Pasadena/Arcadia/Monrovia corridor, inland communities
- Embedded Google Map
- Link to full team page (/people/)
- Link to GBP review page
**Schema:** `LocalBusiness`, `GeoCoordinates`, `PostalAddress`, `BreadcrumbList`

---

#### /locations/irvine/ — Orange County Hub

**URL:** `eptdesign.com/locations/irvine/`
**Purpose:** Establish presence for OC developer, commercial, and multifamily market
**Target queries:** "landscape architect Irvine," "landscape architect Orange County," "multifamily landscape design Irvine," "commercial landscape architect OC"
**Content requirements:**
- 700–900 words on EPTDESIGN's Irvine studio and OC market expertise
- Full address, phone, hours
- Irvine Company relationship referenced (if permitted)
- Village at Irvine Spectrum and other OC/south OC projects
- Dan Hoon as primary OC contact (multifamily expertise)
- Markets served: Irvine, Newport Beach, Aliso Viejo, Laguna Niguel, Mission Viejo, Anaheim
- Embedded Google Map
**Schema:** `LocalBusiness`, `GeoCoordinates`, `PostalAddress`, `BreadcrumbList`

---

#### /locations/claremont/ — Inland Empire / Colleges

**URL:** `eptdesign.com/locations/claremont/`
**Purpose:** Establish presence for Inland Empire institutional and residential market; leverage Claremont Colleges proximity
**Target queries:** "landscape architect Claremont," "landscape architect Inland Empire," "college campus landscape architect Claremont"
**Content requirements:**
- 600–800 words on EPTDESIGN's Claremont studio
- Full address, phone, hours
- Pomona College four-project relationship featured
- Claremont Colleges consortium as institutional market
- Residential estate work in Claremont/Upland/Rancho Cucamonga if applicable
**Schema:** `LocalBusiness`, `GeoCoordinates`, `PostalAddress`, `BreadcrumbList`

---

#### /locations/santa-barbara/ — Coastal Residential

**URL:** `eptdesign.com/locations/santa-barbara/`
**Purpose:** Establish presence for Santa Barbara / Montecito HNW residential market
**Target queries:** "landscape architect Santa Barbara," "estate landscape design Montecito," "garden designer Santa Barbara"
**Content requirements:**
- 600–800 words on EPTDESIGN's Santa Barbara studio and coastal estate expertise
- Full address, phone, hours
- Nord Eriksson estate expertise as primary credential for this market
- Any Santa Barbara / Montecito projects (if client-permissible)
- Coastal landscape considerations: salt-tolerant plants, fire-wise landscaping, water restrictions
**Schema:** `LocalBusiness`, `GeoCoordinates`, `PostalAddress`, `BreadcrumbList`

---

#### /locations/san-diego/ — Southern Hub

**URL:** `eptdesign.com/locations/san-diego/`
**Purpose:** Establish presence for San Diego market — civic, healthcare, commercial, and residential
**Target queries:** "landscape architect San Diego," "landscape design firm San Diego," "park design San Diego"
**Content requirements:**
- 600–800 words on EPTDESIGN's San Diego studio
- Full address, phone, hours
- Relevant San Diego projects featured
- Markets served: San Diego, Chula Vista, La Jolla, Coronado, North County
**Schema:** `LocalBusiness`, `GeoCoordinates`, `PostalAddress`, `BreadcrumbList`

---

### Section C: /work/ — 87 Pages That Need to Work Harder

The 87 existing project pages are the firm's most valuable latent SEO asset. They demonstrate real capability across all sectors. The problem is they are structured as a gallery, not as searchable content.

#### Priority Projects for Content Expansion (Phase 1)

The following projects should receive full content expansion as Phase 1 priority, based on search relevance, sector coverage, and award/client authority:

| Project | Priority Rationale | Target Query Cluster |
|---|---|---|
| **Google Backlot (Venice Campus)** | High-profile tech client; urban design showcase | "tech campus landscape design," "Google campus landscape" |
| **Cedars-Sinai AHSP** | AIA Academy award winner; healthcare design proof | "healthcare landscape design," "healing garden design Los Angeles" |
| **UCLA Botanical Garden** | Institutional; botanical/ecological credibility | "university landscape design Los Angeles," "botanical garden design" |
| **Glendale Narrows Riverwalk** | ENR Best Projects; civic/public realm showcase | "riverfront park design," "civic landscape architecture California" |
| **Kaiser Permanente #1** | Healthcare; first of four-project relationship | "Kaiser Permanente landscape," "healthcare campus design" |
| **Kaiser Permanente #2–4** | Healthcare relationship depth | Cross-link all four; cluster authority |
| **Pomona College #1** | Higher education; first of four-project relationship | "college campus landscape," "Pomona College" |
| **Pomona College #2–4** | Education relationship depth | Cross-link all four; cluster authority |
| **Village at Irvine Spectrum** | Multifamily; developer client; OC market | "multifamily landscape design Irvine," "mixed-use landscape" |

#### Project Page Content Standard (Apply to All 87 Eventually)

Each project page should include:

| Element | Current State | Required State |
|---|---|---|
| Project name | Usually present | Full name, not abbreviated |
| Client name | Sometimes present | Full client name, linkable |
| Location | Sometimes present | City, State — structured in schema |
| Year completed | Usually absent | Year completed + duration if notable |
| Project scope | Usually absent | Acreage, program elements, phased description |
| EPTDESIGN role | Usually absent | Landscape architect of record, subconsultant, etc. |
| Principal(s) | Usually absent | Named principal with link to /people/ page |
| Awards | Usually absent | Award name, year, category |
| Services | Usually absent | 1–3 service tags with links to /services/ pages |
| Outcomes | Usually absent | Measurable results: LEED credits, species count, acreage |
| Schema | None | `Project`-type schema (or `CreativeWork`), `Person`, `Organization` |
| Word count | Under 300 | 500–800 per project |

---

### Section D: /about/ — Entity Definition Subsections

The current /about/ page is insufficient for entity-building purposes. Three subsections must be added.

#### /about/history/

**URL:** `eptdesign.com/about/history/`
**Purpose:** The most important entity-building page on the site. This is where Google and AI systems learn who EPTDESIGN is, in verifiable, structured, factual terms.
**Target queries:** "EPTDESIGN history," "EPTDESIGN founded," "landscape architecture firm California history," "California modernist landscape architecture"
**Content requirements:**
- 1,200–1,500 words structured as a chronological narrative with milestone callouts
- 1962: Founding by Bob Eriksson
- Garrett Eckbo lineage established (verifiable connection — confirm with Nord Eriksson)
- Studio expansion dates: when each of the five studios opened
- ESOP conversion: year and significance
- Key award milestones: FASLA fellowship year, first ASLA award, etc.
- Notable project milestones: first institutional project, first healthcare project, etc.
- 2026 current state: 35–40 staff, five studios, six sectors
- Visual timeline graphic recommended (also useful for PR/social)
**Schema:** `Organization`, `Event` (milestones), `BreadcrumbList`

**Assumption:** The Eckbo lineage connection needs to be confirmed with Nord Eriksson and documented with a verifiable primary source (not just asserted). If it cannot be substantiated, this section should be written around Bob Eriksson's founding vision and design philosophy without making unverifiable claims about the Eckbo connection.

---

#### /about/awards/

**URL:** `eptdesign.com/about/awards/`
**Purpose:** Consolidate all award recognition in one discoverable, schema-rich page; build credibility signals for AI and search systems
**Target queries:** "EPTDESIGN awards," "landscape architecture firm awards California"
**Content requirements:**
- Complete list of all ASLA Merit/Honor Awards (year, project, category)
- AIA Academy on Architecture for Health recognition (Cedars-Sinai AHSP)
- ENR California Best Projects wins (year, project, category)
- Any LEED project certifications (year, project, certification level)
- Any Houzz, regional, or other relevant recognitions
- Each award entry: Award Name, Year, Project, Awarding Body, Brief Description
**Schema:** `Award` type within `Organization`, structured list

---

#### /about/employee-owned/

**URL:** `eptdesign.com/about/employee-owned/`
**Purpose:** Differentiate EPTDESIGN through the ESOP story; target clients who value firm stability and aligned incentives; also functions as talent recruitment content
**Target queries:** "employee-owned landscape architecture firm," "ESOP design firm," "landscape architecture firm ownership"
**Content requirements:**
- 700–900 words explaining the ESOP structure and what it means for clients and staff
- When the ESOP was established (confirm date)
- What 100% employee ownership means operationally
- Why it matters for clients: stability, principal continuity, aligned incentives
- Why it matters for staff: ownership culture, long-term commitment
- Scott Horsley quote on ESOP as a strategic choice
- CTA linking to careers/people
**Schema:** `Organization`, `BreadcrumbList`

---

### Section E: /people/ — Principal Pages That Build Personal Authority

Current principal pages are thin. Each principal should have a page that functions as a structured, citable professional profile — the equivalent of a strong LinkedIn page but on EPTDESIGN's own domain.

#### Principal Page Content Standard

Each page should include:

| Element | Current State | Required State |
|---|---|---|
| Full name | Present | Present |
| Title/role | Present | Present + expanded (Managing Principal vs. just "Principal") |
| Credentials | Partial | Full: FASLA, ASLA, LEED AP, AIA affiliation, state licenses |
| Professional biography | Short | 400–600 words minimum; career arc, design philosophy, notable projects |
| Featured projects | Absent | 3–5 projects with links to /work/ pages |
| Services led | Absent | Links to relevant /services/ pages |
| Locations served | Absent | Link to relevant /locations/ pages |
| Publications / press | Absent | Links to Veranda, Martha Stewart Living, LAM, etc. |
| Speaking / presentations | Absent | ASLA chapter presentations, university lectures |
| Quote / philosophy | Absent | 1–2 sentences in the principal's voice |
| Photo | Present | Present (professional, high-res) |
| Schema | Absent | `Person` with `hasCredential`, `worksFor`, `alumniOf` if applicable |

#### Priority Principal Pages

**Scott Horsley — Managing Principal**
- Primary credential: Managing Principal (ASLA member, confirm)
- Areas: Practice leadership, business development, client relationships
- Projects to feature: across sectors as firm lead
- Queries: "EPTDESIGN managing principal," "Scott Horsley landscape architect"

**Nord Eriksson FASLA — Estate Design**
- Primary credential: FASLA (highest priority credential to feature)
- Areas: Estate residential, private gardens, HNW clients
- Projects: Estate portfolio (with client permission)
- Press: Veranda, Martha Stewart Living (with links)
- Eckbo lineage connection
- Queries: "Nord Eriksson landscape architect," "Nord Eriksson FASLA," "estate landscape architect Pasadena"

**Stephen Carroll ASLA LEED AP — Sustainable / Healthcare**
- Primary credentials: ASLA, LEED AP
- Areas: Healthcare landscape design, sustainable site design, LEED-certified projects
- Projects: Kaiser Permanente, Cedars-Sinai AHSP, LEED Platinum project(s)
- Queries: "Stephen Carroll landscape architect," "LEED landscape architect Southern California"

**Dan Hoon — Multifamily / Housing**
- Primary credential: 6-state licensure (confirm states)
- Areas: Multifamily housing, mixed-use development, Western US developer market
- Projects: Village at Irvine Spectrum, other multifamily portfolio
- Queries: "Dan Hoon landscape architect," "multifamily landscape architect California"

**Ross Woodley — Residential**
- Primary areas: Residential design (scope to confirm with Alison Spicer)
- Projects: Residential portfolio
- Queries: "Ross Woodley landscape architect"

**Matthew Lysne — (Role to confirm)**
- Confirm role, credentials, and primary project areas with Alison Spicer

**Alison Spicer — Marketing Director**
- Optional: some firms include marketing/business development directors on the people page, as it humanizes the firm and provides a direct contact for press inquiries
- If included: note her role as the media/marketing contact; link her LinkedIn

---

## 3. Internal Linking Strategy

### The Topical Authority Web

Internal linking is how topical authority flows across the site. A service page that links to 5 project pages tells Google: this service is substantiated by real work. A project page that links to a principal page tells Google: this person has demonstrated expertise in this sector. A location page that links to service pages and project pages tells Google: this firm operates in this geography across these service types.

Without intentional internal linking, these connections don't register — even if the content exists.

### Linking Architecture by Page Type

**Homepage → Links To:**
- /services/ (hub)
- /locations/pasadena/ (primary location)
- 3–4 featured project pages (/work/)
- /about/history/
- /people/ (team overview)

**Service Pages → Links To:**
- Related service pages (e.g., /services/healthcare-landscape-design/ links to /services/sustainable-landscape-leed/)
- 4–6 relevant project pages (/work/)
- 1–2 principal pages (/people/)
- 1–3 location pages (/locations/) where service is offered
- /about/awards/ (for award-winning work in that sector)

**Project Pages → Links To:**
- Primary service category page (/services/)
- Secondary service category page(s) if applicable
- Principal(s) involved (/people/)
- Location page (/locations/) for the studio that led the project
- Related projects (3 "similar projects" links at bottom of page)

**Location Pages → Links To:**
- All service pages offered from that location
- Featured project pages in that geography
- Primary principal(s) associated with that studio
- /about/ page

**People Pages → Links To:**
- Service pages that principal leads
- Project pages that principal contributed to
- Location pages for studios where principal works
- Any press or publication links (external)

**About/History → Links To:**
- /about/awards/
- /about/employee-owned/
- /people/ (team)
- /services/ (overview)

### Linking Volume Targets

| Page Type | Outbound Internal Links Target | Inbound Internal Links Target |
|---|---|---|
| Homepage | 10–15 | — |
| /services/ hub | 12–18 | 3–5 |
| Individual service pages | 8–14 | 5–10 |
| Location pages | 8–12 | 4–8 |
| Project pages | 5–8 | 3–6 |
| People pages | 6–10 | 5–10 |
| /about/history/ | 8–12 | 4–6 |
| /about/awards/ | 5–8 | 3–5 |

### The Anchor Text Standard

Anchor text in internal links should be descriptive and keyword-relevant, not generic.

| Avoid | Use Instead |
|---|---|
| "click here" | "estate landscape design services" |
| "learn more" | "our healthcare landscape design portfolio" |
| "see projects" | "view Kaiser Permanente campus projects" |
| "meet the team" | "landscape architect Stephen Carroll, LEED AP" |
| "our services" | "landscape architecture services in Southern California" |

---

## 4. URL Structure Recommendations

### Clean URL Principles

EPTDESIGN's URLs should be:
- Lowercase only
- Hyphenated (not underscored)
- Descriptive without being verbose (under 65 characters where possible)
- Free of parameters, session IDs, or unnecessary numbers
- Logical and predictable (a user who reads the URL should know what the page is about)

### URL Audit: Existing vs. Recommended

| Page | Existing URL Pattern (assumed) | Recommended URL |
|---|---|---|
| Services hub | Does not exist | /services/ |
| Estate design service | Does not exist | /services/estate-residential-garden-design/ |
| Healthcare service | Does not exist | /services/healthcare-landscape-design/ |
| Campus service | Does not exist | /services/campus-landscape-architecture/ |
| Multifamily service | Does not exist | /services/multifamily-housing-landscape/ |
| Parks service | Does not exist | /services/parks-civic-design/ |
| Pasadena location | Does not exist | /locations/pasadena/ |
| Irvine location | Does not exist | /locations/irvine/ |
| Firm history | Does not exist | /about/history/ |
| Awards | Does not exist | /about/awards/ |
| ESOP story | Does not exist | /about/employee-owned/ |
| Glendale Narrows project | /work/glendale-narrows (assumed) | /work/glendale-narrows-riverwalk/ |
| Kaiser Permanente projects | /work/kaiser-1 (assumed) | /work/kaiser-permanente-[location]-campus/ |

**Assumption:** The existing /work/ project slugs may or may not follow clean URL conventions. Alison Spicer should audit current project URLs before redirecting. If existing URLs have any inbound links, 301 redirects are required.

### URL Redirect Requirements

If any existing pages are renamed or restructured:
- All old URLs must 301-redirect to new URLs
- Do not let old URLs 404 — any inbound link equity is lost on a 404
- Confirm Cloudflare supports redirect rules (it does) and implement at the CDN level for speed

---

## 5. Priority Build Order

### The Decision Logic

Pages are prioritized based on four factors:
1. **Search volume** — how many people are searching for this
2. **Business impact** — does it support high-margin or strategic work?
3. **Entity clarity** — does it help Google understand what EPTDESIGN is?
4. **Build complexity** — how much content and design effort is required?

### Phase 1 — Foundation (Months 1–2) — "Google Needs to Know Who We Are"

These pages establish the entity and prevent further SEO drift. None of them require new design components — they are content-first additions to existing sections.

| Priority | Page | Rationale | Est. Effort |
|---|---|---|---|
| 1 | `/about/history/` | Highest entity impact; no design required | 2 days copy |
| 2 | `/about/awards/` | Entity credibility; consolidation of existing info | 1 day copy |
| 3 | `/about/employee-owned/` | Differentiation; entity signal | 1 day copy |
| 4 | `/people/nord-eriksson/` (expanded) | FASLA; estate service lead; editorial press | 1.5 days copy |
| 5 | `/people/stephen-carroll/` (expanded) | LEED AP; healthcare lead | 1.5 days copy |
| 6 | **Unblock AI crawlers in robots.txt** | Zero-effort, immediate impact | 30 minutes |
| 7 | **Complete 5 GBP profiles** | Local pack prerequisite | 2–3 days |
| 8 | **Add Organization + LocalBusiness schema** | Entity prerequisite | 1 day dev |

---

### Phase 2 — Service Architecture (Months 2–5) — "We Need Pages That Rank"

Build the /services/ section in order of business priority.

| Priority | Page | Rationale | Est. Effort |
|---|---|---|---|
| 9 | `/services/landscape-architecture/` | Top-of-funnel hub; all buyer types | 2 days copy + design |
| 10 | `/services/` (hub) | Navigation anchor for service section | 1 day copy |
| 11 | `/services/estate-residential-garden-design/` | Highest margin; Nord Eriksson lead | 2 days copy |
| 12 | `/services/healthcare-landscape-design/` | Kaiser + Cedars-Sinai authority; AIA award | 2 days copy |
| 13 | `/services/campus-landscape-architecture/` | Pomona College + UCLA authority | 2 days copy |
| 14 | `/services/multifamily-housing-landscape/` | Dan Hoon expertise; Irvine Company | 2 days copy |
| 15 | `/services/sustainable-landscape-leed/` | Differentiator; Stephen Carroll | 1.5 days copy |
| 16 | `/services/parks-civic-design/` | Glendale Narrows ENR win | 1.5 days copy |
| 17 | `/services/urban-design-planning/` | Google Backlot; developer market | 1.5 days copy |
| 18 | `/services/master-planning/` | Institutional; relationship-depth proof | 1 day copy |

---

### Phase 3 — Location Pages (Months 3–6) — "We Need to Be Found Locally"

| Priority | Page | Rationale | Est. Effort |
|---|---|---|---|
| 19 | `/locations/pasadena/` | HQ; primary market; highest local search volume | 2 days copy |
| 20 | `/locations/irvine/` | Developer market; Irvine Company; Dan Hoon | 1.5 days copy |
| 21 | `/locations/santa-barbara/` | Estate market; Nord Eriksson | 1.5 days copy |
| 22 | `/locations/san-diego/` | Southern market; civic/healthcare | 1.5 days copy |
| 23 | `/locations/claremont/` | Colleges; secondary residential | 1 day copy |

---

### Phase 4 — Project Page Refresh (Months 4–9) — "87 Pages Need to Pull Their Weight"

| Priority | Projects | Rationale | Est. Effort |
|---|---|---|---|
| 24 | Cedars-Sinai AHSP | AIA award; healthcare lead project | 1 day |
| 25 | Glendale Narrows Riverwalk | ENR award; civic lead project | 1 day |
| 26 | Google Backlot (Venice) | High-profile client; tech/urban | 1 day |
| 27 | UCLA Botanical Garden | Institutional; botanical credentials | 1 day |
| 28 | Kaiser Permanente (all 4) | Healthcare relationship cluster | 3 days (cluster) |
| 29 | Pomona College (all 4) | Education relationship cluster | 3 days (cluster) |
| 30 | Village at Irvine Spectrum | Multifamily; OC market | 1 day |
| 31 | Remaining 76 project pages | Systematic content lift | Ongoing / batched |

---

### Phase 5 — Authority & Thought Leadership (Months 6–18) — "Content That Gets Cited"

| Priority | Action | Rationale | Est. Effort |
|---|---|---|---|
| 32 | Nord Eriksson byline article (estate design philosophy) | FASLA authority; AI citation candidate | 1 week |
| 33 | Stephen Carroll byline (LEED landscape) | LEED authority; sustainability queries | 1 week |
| 34 | Eckbo lineage essay (history section) | AI citation; design history queries | 1 week |
| 35 | Dan Hoon byline (multifamily amenity trends) | Developer audience; LinkedIn primary | 1 week |
| 36 | ASLA citation campaign | Professional directory; DR boost | 2 weeks |
| 37 | University backlink requests (Pomona, UCLA) | High-DR institutional links | 2 weeks |
| 38 | Partner backlink requests (HOK, Gensler, Trammell Crow) | Architecture firm co-citations | 1 month |
| 39 | Houzz Pro profile completion | HNW residential discovery | 1 week |

---

## 6. Schema Markup Map

Schema markup is machine-readable structured data that tells search engines and AI systems exactly what a page is about. Without it, every classification must be inferred. With it, every key fact is explicitly declared.

EPTDESIGN currently has no schema markup anywhere. The following map defines which schema types apply to which page types and what the key properties are.

### Schema Type by Page Type

| Page Type | Primary Schema | Secondary Schema | Key Properties |
|---|---|---|---|
| **Homepage** | `Organization` | `LocalBusiness` | name, foundingDate, numberOfEmployees, address (HQ), url, logo, sameAs (social profiles, ASLA), description, areaServed |
| **Services hub** | `Service` | `Organization` | serviceType, provider, areaServed, description |
| **Individual service pages** | `Service` | `FAQPage` | name, serviceType, provider (EPTDESIGN), areaServed, hasOfferCatalog, description |
| **Location pages** | `LocalBusiness` | `GeoCoordinates` | name ("EPTDESIGN — Pasadena"), address (PostalAddress), telephone, openingHours, geo (GeoCoordinates), url, parentOrganization |
| **Project pages** | `CreativeWork` | `Person`, `Organization` | name, description, locationCreated (PostalAddress), dateCreated, creator (Person — principal), contributor (Organization — EPTDESIGN), award (if applicable), keywords (service category) |
| **People pages** | `Person` | `ProfilePage` | name, jobTitle, honorificSuffix (FASLA / ASLA / LEED AP), worksFor (EPTDESIGN), hasCredential, description, url, sameAs (LinkedIn), knowsAbout (service areas) |
| **/about/history/** | `Organization` | `Event` (milestones) | foundingDate, foundingLocation, description, member (key principals), award |
| **/about/awards/** | `Organization` | `AchievementCertification` | award (name, year, description), recognizedBy (ASLA / AIA / ENR) |
| **Blog/Our Stories posts** | `Article` | `Person` (author) | headline, author, datePublished, dateModified, publisher, description, image |
| **All pages** | `BreadcrumbList` | — | itemListElement (ordered crumbs: Home > Section > Page) |

### Schema Priority Implementation Order

| Priority | Schema Type | Page(s) | Reason |
|---|---|---|---|
| 1 | `Organization` | Homepage, /about/ | Entity recognition — most critical |
| 2 | `LocalBusiness` | All 5 /locations/ pages | Local pack eligibility |
| 3 | `Person` | All /people/ pages | Principal entity clarity |
| 4 | `BreadcrumbList` | All pages | Site structure signal |
| 5 | `Service` | All /services/ pages | Service category classification |
| 6 | `FAQPage` | Service pages + key /about/ pages | Rich result eligibility; AI citation |
| 7 | `CreativeWork` | All /work/ project pages | Portfolio classification |
| 8 | `Article` | All /our-stories/ posts | Content type classification |

### Organization Schema — Minimum Required Properties (Homepage)

```json
{
  "@context": "https://schema.org",
  "@type": ["Organization", "LocalBusiness"],
  "name": "EPTDESIGN",
  "legalName": "EPT Design Inc.",
  "url": "https://www.eptdesign.com",
  "logo": "https://www.eptdesign.com/[logo-url]",
  "foundingDate": "1962",
  "numberOfEmployees": {
    "@type": "QuantitativeValue",
    "minValue": 35,
    "maxValue": 40
  },
  "description": "EPTDESIGN is a landscape architecture and urban design firm founded in 1962, headquartered in Pasadena, California, with studios in Irvine, Claremont, Santa Barbara, and San Diego. 100% employee-owned.",
  "address": {
    "@type": "PostalAddress",
    "streetAddress": "[Pasadena Street Address]",
    "addressLocality": "Pasadena",
    "addressRegion": "CA",
    "postalCode": "[ZIP]",
    "addressCountry": "US"
  },
  "telephone": "[Pasadena Phone]",
  "areaServed": ["Los Angeles County", "Orange County", "San Bernardino County", "Santa Barbara County", "San Diego County"],
  "sameAs": [
    "https://www.linkedin.com/company/eptdesign",
    "https://www.asla.org/[member-profile]",
    "[other verified profiles]"
  ],
  "knowsAbout": ["Landscape Architecture", "Urban Design", "Estate Garden Design", "Healthcare Landscape Design", "Campus Landscape Architecture", "Multifamily Housing Landscape", "Parks and Civic Design", "Sustainable Site Design"]
}
```

**Assumption:** Legal name "EPT Design Inc." is assumed. Confirm exact legal entity name with Scott Horsley or Alison Spicer before publishing schema. Similarly confirm all addresses, phone numbers, and founding year with primary sources.

### LocalBusiness Schema — Location Page Template

Each of the five location pages should include a `LocalBusiness` schema instance with:
- `name`: "EPTDESIGN — [City]" (e.g., "EPTDESIGN — Irvine")
- `parentOrganization`: Reference to the main EPTDESIGN Organization
- `address`: Specific studio address
- `geo`: Latitude/longitude (for local pack eligibility)
- `telephone`: Studio-specific phone if different from HQ
- `url`: The specific location page URL (not the homepage)

### FAQPage Schema — Service Page Template

Each service page should include a `FAQPage` schema with 3–5 questions and answers structured around:
- What the service is
- Who the ideal client is
- What the process looks like
- What geographic area is served
- What makes EPTDESIGN's approach distinctive in this service area

These questions should appear as visible content on the page (not hidden), both because Google requires this for FAQ rich results and because they address real buyer questions at the consideration stage.

---

## Appendix A: Page Count Summary

| Section | Existing Pages | New Pages Required | Total |
|---|---|---|---|
| /services/ | 0 | 10 (hub + 9 service pages) | 10 |
| /locations/ | 0 | 5 | 5 |
| /work/ | 87 | 0 new, 87 to refresh | 87 |
| /about/ | 1 | 3 (history, awards, ESOP) | 4 |
| /people/ | 7 (approx.) | 0 new, 7 to expand | 7 |
| /our-stories/ | ~12 (approx.) | Ongoing | 12+ |
| Homepage | 1 | 0 new, 1 to refresh | 1 |
| **Total** | **~108** | **18 new** | **~126** |

---

## Appendix B: Open Questions for Alison Spicer

The following questions require internal clarification before content can be finalized for specific pages:

| Question | Affects |
|---|---|
| What are Dan Hoon's 6 state licenses? | /people/dan-hoon/, /services/multifamily-housing-landscape/ |
| Is the Garrett Eckbo lineage documentable with a primary source? | /about/history/ |
| What year was the ESOP established? | /about/employee-owned/, /about/history/ |
| Which Kaiser Permanente facilities can be named publicly? | Kaiser project pages, /services/healthcare-landscape-design/ |
| Is the Pomona College relationship permitted for public case studies? | Pomona project pages, /services/campus-landscape-architecture/ |
| What is Matthew Lysne's role and primary project areas? | /people/matthew-lysne/ |
| What is the exact legal entity name for schema? | Organization schema on homepage |
| What is EPTDESIGN's primary phone number per studio? | LocalBusiness schema, /locations/ pages |
| Are there any existing /work/ URLs with inbound links that should not be changed? | Redirect planning |
| Has Cloudflare's AI crawler block been confirmed as intentional? | robots.txt remediation |
| What CMS is the site built on? (affects schema implementation method) | Technical implementation |

---

*Document end. This architecture should be reviewed with Alison Spicer and the web team before build begins. Phase 1 actions (robots.txt, GBP, schema, /about/history/) can begin immediately without a new design system. All remaining phases require coordination with the site's web development resource.*
