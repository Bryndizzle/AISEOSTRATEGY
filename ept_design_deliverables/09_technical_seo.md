# 09 — Technical SEO Audit & Implementation Plan
## EPTDESIGN | Priority 1: Complete Before Any Content Work

**Prepared:** February 2026
**Status:** Immediate action required
**Audience:** Internal (Alison + web/IT contact); forward relevant sections to Cloudflare admin

---

> **Why this document comes first:** Content improvements, schema implementation, and link building all depend on crawlers being able to access the site. Right now, the most important AI platforms — ChatGPT, Google's AI Overviews, and Perplexity — cannot read EPTDESIGN's website. That is the single most consequential issue to fix. Everything else in this strategy is downstream of that.

---

## 1. CRITICAL ISSUES

These four issues must be resolved before any other SEO work begins. Completing them in order is recommended: AI crawler access first, then address data, then GBP corrections.

---

### 1a. AI Crawler Blocking — Cloudflare Managed Content Settings

**The Problem**

EPTDESIGN's Cloudflare configuration is currently blocking every major AI crawler. This is the result of two overlapping settings:

1. **Cloudflare Content-Signal:** `search=yes, ai-train=no` — This tells AI systems that traditional search indexing is permitted but AI training is not. This distinction is meaningful and appropriate: EPTDESIGN does not want its project photography or design work used to train AI models.

2. **robots.txt (via Cloudflare Managed Content):** All AI bots are currently listed as blocked. This means crawling is blocked entirely — not just training. The consequence is that AI systems that would cite EPTDESIGN in responses (ChatGPT, Google AI Overviews, Perplexity, Apple Intelligence) cannot read the site at all.

**The Critical Distinction: Crawling vs. Training**

These are not the same thing. Blocking training is a legitimate business decision. Blocking crawling prevents citations.

- **Training:** An AI company uses your content to modify its underlying model weights. The `ai-train=no` Content-Signal addresses this.
- **Crawling for citations:** An AI reads your page to answer a user's question and credits your site. This is equivalent to Google reading your page to serve a search result. Blocking this means EPTDESIGN is invisible to AI citation systems.

Competitor Sasaki (DR 70) currently receives 88 AI citations. EPTDESIGN receives zero. The robots.txt configuration is a primary reason.

**What to Fix in Cloudflare**

Log into the Cloudflare dashboard for eptdesign.com. Navigate to: **Security > Bots > Bot Management** (or **Managed Rules**, depending on your plan tier). Also check **Scrape Shield** and any **WAF custom rules** that explicitly block user-agents.

The robots.txt file served by Cloudflare's Managed Content system controls the `User-agent` directives. You will need to edit this file to selectively allow AI citation bots while maintaining the training block signal.

**Bots to Allow (Edit robots.txt)**

| Bot Name | Owner | Why Allow |
|---|---|---|
| `GPTBot` | OpenAI / ChatGPT | ChatGPT citations and ChatGPT Search results |
| `Google-Extended` | Google | Google AI Overviews (formerly SGE); also Gemini |
| `Applebot-Extended` | Apple | Apple Intelligence responses |
| `PerplexityBot` | Perplexity AI | Perplexity is the fastest-growing AI search engine |
| `OAI-SearchBot` | OpenAI | ChatGPT's dedicated search crawler (separate from GPTBot) |

**Bots to Keep Blocked**

| Bot Name | Reason |
|---|---|
| `CCBot` | Common Crawl — primary training dataset source; block is appropriate |
| `Bytespider` | ByteDance/TikTok — no citation value, high training risk |
| `meta-externalagent` | Meta AI training crawler; no citation benefit |
| `Diffbot` | Data extraction for commercial resale; no citation benefit |

**Updated robots.txt — Replace Existing AI-Related Directives With:**

```
# AI Citation Crawlers — ALLOWED (reading for responses, not training)
User-agent: GPTBot
Allow: /

User-agent: OAI-SearchBot
Allow: /

User-agent: Google-Extended
Allow: /

User-agent: Applebot-Extended
Allow: /

User-agent: PerplexityBot
Allow: /

# AI Training Crawlers — BLOCKED (training use not permitted)
User-agent: CCBot
Disallow: /

User-agent: Bytespider
Disallow: /

User-agent: meta-externalagent
Disallow: /

User-agent: Diffbot
Disallow: /

# All other crawlers follow standard rules below
User-agent: *
Allow: /

Sitemap: https://eptdesign.com/sitemap.xml
```

**Maintain ai-train=no Content-Signal**

The Cloudflare Content-Signal setting (`ai-train=no`) should remain as-is. This communicates the training restriction at the platform level and is respected by compliant AI systems. It is independent of the robots.txt crawling permission and does not need to change.

**Verification After Implementation**

After updating robots.txt, verify the change is live by visiting: `https://eptdesign.com/robots.txt` in a browser. The updated directives should be visible within minutes of saving in Cloudflare.

You can also test user-agent blocking using Google Search Console's URL Inspection tool or a third-party robots.txt tester (e.g., technicalseo.com/tools/robots-txt-tester/).

**Expected Timeline for AI Citation Impact**

- Week 1: Crawlers begin accessing site once robots.txt is updated
- Weeks 2-4: AI systems index content and begin surfacing it in responses
- Weeks 4-8: First verifiable AI citations expected for branded queries ("EPTDESIGN," "EPT Design landscape architecture Pasadena")
- Weeks 8-16: Topical citations possible for service + location queries if supporting content is in place

> **Assumption:** Timeline assumes compliant AI crawler behavior. GPTBot, Google-Extended, and PerplexityBot all respect robots.txt directives. Crawl frequency after unblocking depends on the crawler's own schedule and the site's overall authority signal.

---

### 1b. Cloudflare Bot Protection Blocking Ahrefs Crawler (403 Responses)

**The Problem**

The Ahrefs site crawler (user-agent: `AhrefsBot`) is currently receiving 403 Forbidden responses from EPTDESIGN's domain. This means Ahrefs cannot audit the site's technical health, index its internal link structure, or track keyword rankings accurately.

This is a monitoring problem: it prevents EPTDESIGN from using Ahrefs to measure the impact of this strategy. If you cannot measure, you cannot manage.

**Why This Happens**

Cloudflare's aggressive bot protection mode blocks many legitimate SEO tool crawlers by default. This is a misconfiguration rather than an intentional decision — Ahrefs poses no security risk.

**Fix**

In Cloudflare dashboard: **Security > WAF > Custom Rules** (or **Tools > IP Access Rules**).

Add an allow rule for AhrefsBot by user-agent string:

- Navigate to **Security > WAF > Custom Rules**
- Create a new rule: `(http.user_agent contains "AhrefsBot")` → Action: **Skip** (bypass WAF)

Alternatively, whitelist the Ahrefs IP ranges (published at ahrefs.com/robot) using **Security > Tools > IP Access Rules** with action: **Allow**.

Also check for and allow the following SEO/monitoring user-agents if blocked:
- `Screaming Frog SEO Spider` (if used for on-site audits)
- `Semrushbot`
- `Moz`

**Implication for This Strategy**

Until Ahrefs crawling is restored, baseline data for organic keywords and traffic will remain at zero (which is what the current audit shows). This is an instrumentation problem, not necessarily a true reflection of the site's performance — though the site's performance is also genuinely poor and should not be assumed to be better than reported.

---

### 1c. Website Address Error — Pasadena Office

**The Problem**

EPTDESIGN's website currently lists the Pasadena headquarters address as:

> 7 N Fair Oaks Ave, Pasadena, CA

The correct address — confirmed by Google Business Profile, Yelp, and Los Angeles County property records — is:

> 234 N El Molino Ave, Suite 100, Pasadena, CA 91101

This is a NAP (Name, Address, Phone) inconsistency. It signals to search engines and AI systems that there is uncertainty about the firm's identity and location. For local SEO and AI entity confirmation, NAP consistency across all platforms is foundational.

**Fix — Website**

Update the Pasadena address on all pages where it appears:
- Contact page
- Footer (if address appears in footer markup)
- About page (if address listed)
- Any embedded Google Maps widget (update map pin if hardcoded)
- Schema markup (see Section 2 below)

**Fix — Canonical Address to Use Everywhere**

```
EPTDESIGN
234 N El Molino Ave, Suite 100
Pasadena, CA 91101
```

Confirm the phone number associated with this address is consistent: verify it matches GBP, website, and any directory listings before updating schema markup.

---

### 1d. HTTP → HTTPS on All GBP Website URLs

**The Problem**

The website URLs listed on EPTDESIGN's Google Business Profile entries for one or more studio locations are using `http://` rather than `https://`. This causes:

1. A minor trust signal degradation in Google's systems
2. A potential redirect chain: user clicks GBP link → HTTP URL → Cloudflare redirects to HTTPS → longer load time
3. Inconsistency that AI systems may interpret as separate entity variants

**Fix**

Log into Google Business Profile (business.google.com) for each of the 5 studio locations. For each:

1. Click **Edit Profile**
2. Scroll to **Website**
3. Confirm the URL begins with `https://` not `http://`
4. Update if necessary and save

Also verify that the website URLs listed in GBP point to location-specific pages where those exist (e.g., `https://eptdesign.com/studio/irvine/`) rather than all pointing to the homepage. Distinct landing pages for each studio improve local relevance signals.

---

## 2. Schema Markup Implementation Plan

Schema markup is structured data added to HTML pages that helps search engines and AI systems understand what a page is about, who the entity is, and how pieces of content relate to each other. EPTDESIGN currently has no schema markup on any pages. This is a significant gap for a firm that relies on local search visibility and entity recognition.

Implementation should be done in JSON-LD format, placed in the `<head>` of each relevant page. If the site runs on WordPress with Yoast SEO, Yoast can generate some schema automatically — but project pages, person pages, and studio-specific pages will require manual or custom implementation.

---

### Schema Type 1: Organization (Firm-Level)

**Where:** Homepage and all pages (place in site-wide `<head>` template)
**Purpose:** Establishes EPTDESIGN as a known entity — name, founding date, locations, social profiles, description

```json
{
  "@context": "https://schema.org",
  "@type": "Organization",
  "name": "EPTDESIGN",
  "alternateName": "EPT Design",
  "url": "https://eptdesign.com",
  "logo": "https://eptdesign.com/wp-content/uploads/eptdesign-logo.png",
  "foundingDate": "1962",
  "description": "Landscape architecture and urban design firm founded in 1962, headquartered in Pasadena, California. Employee-owned (ESOP). Five studios serving Southern California.",
  "numberOfEmployees": {
    "@type": "QuantitativeValue",
    "minValue": 35,
    "maxValue": 40
  },
  "address": {
    "@type": "PostalAddress",
    "streetAddress": "234 N El Molino Ave, Suite 100",
    "addressLocality": "Pasadena",
    "addressRegion": "CA",
    "postalCode": "91101",
    "addressCountry": "US"
  },
  "sameAs": [
    "https://www.linkedin.com/company/eptdesign",
    "https://www.instagram.com/eptdesign",
    "https://www.houzz.com/pro/eptdesign"
  ]
}
```

> **Assumption:** Social profile URLs above are placeholders — confirm actual LinkedIn, Instagram, and Houzz URLs and update before publishing.

---

### Schema Type 2: LocalBusiness (Each Studio)

**Where:** Studio/location landing pages (one per studio)
**Purpose:** Associates each office with its city for local search; enables Google to show the right location for city-specific queries

Example — Pasadena headquarters:

```json
{
  "@context": "https://schema.org",
  "@type": "LocalBusiness",
  "name": "EPTDESIGN — Pasadena",
  "image": "https://eptdesign.com/wp-content/uploads/pasadena-studio.jpg",
  "url": "https://eptdesign.com/studio/pasadena/",
  "telephone": "[CONFIRM PHONE NUMBER]",
  "address": {
    "@type": "PostalAddress",
    "streetAddress": "234 N El Molino Ave, Suite 100",
    "addressLocality": "Pasadena",
    "addressRegion": "CA",
    "postalCode": "91101",
    "addressCountry": "US"
  },
  "geo": {
    "@type": "GeoCoordinates",
    "latitude": 34.1478,
    "longitude": -118.1445
  },
  "openingHoursSpecification": {
    "@type": "OpeningHoursSpecification",
    "dayOfWeek": ["Monday","Tuesday","Wednesday","Thursday","Friday"],
    "opens": "08:00",
    "closes": "17:00"
  },
  "parentOrganization": {
    "@type": "Organization",
    "name": "EPTDESIGN",
    "url": "https://eptdesign.com"
  }
}
```

Replicate this schema for Irvine, Claremont, Santa Barbara, and San Diego studios with the correct addresses, phone numbers, and geo-coordinates for each.

---

### Schema Type 3: Person (Principals)

**Where:** Bio/team pages for each principal
**Purpose:** Establishes principals as named entities linked to EPTDESIGN; enables AI systems to surface them as authoritative voices

```json
{
  "@context": "https://schema.org",
  "@type": "Person",
  "name": "Nord Eriksson",
  "honorificSuffix": "FASLA",
  "jobTitle": "Principal",
  "worksFor": {
    "@type": "Organization",
    "name": "EPTDESIGN",
    "url": "https://eptdesign.com"
  },
  "sameAs": [
    "https://www.linkedin.com/in/[norderikssonlinkedin]",
    "https://www.asla.org/memberprofile/[id]"
  ]
}
```

Repeat for Stephen Carroll, Scott Horsley, Matthew Lysne, and all other named principals. The `sameAs` links to LinkedIn and ASLA member profiles are the highest-value properties — they create cross-platform entity connections that AI systems use to verify identity.

---

### Schema Type 4: CreativeWork / Project Pages

**Where:** Each of the 87 project pages
**Purpose:** Identifies projects as landscape architecture works with named collaborators, client, and location

```json
{
  "@context": "https://schema.org",
  "@type": "CreativeWork",
  "name": "Narrows Riverwalk",
  "description": "A $31 million urban riverwalk project along the Los Angeles River in Glendale, California. Phase 3 completion expected 2027.",
  "creator": {
    "@type": "Organization",
    "name": "EPTDESIGN",
    "url": "https://eptdesign.com"
  },
  "locationCreated": {
    "@type": "Place",
    "name": "Glendale, CA",
    "address": {
      "@type": "PostalAddress",
      "addressLocality": "Glendale",
      "addressRegion": "CA",
      "addressCountry": "US"
    }
  },
  "keywords": "landscape architecture, urban design, riverwalk, Los Angeles River, Glendale"
}
```

This schema can be templated: project name, description, and location change per page; the creator block stays constant. If the site uses a page template for project pages, a developer can inject this schema dynamically using Yoast custom fields or an ACF (Advanced Custom Fields) integration.

---

### Schema Type 5: FAQPage (Service Pages)

**Where:** Key service pages (Landscape Architecture, Urban Design, Community Planning, etc.)
**Purpose:** Enables FAQ rich results in Google; also provides directly extractable answers for AI Overview responses

```json
{
  "@context": "https://schema.org",
  "@type": "FAQPage",
  "mainEntity": [
    {
      "@type": "Question",
      "name": "What types of projects does EPTDESIGN work on?",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "EPTDESIGN specializes in landscape architecture and urban design for institutional, civic, healthcare, university, and mixed-use projects across Southern California. Notable projects include the Narrows Riverwalk in Glendale, campus landscapes for Pomona College and CSU Fullerton, and healing gardens for Cedars-Sinai and Kaiser Permanente."
      }
    },
    {
      "@type": "Question",
      "name": "Where is EPTDESIGN located?",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "EPTDESIGN operates five studios: Pasadena (headquarters at 234 N El Molino Ave, Suite 100), Irvine, Claremont, Santa Barbara, and San Diego."
      }
    }
  ]
}
```

Write 3-5 relevant FAQ questions per service page, grounded in the actual questions clients ask before engaging a landscape architecture firm.

---

### Schema Type 6: BreadcrumbList

**Where:** All interior pages
**Purpose:** Helps search engines understand site hierarchy; improves click-through rates via rich results

```json
{
  "@context": "https://schema.org",
  "@type": "BreadcrumbList",
  "itemListElement": [
    {
      "@type": "ListItem",
      "position": 1,
      "name": "Home",
      "item": "https://eptdesign.com"
    },
    {
      "@type": "ListItem",
      "position": 2,
      "name": "Projects",
      "item": "https://eptdesign.com/projects/"
    },
    {
      "@type": "ListItem",
      "position": 3,
      "name": "Narrows Riverwalk",
      "item": "https://eptdesign.com/projects/narrows-riverwalk/"
    }
  ]
}
```

Yoast SEO can generate BreadcrumbList schema automatically if breadcrumbs are enabled in Yoast settings. Verify this is active.

---

### Schema Type 7: AggregateRating

**Where:** Homepage and LocalBusiness schemas
**Purpose:** Displays star ratings in search results; increases click-through rate
**Status:** Implement once Google Business Profile reviews exceed 10 per location. Current total across all 5 locations is 5 reviews — schema should not be added yet as sparse ratings can suppress rather than elevate results.

Prioritise GBP review-building first (see Section 6), then add AggregateRating schema once a meaningful baseline exists.

---

## 3. Indexation and Crawl Health

### Sitemap

EPTDESIGN uses Yoast SEO, which generates an XML sitemap automatically at `https://eptdesign.com/sitemap.xml`. The sitemap exists and references the 87 project pages.

**The Problem**

All 87 project pages show a `lastmod` date of July 2021. Search engines use `lastmod` to prioritise crawl budget. Pages with a stale `lastmod` date are crawled less frequently. If project pages are not being recrawled, updated metadata, schema markup, or content changes will not be indexed promptly.

**Fix**

After each wave of content updates (see deliverable 10 — Content Strategy), update the `lastmod` field in Yoast for each refreshed page. This is done automatically if you use Yoast's sitemap regeneration on publish/update.

- Set Yoast to regenerate sitemap on page save: Yoast SEO > Search Appearance > verify "XML Sitemaps" is enabled
- After updating project pages, re-submit the sitemap in Google Search Console: Sitemaps > Enter sitemap URL > Submit
- Verify Google is crawling updated pages via the URL Inspection tool

**Sitemap Structure Recommendation**

Break the sitemap into sub-sitemaps by section once schema and content work begins:

```
sitemap_index.xml
  ├── sitemap-pages.xml         (service pages, about, contact)
  ├── sitemap-projects.xml      (87 project pages)
  ├── sitemap-team.xml          (principal/bio pages)
  └── sitemap-locations.xml     (5 studio landing pages)
```

This structure helps search engines allocate crawl budget appropriately and surfaces team/location pages which are currently likely buried.

---

### robots.txt Review (Non-AI Directives)

Beyond the AI bot changes described in Section 1a, audit the full robots.txt for unintended blocks.

Common mistakes to check:
- Is `/projects/` or any project subdirectory disallowed? If yes, this explains the indexed page deficiency.
- Are admin URLs (`/wp-admin/`) correctly blocked? They should be.
- Are any media directories (`/wp-content/uploads/`) blocked? Project photography should be crawlable for Google Image Search.

Target robots.txt state:
```
User-agent: *
Disallow: /wp-admin/
Allow: /wp-admin/admin-ajax.php
Allow: /

Sitemap: https://eptdesign.com/sitemap.xml
```

Then add the AI bot directives from Section 1a below this block.

---

### Crawl Budget for 87 Project Pages

With DR 29 and low external authority, Google allocates a relatively small crawl budget to eptdesign.com. 87 project pages competing for that budget means low-value or thin pages can crowd out high-value ones.

**Recommendations:**

1. Audit project pages for thin content (under 300 words of unique text). Pages that are mostly images with a one-line caption should either be consolidated or expanded before being included in the sitemap.
2. Consider noindexing archived or very old projects that are unlikely to generate search traffic, to concentrate crawl budget on active and high-quality pages.
3. Improve internal linking from the homepage and main Projects page to individual project pages — this signals importance to Google and increases crawl frequency.

---

## 4. On-Page Technical Fixes

### H1 Tags

Every page should have exactly one H1 tag that is distinct from the page title tag. Project pages likely use the project name as an H1. Verify:
- Every project page has an H1
- H1 is not duplicated (two H1s on one page is a common WordPress theme issue)
- H1 contains the primary keyword for the page (e.g., "Narrows Riverwalk — Urban Landscape Design, Glendale CA")

Audit with Screaming Frog or Ahrefs Site Audit (once 403 issue is resolved).

---

### Meta Descriptions

Meta descriptions do not directly affect rankings but significantly affect click-through rates from search results. Yoast can auto-generate them from page content, but auto-generated descriptions are rarely optimised.

Write custom meta descriptions for:
- All service pages
- All studio location pages
- The 20 highest-traffic potential project pages (prioritise by project scale and client prestige)
- Homepage

**Meta description formula:**
`[What the project/service is] by [EPTDESIGN] in [Location]. [One specific differentiator or outcome]. [Soft CTA or credential].`

Example — Narrows Riverwalk:
> "Landscape architecture for the Narrows Riverwalk in Glendale, CA — a $31M urban riverfront project by EPTDESIGN. Transforming the LA River corridor for public recreation and ecological resilience."

Character limit: 150-160 characters.

---

### Title Tag Formula

Apply a consistent, keyword-rich title tag formula across the site:

```
[Project or Service Name] | Landscape Architecture | [City, CA] | EPTDESIGN
```

Examples:
- `Narrows Riverwalk | Urban Landscape Design | Glendale, CA | EPTDESIGN`
- `University Campus Landscape Architecture | Southern California | EPTDESIGN`
- `Landscape Architecture Firm | Pasadena, CA | Since 1962 | EPTDESIGN`

Keep under 60 characters where possible. "Since 1962" is a trust signal that can be used on the homepage title and About page, but omit from project pages where it competes with location/service terms.

---

### Image Alt Text

EPTDESIGN's project photography is a significant content asset. Currently it is likely serving no SEO value because alt text is missing or generic.

**Fix:** For each project page photograph, write descriptive alt text:

Formula: `[What is shown] — [Project Name], [Location] — EPTDESIGN`

Example: `Pedestrian promenade along the LA River — Narrows Riverwalk, Glendale CA — EPTDESIGN landscape architecture`

Alt text serves two purposes: Google Image Search visibility (project photography queries are a legitimate traffic source for design firms) and accessibility compliance.

---

### Internal Linking

EPTDESIGN's 87 project pages are likely operating as silos — individual pages with no links to related projects, relevant service pages, or studio location pages.

**Internal linking priorities:**

1. Each project page should link to the relevant studio location page (e.g., Glendale Riverwalk → Pasadena studio page)
2. Each project page should link to the relevant service page (e.g., Riverwalk → Urban Design service page)
3. Service pages should link to 3-5 representative project pages
4. The Projects index page should feature priority projects prominently with direct links
5. Principal bio pages should link to projects they led

A simple internal linking structure transforms isolated project pages into a coherent authority network. This also increases pages-per-session from users exploring the portfolio, which is a positive engagement signal.

---

## 5. Core Web Vitals and Mobile Performance

### Mobile-First

Google indexes the mobile version of pages. With Cloudflare handling CDN and security layers, ensure:
- No render-blocking JavaScript that is not deferred on mobile
- Cloudflare's Rocket Loader (if enabled) is not conflicting with any site scripts
- Cloudflare's HTML/CSS/JS minification is enabled (Speed > Optimization > Auto Minify)

Test mobile performance at: Google PageSpeed Insights (pagespeed.web.dev)
Target score: 70+ on mobile for key pages.

---

### Image Optimization

Project photography is the heaviest element on most pages. Current format is likely JPEG at original resolution.

**Target:**
- Convert all project photography to WebP format (30-40% smaller than JPEG at equivalent quality)
- Maximum file size: 150KB per image for in-page hero images; 80KB for thumbnails
- Implement lazy loading for images below the fold (`loading="lazy"` attribute)
- Use responsive images (`srcset`) to serve appropriate sizes for mobile vs. desktop

If the site runs on WordPress, use a plugin such as ShortPixel or Imagify to automate WebP conversion and compression. Cloudflare also offers automatic WebP serving via Polish (Speed > Optimization > Polish: Lossless or Lossy).

---

### Core Web Vitals Targets

| Metric | Target | Notes |
|---|---|---|
| LCP (Largest Contentful Paint) | Under 2.5 seconds | Hero images on project pages are likely the LCP element — optimise those first |
| FID / INP (Interaction to Next Paint) | Under 200ms | Ensure no heavy JavaScript event handlers on key pages |
| CLS (Cumulative Layout Shift) | Under 0.1 | Set explicit width/height attributes on all images to prevent layout shift |

Measure using:
- Google Search Console: Core Web Vitals report (field data from real users)
- Google PageSpeed Insights: Both lab and field data
- web.dev/measure

---

## 6. Local Technical SEO

### NAP Consistency Audit

The table below reflects the known address discrepancy for Pasadena and flags all locations for verification. NAP consistency should be confirmed and standardised before submitting any new directory listings.

**Correct Canonical NAP for All Locations (to verify against each source):**

| Studio | Address (Canonical) | Phone | GBP | Website | Houzz | Yelp | LinkedIn |
|---|---|---|---|---|---|---|---|
| Pasadena (HQ) | 234 N El Molino Ave #100, Pasadena, CA 91101 | [Confirm] | Verify | **Fix: shows wrong address** | Verify | Verify | Verify |
| Irvine | [Confirm full address] | [Confirm] | Verify | Verify | Verify | Verify | Verify |
| Claremont | [Confirm full address] | [Confirm] | Verify | Verify | Verify | Verify | Verify |
| Santa Barbara | [Confirm full address] | [Confirm] | Verify | Verify | Verify | Verify | Verify |
| San Diego | [Confirm full address] | [Confirm] | Verify | Verify | Verify | Verify | Verify |

> **Action:** Pull current live listings from each platform and compare to the correct canonical data. Any inconsistency in street address format, suite number notation, phone number format (+1 vs. 10-digit), or business name casing should be corrected to match the canonical exactly.

**Canonical name format to use everywhere:** `EPTDESIGN` (no space, all caps as stylised — confirm this matches legal entity name for formal directories)

---

### Structured Citations Checklist

Build and verify listings in priority order. Higher-authority directories contribute more to local entity confirmation.

| Directory | Priority | Status | Notes |
|---|---|---|---|
| Google Business Profile (×5) | Critical | Exists — fix needed | Update addresses, switch to HTTPS URLs, add descriptions |
| ASLA Member Directory | Critical | Unknown | Enhanced profile with project photos and descriptions |
| AIA Directory | High | Unknown | List as collaborating firm; ensure link to eptdesign.com |
| Houzz | High | Exists — update needed | Wrong address per audit; enhance with project photos |
| Yelp | High | Exists — verify NAP | Confirm address for all locations |
| ENR California | High | Partial | Ensure award listings link back to eptdesign.com |
| USGBC / LEED Project Database | High | Unknown | List Frontier Project (LEED Platinum) with firm credit |
| BBB (Better Business Bureau) | Medium | Unknown | Create or claim listing with correct NAP |
| Clutch.co | Medium | Unknown | Professional services directory; useful for B2B searches |
| Pasadena Chamber of Commerce | Medium | Unknown | Local authority signal for Pasadena geo-relevance |
| Irvine Chamber of Commerce | Medium | Unknown | Local signal for Irvine studio |
| Santa Barbara Chamber | Medium | Unknown | Local signal for Santa Barbara studio |
| LinkedIn Company Page | High | Likely exists | Verify address, add all studio locations |
| Archinect | Medium | Unknown | Architecture community directory |
| ArchDaily Firm Profile | Medium | Unknown | Profile allows project submissions |

---

### GBP Technical Fixes — Step-by-Step

**Step 1: Claim and verify all 5 locations**
Log in at business.google.com. Confirm all 5 studio locations appear under the account. If any are unclaimed, initiate verification via postcard or phone.

**Step 2: Fix website URLs to HTTPS**
For each location: Edit Profile > Website > change `http://` to `https://`. Save.

**Step 3: Correct Pasadena address**
For the Pasadena HQ listing: Edit Profile > Address > update to `234 N El Molino Ave, Suite 100, Pasadena, CA 91101`. Save. Google may require re-verification after address change.

**Step 4: Add business descriptions**
Each GBP location should have a unique description (750 character maximum). Description should include: what the firm does, founding year, the studio city specifically, and a call to action.

Example — Pasadena HQ:
> "EPTDESIGN is a landscape architecture and urban design firm founded in 1962, headquartered in Pasadena, CA. Employee-owned (ESOP) with five studios across Southern California. We design civic spaces, university campuses, healthcare landscapes, and urban parks. Projects include the Narrows Riverwalk in Glendale and campus landscapes for Pomona College and UCLA. Contact our Pasadena studio to discuss your project."

**Step 5: Add service categories**
Primary category: `Landscape Architect`
Secondary categories (where supported): `Urban Design`, `Urban Planner`, `Landscape Designer`

**Step 6: Add project photos to each location**
Upload 5-10 high-quality project photographs per location. Use photos of projects in or near that studio's geography where possible. Photos with geo-metadata intact may provide an additional local signal.

**Step 7: Solicit reviews systematically**
Current total: 5 reviews across 5 locations (approximately 1 per location). This is extremely low for a 64-year firm.

Review-building approach:
- Identify 20 past clients per studio who had positive project experiences (project managers, facilities directors, city project coordinators)
- Alison sends personalised email with a direct GBP review link for the relevant studio
- Link format: `https://search.google.com/local/writereview?placeid=[PLACE_ID]`
- Follow up once after 7 days

**Step 8: Answer Google Q&A**
Check the Q&A section on each GBP listing. Answer any existing questions. Pre-populate with 3-5 common questions and answers (Google allows business owners to post their own Q&A). Use the same FAQ content developed for FAQPage schema.

---

## Implementation Priority Sequence

| Priority | Task | Owner | Estimated Time |
|---|---|---|---|
| 1 | Update robots.txt to allow AI citation bots | Web/IT admin | 30 minutes |
| 2 | Fix Pasadena address on website | Web admin | 1 hour |
| 3 | Update all GBP website URLs to HTTPS | Alison | 30 minutes |
| 4 | Correct GBP addresses and add descriptions | Alison | 2 hours |
| 5 | Allow Ahrefs bot in Cloudflare WAF | Web/IT admin | 30 minutes |
| 6 | Implement Organization + LocalBusiness schema | Developer | 4 hours |
| 7 | Implement Person schema for principals | Developer | 3 hours |
| 8 | Audit and fix H1 tags across site | Developer/SEO | 3 hours |
| 9 | Write custom meta descriptions for priority pages | Alison + SEO | 4 hours |
| 10 | Implement CreativeWork schema on project pages | Developer | 6 hours |
| 11 | Image audit: convert to WebP, add alt text | Developer | 8 hours |
| 12 | Sitemap refresh + resubmit to Search Console | Developer | 1 hour |
| 13 | Internal linking audit and implementation | SEO | 4 hours |
| 14 | Citation building (ASLA, AIA, Houzz, directories) | Alison | Ongoing |
| 15 | GBP review solicitation campaign | Alison | Ongoing |

---

*Document version: February 2026. Review and update after each implementation phase.*
