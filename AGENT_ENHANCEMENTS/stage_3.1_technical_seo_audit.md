# Stage 3.1: Technical SEO Audit

**Stage Type**: Analysis & Diagnosis
**Integration Point**: Insert AFTER Stage 3 (Gap Analysis), BEFORE Stage 3.5 (Page Recommendations)
**Purpose**: Identify and prioritize technical SEO issues blocking rankings, indexability, and user experience
**Status**: ✅ Active Enhancement
**Created**: 19 January 2026

---

## Problem This Solves

**Current State**: Agent mentions "technical SEO" in gap analysis but doesn't provide:
- Specific technical issues identified
- Prioritized fix list with difficulty/impact ratings
- Step-by-step remediation instructions
- Core Web Vitals analysis
- Mobile usability audit
- Schema markup recommendations

**Gap**: Clients know "technical issues exist" but don't have an actionable checklist of WHAT to fix and HOW to fix it.

**Solution**: Automatically generate a complete technical SEO audit with prioritized issues, fix instructions, and expected impact.

---

## When to Execute Stage 3.1

**Trigger**: ALWAYS execute after Stage 3 (Gap Analysis) in Strategy Mode

**Input Required**:
- Website URL
- Access to Google Search Console (if available)
- Access to website analytics (if available)
- CMS platform (WordPress, Shopify, custom, etc.)

**Tools Used** (agent instructs user to run if not already available):
- Google PageSpeed Insights
- Google Mobile-Friendly Test
- Google Search Console (coverage reports, Core Web Vitals)
- Screaming Frog (if available) or similar crawler
- Manual inspection of key pages

**Output**: Complete technical SEO audit document with prioritized issues and fix instructions

---

## Technical SEO Audit Components

### 1. Core Web Vitals Analysis

**Purpose**: Identify page speed and user experience issues affecting rankings

**What to Audit**:
- **LCP (Largest Contentful Paint)**: Should be under 2.5 seconds
- **FID (First Input Delay)**: Should be under 100ms
- **CLS (Cumulative Layout Shift)**: Should be under 0.1
- **INP (Interaction to Next Paint)**: Should be under 200ms (replacing FID)

**Output Format**:
```markdown
## Core Web Vitals Audit

### Current Performance

**Desktop Performance**:
- LCP: [X]s (Target: <2.5s) - ❌ FAIL / ✅ PASS
- FID/INP: [X]ms (Target: <100ms / <200ms) - ❌ FAIL / ✅ PASS
- CLS: [X] (Target: <0.1) - ❌ FAIL / ✅ PASS
- Overall Score: [X]/100

**Mobile Performance**:
- LCP: [X]s (Target: <2.5s) - ❌ FAIL / ✅ PASS
- FID/INP: [X]ms (Target: <100ms / <200ms) - ❌ FAIL / ✅ PASS
- CLS: [X] (Target: <0.1) - ❌ FAIL / ✅ PASS
- Overall Score: [X]/100

### Issues Identified

#### Issue 1: Slow LCP ([X]s on mobile)
- **Impact**: HIGH - Directly affects rankings and user experience
- **Cause**: [Large unoptimized hero image (2.4MB), render-blocking JavaScript]
- **Fix Priority**: 🔴 CRITICAL
- **Difficulty**: MEDIUM
- **How to Fix**:
  1. Compress hero image to WebP format (target: <150KB)
  2. Add `loading="eager"` to above-fold images
  3. Preload critical images: `<link rel="preload" as="image" href="hero.webp">`
  4. Implement image CDN (Cloudflare, Cloudinary)
- **Expected Impact**: LCP reduced from [X]s to ~2.0s
- **Time to Fix**: 2-3 hours

#### Issue 2: High CLS ([X] score)
- **Impact**: HIGH - Affects mobile rankings and conversions
- **Cause**: [Images without width/height attributes, late-loading fonts]
- **Fix Priority**: 🔴 CRITICAL
- **Difficulty**: MEDIUM
- **How to Fix**:
  1. Add explicit width/height to all images in HTML
  2. Use `font-display: swap` for web fonts
  3. Reserve space for dynamic content (ads, embeds)
  4. Preload critical fonts: `<link rel="preload" as="font">`
- **Expected Impact**: CLS reduced from [X] to <0.1
- **Time to Fix**: 3-4 hours

#### Issue 3: [Additional Core Web Vitals issue]
[Continue for all identified issues...]

### Quick Wins (Implement First)

1. **[Quick Win 1]**: [Brief description + expected impact]
2. **[Quick Win 2]**: [Brief description + expected impact]
3. **[Quick Win 3]**: [Brief description + expected impact]

### Resources
- PageSpeed Insights report: [URL]
- Google Search Console Core Web Vitals report: [URL]
- Fix guide: [Link to official Google documentation]
```

---

### 2. Indexability & Crawlability Audit

**Purpose**: Ensure search engines can discover, crawl, and index all important pages

**What to Audit**:
- Robots.txt configuration
- XML sitemap status and accuracy
- Noindex/nofollow tags (intentional vs accidental)
- Canonical tags (correct implementation)
- Redirect chains and loops
- Orphan pages (no internal links)
- Crawl errors from Google Search Console

**Output Format**:
```markdown
## Indexability & Crawlability Audit

### Current Index Status

**Pages Submitted vs Indexed** (from Google Search Console):
- Submitted in sitemap: [X] pages
- Indexed: [Y] pages
- Not indexed: [Z] pages
- **Index coverage**: [Y/X]% (Target: >95%)

### Issues Identified

#### Issue 1: [X] Important Pages Not Indexed
- **Affected Pages**: [List specific URLs or page types]
- **Impact**: 🔴 CRITICAL - High-value pages not appearing in search
- **Cause**: [noindex tag, robots.txt block, redirect, soft 404, etc.]
- **Fix Priority**: 🔴 CRITICAL
- **Difficulty**: EASY
- **How to Fix**:
  1. [Step 1: Remove noindex tag from affected pages]
  2. [Step 2: Submit sitemap to GSC]
  3. [Step 3: Request indexing via URL Inspection Tool]
- **Expected Impact**: [X] pages indexed within 1-2 weeks
- **Time to Fix**: 30 mins - 1 hour

#### Issue 2: Robots.txt Blocking Important Pages
- **Affected Pages**: [Specific directories or URLs blocked]
- **Impact**: HIGH - Pages cannot be crawled by search engines
- **Cause**: Overly restrictive robots.txt rules
- **Current robots.txt**:
```
User-agent: *
Disallow: /blog/    ← BLOCKING BLOG CONTENT
Disallow: /services/    ← BLOCKING SERVICE PAGES
```
- **Fix Priority**: 🔴 CRITICAL
- **Difficulty**: EASY
- **How to Fix**:
  1. Remove overly broad Disallow rules
  2. Only block: /admin/, /checkout/, /cart/, /account/
  3. Test new robots.txt with Google Robots Testing Tool
  4. Upload corrected robots.txt
- **Expected Impact**: [X] pages become crawlable immediately
- **Time to Fix**: 15-30 mins

#### Issue 3: XML Sitemap Missing or Outdated
- **Current Status**: [Sitemap exists but outdated / No sitemap found]
- **Impact**: MEDIUM - Search engines may miss new content
- **Fix Priority**: 🟠 HIGH
- **Difficulty**: EASY
- **How to Fix (WordPress)**:
  1. Install Yoast SEO or RankMath plugin
  2. Enable XML sitemap feature
  3. Submit sitemap URL to Google Search Console: [yourdomain.com/sitemap.xml]
  4. Set automatic updates
- **How to Fix (Custom Site)**:
  1. Generate XML sitemap (use online generator or script)
  2. Include all indexable pages (exclude: admin, checkout, duplicates)
  3. Upload to root directory
  4. Submit to GSC
  5. Add sitemap reference to robots.txt:
     ```
     Sitemap: https://yourdomain.com/sitemap.xml
     ```
- **Expected Impact**: Faster discovery of new content
- **Time to Fix**: 30 mins - 1 hour

#### Issue 4: Redirect Chains
- **Affected Pages**: [List pages with redirect chains]
- **Example Chain**: Page A → Page B → Page C → Page D (3 redirects)
- **Impact**: MEDIUM - Slows crawling, wastes link equity
- **Fix Priority**: 🟠 MEDIUM
- **Difficulty**: MEDIUM
- **How to Fix**:
  1. Audit all redirects (use Screaming Frog or Redirect Checker)
  2. Update chains to point directly to final destination
  3. Example: Change Page A → Page D (direct 301)
  4. Update internal links to point to final URLs
- **Expected Impact**: Faster crawling, improved link equity flow
- **Time to Fix**: 2-3 hours (depending on number of chains)

#### Issue 5: Orphan Pages (No Internal Links)
- **Orphan Pages Found**: [X] pages
- **Example URLs**: [List 3-5 example orphan pages]
- **Impact**: MEDIUM - Pages difficult for search engines and users to discover
- **Fix Priority**: 🟠 MEDIUM
- **Difficulty**: EASY
- **How to Fix**:
  1. Identify all orphan pages (pages with 0 internal links)
  2. Add contextual internal links from related pages
  3. Add to relevant navigation/footer if appropriate
  4. Add to sitemap
- **Expected Impact**: Improved crawling, better page discovery
- **Time to Fix**: 1-2 hours

#### Issue 6: Incorrect Canonical Tags
- **Pages with Canonical Issues**: [X] pages
- **Issue Type**: [Self-referencing canonical missing / Canonical pointing to wrong page / Canonical chain]
- **Impact**: HIGH - Can cause indexing confusion
- **Fix Priority**: 🟠 HIGH
- **Difficulty**: MEDIUM
- **How to Fix**:
  1. Audit all canonical tags
  2. Ensure each page has self-referencing canonical: `<link rel="canonical" href="https://yourdomain.com/this-page/">`
  3. Remove canonical tags pointing to other pages (unless intentional duplicate)
  4. Fix canonical chains (A → B → C should be A → C, B → C)
- **Expected Impact**: Clearer indexing signals to Google
- **Time to Fix**: 2-4 hours

### Indexability Summary

| Issue | Impact | Priority | Difficulty | Time to Fix |
|-------|--------|----------|------------|-------------|
| [Issue 1] | CRITICAL | 🔴 | EASY | [X hours] |
| [Issue 2] | HIGH | 🟠 | MEDIUM | [X hours] |
| [Continue...] | | | | |

**Total estimated time**: [X] hours
```

---

### 3. Mobile Usability Audit

**Purpose**: Ensure site works perfectly on mobile devices (60-70% of traffic)

**What to Audit**:
- Mobile-friendly test results
- Viewport configuration
- Touch element sizing
- Text readability
- Horizontal scrolling issues
- Mobile-specific errors from GSC

**Output Format**:
```markdown
## Mobile Usability Audit

### Current Mobile-Friendly Status

**Google Mobile-Friendly Test**: ✅ PASS / ❌ FAIL
- Test URL: [link to test results]

**GSC Mobile Usability Report**:
- Pages with issues: [X] pages
- Issue types: [List issue types from GSC]

### Issues Identified

#### Issue 1: Text Too Small to Read
- **Affected Pages**: [X] pages (primarily blog posts)
- **Impact**: HIGH - Poor user experience, potential mobile ranking penalty
- **Fix Priority**: 🔴 CRITICAL
- **Difficulty**: EASY
- **Current State**: Font size [X]px on mobile
- **How to Fix**:
  1. Set minimum font size to 16px for body text
  2. CSS fix:
     ```css
     body {
       font-size: 16px;
       line-height: 1.5;
     }
     ```
  3. Test on multiple mobile devices
- **Expected Impact**: Improved mobile readability, better engagement
- **Time to Fix**: 30 mins

#### Issue 2: Clickable Elements Too Close Together
- **Affected Pages**: Navigation menu, service links
- **Impact**: HIGH - Users accidentally tap wrong links
- **Fix Priority**: 🔴 CRITICAL
- **Difficulty**: EASY
- **How to Fix**:
  1. Ensure minimum 48x48px tap target size
  2. Add spacing between clickable elements (min 8px)
  3. CSS fix:
     ```css
     a, button {
       min-height: 48px;
       min-width: 48px;
       padding: 12px 16px;
     }
     ```
  4. Test with finger (not mouse) on actual mobile device
- **Expected Impact**: Fewer mis-taps, better mobile UX
- **Time to Fix**: 1-2 hours

#### Issue 3: Viewport Not Configured
- **Impact**: CRITICAL - Site not responsive on mobile
- **Fix Priority**: 🔴 CRITICAL
- **Difficulty**: EASY
- **How to Fix**:
  1. Add viewport meta tag to `<head>`:
     ```html
     <meta name="viewport" content="width=device-width, initial-scale=1.0">
     ```
  2. Test responsiveness on multiple screen sizes
- **Expected Impact**: Site becomes properly responsive
- **Time to Fix**: 5 mins

#### Issue 4: Content Wider Than Screen
- **Affected Pages**: [Pages with horizontal scrolling]
- **Impact**: HIGH - Poor mobile experience
- **Fix Priority**: 🟠 HIGH
- **Difficulty**: MEDIUM
- **Cause**: [Fixed-width elements, large images, tables]
- **How to Fix**:
  1. Remove fixed widths from CSS (use max-width: 100% instead)
  2. Make images responsive:
     ```css
     img {
       max-width: 100%;
       height: auto;
     }
     ```
  3. Make tables scrollable on mobile:
     ```css
     .table-wrapper {
       overflow-x: auto;
       -webkit-overflow-scrolling: touch;
     }
     ```
  4. Test all pages on mobile
- **Expected Impact**: No horizontal scrolling, better mobile UX
- **Time to Fix**: 2-3 hours

### Mobile Usability Summary

| Issue | Pages Affected | Impact | Priority | Time to Fix |
|-------|----------------|--------|----------|-------------|
| Text too small | [X] | HIGH | 🔴 | 30 mins |
| Tap targets too close | [X] | HIGH | 🔴 | 1-2 hours |
| [Continue...] | | | | |

**Total estimated time**: [X] hours
```

---

### 4. Site Speed Optimization

**Purpose**: Improve page load times for better rankings and conversions

**What to Audit**:
- Page load time (desktop and mobile)
- Time to First Byte (TTFB)
- Resource sizes (images, CSS, JavaScript)
- Render-blocking resources
- Server response time
- Caching configuration
- CDN usage

**Output Format**:
```markdown
## Site Speed Optimization Audit

### Current Performance Metrics

**Homepage Load Time**:
- Desktop: [X]s (Target: <3s)
- Mobile: [X]s (Target: <3s)

**Time to First Byte (TTFB)**:
- Current: [X]ms (Target: <200ms)
- Server response time: [X]ms

**Total Page Weight**:
- Homepage: [X]MB (Target: <2MB)
- Average page: [X]MB

### Issues Identified

#### Issue 1: Unoptimized Images ([X]MB total)
- **Impact**: CRITICAL - Slow page loads, poor Core Web Vitals
- **Fix Priority**: 🔴 CRITICAL
- **Difficulty**: MEDIUM
- **Current State**:
  - [X] images over 1MB
  - Formats: JPEG, PNG (not modern formats)
  - No lazy loading
- **How to Fix**:
  1. **Convert to WebP/AVIF**:
     - Use tool: Squoosh, ImageOptim, or Cloudinary
     - Target: <150KB per image
  2. **Implement lazy loading**:
     ```html
     <img src="image.webp" loading="lazy" alt="description">
     ```
  3. **Use responsive images**:
     ```html
     <img src="image-mobile.webp"
          srcset="image-mobile.webp 480w,
                  image-tablet.webp 768w,
                  image-desktop.webp 1200w"
          sizes="(max-width: 480px) 100vw,
                 (max-width: 768px) 50vw,
                 33vw">
     ```
  4. **Add image CDN**: Cloudflare Images, Cloudinary, or ImageKit
- **Expected Impact**: Page weight reduced by [X]%, LCP improved by [X]s
- **Time to Fix**: 4-6 hours (one-time), then automatic with CDN

#### Issue 2: Render-Blocking JavaScript & CSS
- **Impact**: HIGH - Delays page rendering
- **Fix Priority**: 🟠 HIGH
- **Difficulty**: MEDIUM
- **Current State**:
  - [X] render-blocking CSS files
  - [X] render-blocking JS files
  - Total blocking time: [X]ms
- **How to Fix**:
  1. **Inline critical CSS** (above-fold styles):
     ```html
     <style>
       /* Critical above-fold CSS here */
     </style>
     ```
  2. **Defer non-critical CSS**:
     ```html
     <link rel="preload" href="styles.css" as="style" onload="this.onload=null;this.rel='stylesheet'">
     <noscript><link rel="stylesheet" href="styles.css"></noscript>
     ```
  3. **Defer JavaScript**:
     ```html
     <script src="script.js" defer></script>
     ```
  4. **Async for non-critical JS**:
     ```html
     <script src="analytics.js" async></script>
     ```
- **Expected Impact**: Faster initial render, improved FCP and LCP
- **Time to Fix**: 3-4 hours

#### Issue 3: No Browser Caching
- **Impact**: HIGH - Repeat visitors reload all resources
- **Fix Priority**: 🟠 HIGH
- **Difficulty**: EASY
- **How to Fix (Apache - .htaccess)**:
  ```apache
  <IfModule mod_expires.c>
    ExpiresActive On
    ExpiresByType image/jpg "access plus 1 year"
    ExpiresByType image/jpeg "access plus 1 year"
    ExpiresByType image/png "access plus 1 year"
    ExpiresByType image/webp "access plus 1 year"
    ExpiresByType text/css "access plus 1 month"
    ExpiresByType application/javascript "access plus 1 month"
    ExpiresByType application/pdf "access plus 1 month"
  </IfModule>
  ```
- **How to Fix (Nginx)**:
  ```nginx
  location ~* \.(jpg|jpeg|png|webp|css|js)$ {
    expires 1y;
    add_header Cache-Control "public, immutable";
  }
  ```
- **Expected Impact**: Faster page loads for returning visitors
- **Time to Fix**: 30 mins

#### Issue 4: Slow Server Response Time (TTFB >500ms)
- **Impact**: HIGH - Affects all page load metrics
- **Fix Priority**: 🟠 HIGH
- **Difficulty**: MEDIUM-HIGH
- **Current TTFB**: [X]ms (Target: <200ms)
- **How to Fix**:
  1. **Upgrade hosting**: Shared hosting → VPS or managed WordPress hosting
  2. **Enable caching**:
     - WordPress: Install WP Rocket or W3 Total Cache
     - Custom: Implement Redis or Memcached
  3. **Use CDN**: Cloudflare (free) or premium CDN
  4. **Optimize database**: Clean up, add indexes, remove unused data
  5. **Reduce plugins**: Disable unnecessary WordPress plugins
- **Expected Impact**: TTFB reduced to <200ms, faster overall load
- **Time to Fix**: 2-4 hours (or hosting migration: 4-8 hours)

#### Issue 5: No CDN (Content Delivery Network)
- **Impact**: MEDIUM-HIGH - Slower loads for distant users
- **Fix Priority**: 🟠 MEDIUM
- **Difficulty**: EASY
- **How to Fix**:
  1. **Sign up for Cloudflare** (free plan sufficient)
  2. Change DNS nameservers to Cloudflare
  3. Enable "Auto Minify" for HTML, CSS, JS
  4. Enable "Brotli" compression
  5. Set cache rules for static assets
- **Expected Impact**: 30-50% faster load times globally
- **Time to Fix**: 1-2 hours setup

### Site Speed Summary

| Issue | Impact | Priority | Difficulty | Time to Fix | Expected Improvement |
|-------|--------|----------|------------|-------------|----------------------|
| Unoptimized images | CRITICAL | 🔴 | MEDIUM | 4-6 hours | -[X]s load time |
| Render-blocking resources | HIGH | 🟠 | MEDIUM | 3-4 hours | -[X]s FCP |
| No caching | HIGH | 🟠 | EASY | 30 mins | Faster repeat visits |
| Slow TTFB | HIGH | 🟠 | MEDIUM | 2-4 hours | -[X]ms TTFB |
| No CDN | MEDIUM | 🟠 | EASY | 1-2 hours | 30-50% faster global |

**Total estimated time**: 12-18 hours
**Expected overall improvement**: [X]s faster load time
```

---

### 5. Schema Markup Audit

**Purpose**: Implement structured data for rich results and AI visibility

**What to Audit**:
- Existing schema markup
- Missing schema opportunities (FAQPage, HowTo, LocalBusiness, Service, Product)
- Schema validation errors
- Priority schema to implement

**Output Format**:
```markdown
## Schema Markup Audit

### Current Schema Status

**Schema Types Currently Implemented**:
- ✅ Organization schema (Homepage)
- ❌ LocalBusiness schema (Missing)
- ❌ Service schema (Missing)
- ❌ FAQPage schema (Missing)
- ❌ HowTo schema (Missing)

**Schema Validation Errors**: [X] errors found
- [Error 1: Missing required field "address" in Organization]
- [Error 2: Invalid date format in Article schema]

### Schema to Implement (Priority Order)

#### Schema 1: LocalBusiness Schema (Homepage)
- **Priority**: 🔴 CRITICAL (for local businesses)
- **Impact**: HIGH - Essential for Map Pack rankings
- **Difficulty**: EASY
- **Where to Implement**: Homepage
- **Expected Benefit**: Improved local search visibility, Map Pack eligibility
- **How to Implement**:

```json
<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "LocalBusiness",
  "name": "[Business Name]",
  "image": "[Logo URL]",
  "url": "[Website URL]",
  "telephone": "[Phone Number]",
  "address": {
    "@type": "PostalAddress",
    "streetAddress": "[Street Address]",
    "addressLocality": "[City]",
    "addressRegion": "[County]",
    "postalCode": "[Postcode]",
    "addressCountry": "GB"
  },
  "geo": {
    "@type": "GeoCoordinates",
    "latitude": [Latitude],
    "longitude": [Longitude]
  },
  "openingHoursSpecification": [
    {
      "@type": "OpeningHoursSpecification",
      "dayOfWeek": ["Monday", "Tuesday", "Wednesday", "Thursday", "Friday"],
      "opens": "09:00",
      "closes": "17:00"
    }
  ],
  "priceRange": "££",
  "aggregateRating": {
    "@type": "AggregateRating",
    "ratingValue": "[Rating]",
    "reviewCount": "[Review Count]"
  }
}
</script>
```

**Validation**: Test with Google Rich Results Test
**Time to Implement**: 30 mins

---

#### Schema 2: Service Schema (Service Pages)
- **Priority**: 🟠 HIGH
- **Impact**: MEDIUM-HIGH - Helps Google understand services offered
- **Difficulty**: EASY
- **Where to Implement**: All service pages
- **Expected Benefit**: Better service visibility in local search
- **How to Implement**:

```json
<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "Service",
  "serviceType": "[Service Name - e.g., Car Key Replacement]",
  "provider": {
    "@type": "LocalBusiness",
    "name": "[Business Name]"
  },
  "areaServed": {
    "@type": "City",
    "name": "[City/Region]"
  },
  "description": "[Service description]",
  "offers": {
    "@type": "Offer",
    "priceCurrency": "GBP",
    "price": "[Price if fixed, or remove if variable]"
  }
}
</script>
```

**Pages to implement**: [List service pages]
**Time to Implement**: 2-3 hours (template + deploy to all service pages)

---

#### Schema 3: FAQPage Schema (All Pages with FAQs)
- **Priority**: 🔴 CRITICAL (for AI visibility)
- **Impact**: HIGH - Enables FAQ rich results, increases ChatGPT/Perplexity citations
- **Difficulty**: EASY
- **Where to Implement**: All pages with FAQ sections
- **Expected Benefit**: FAQ rich results in SERPs, higher AI citation rate
- **How to Implement**:

```json
<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "FAQPage",
  "mainEntity": [
    {
      "@type": "Question",
      "name": "[Question 1]",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "[Answer 1]"
      }
    },
    {
      "@type": "Question",
      "name": "[Question 2]",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "[Answer 2]"
      }
    }
  ]
}
</script>
```

**Pages to implement**: [List pages with FAQs]
**Time to Implement**: 3-4 hours (template + deploy to all pages with FAQs)

---

#### Schema 4: HowTo Schema (Guide/Instructional Pages)
- **Priority**: 🟠 MEDIUM
- **Impact**: MEDIUM - Enables HowTo rich results
- **Difficulty**: EASY
- **Where to Implement**: Pages with step-by-step instructions
- **Expected Benefit**: HowTo rich results, better AI visibility for process queries
- **How to Implement**:

```json
<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "HowTo",
  "name": "[Title - e.g., How to Get a Spare Car Key]",
  "description": "[Brief description]",
  "step": [
    {
      "@type": "HowToStep",
      "name": "[Step 1 name]",
      "text": "[Step 1 description]"
    },
    {
      "@type": "HowToStep",
      "name": "[Step 2 name]",
      "text": "[Step 2 description]"
    }
  ]
}
</script>
```

**Pages to implement**: [List guide pages]
**Time to Implement**: 2-3 hours

---

#### Schema 5: Article Schema (Blog Posts)
- **Priority**: 🟠 MEDIUM
- **Impact**: MEDIUM - Helps Google understand blog content
- **Difficulty**: EASY
- **Where to Implement**: All blog posts
- **Expected Benefit**: Better blog post visibility, potential featured snippets
- **How to Implement** (WordPress):
  - Use Yoast SEO or RankMath (auto-generates Article schema)
  - Verify implementation with Rich Results Test

**Time to Implement**: 1 hour (plugin configuration)

---

### Schema Implementation Priority

| Schema Type | Priority | Pages Affected | Impact | Time to Implement |
|-------------|----------|----------------|--------|-------------------|
| LocalBusiness | 🔴 CRITICAL | Homepage | HIGH | 30 mins |
| FAQPage | 🔴 CRITICAL | [X] pages | HIGH | 3-4 hours |
| Service | 🟠 HIGH | [X] service pages | MEDIUM | 2-3 hours |
| HowTo | 🟠 MEDIUM | [X] guide pages | MEDIUM | 2-3 hours |
| Article | 🟠 MEDIUM | All blog posts | MEDIUM | 1 hour |

**Total estimated time**: 9-13 hours
**Expected benefit**: Rich results eligibility, improved AI citations
```

---

### 6. Internal Linking Structure Audit

**Purpose**: Optimize internal linking for crawling, link equity flow, and user navigation

**What to Audit**:
- Orphan pages (pages with no internal links)
- Pages with excessive internal links (>100)
- Broken internal links
- Poor anchor text usage
- Pillar/hub structure (if applicable)

**Output Format**:
```markdown
## Internal Linking Structure Audit

### Current Internal Linking Status

**Site Structure**:
- Total pages: [X]
- Pages with 0 internal links (orphans): [X]
- Pages with 1-5 internal links: [X]
- Pages with 6-10 internal links: [X]
- Pages with 10+ internal links: [X]

**Issues Identified**:
- [X] broken internal links found
- [X] orphan pages with 0 internal links
- [X] pages with generic anchor text ("click here", "read more")

### Issues Identified

#### Issue 1: [X] Orphan Pages
- **Affected Pages**: [List orphan pages]
- **Impact**: MEDIUM - Pages difficult to discover
- **Fix Priority**: 🟠 MEDIUM
- **Difficulty**: EASY
- **How to Fix**:
  1. Identify all orphan pages (Screaming Frog → Internal → Orphan Pages)
  2. Add contextual links from related pages
  3. Example: Link to /spare-car-keys/ from:
     - /car-key-replacement/ (related service)
     - /emergency-locksmith/ (related service)
     - Blog post about "lost car keys" (contextual)
  4. Ensure each page has at least 3-5 internal links pointing to it
- **Expected Impact**: Better page discovery, improved crawling
- **Time to Fix**: 2-3 hours

#### Issue 2: [X] Broken Internal Links
- **Examples**:
  - /old-page-url/ (404) linked from 5 pages
  - /services/car-keys/ (redirects) linked from 8 pages
- **Impact**: MEDIUM - Poor UX, wasted crawl budget
- **Fix Priority**: 🟠 MEDIUM
- **Difficulty**: EASY
- **How to Fix**:
  1. Find all broken links (Screaming Frog → Response Codes → Client Error 4xx)
  2. Update links to correct destinations
  3. Fix redirected links (point directly to final URL)
- **Expected Impact**: Improved UX, better crawl efficiency
- **Time to Fix**: 1-2 hours

#### Issue 3: Generic Anchor Text Usage
- **Current State**: 40% of internal links use "click here", "read more", "learn more"
- **Impact**: LOW-MEDIUM - Missed opportunity for keyword context
- **Fix Priority**: 🟡 LOW
- **Difficulty**: MEDIUM
- **How to Fix**:
  1. Audit all internal anchor text
  2. Replace generic text with descriptive, keyword-rich anchors:
     - ❌ "Click here to learn about our services"
     - ✅ "Emergency car locksmith services in Essex"
  3. Use natural language (not over-optimized)
- **Expected Impact**: Better internal link equity flow, clearer page topics
- **Time to Fix**: 3-4 hours

#### Issue 4: No Clear Site Hierarchy (Pillar/Hub Structure)
- **Current State**: Flat structure, no clear pillar pages
- **Impact**: MEDIUM - Missed opportunity for topic authority
- **Fix Priority**: 🟡 LOW (long-term strategy)
- **Difficulty**: HIGH
- **How to Fix**:
  1. Identify pillar topics (e.g., "Car Key Services", "Emergency Locksmith", "Location Guides")
  2. Create pillar pages (comprehensive guides)
  3. Link all related content to pillar pages
  4. Example structure:
     - **Pillar**: /car-key-services/ (comprehensive guide)
     - **Hub**: /spare-car-keys/, /car-key-replacement/, /transponder-keys/ (specific services)
     - **Spoke**: Blog posts about specific makes/models, how-tos
  5. Implement bidirectional linking (spokes → hub → pillar)
- **Expected Impact**: Improved topic authority, better rankings for pillar topics
- **Time to Fix**: 8-12 hours (content creation + internal linking)

### Internal Linking Recommendations

**Quick Wins** (Implement First):
1. Fix all broken internal links ([X] hours)
2. Add internal links to orphan pages ([X] hours)
3. Update top 10 priority pages with 3-5 contextual internal links ([X] hours)

**Long-Term Strategy**:
1. Implement pillar/hub/spoke structure
2. Update all generic anchor text
3. Build internal linking into content creation workflow

**Total estimated time**: 6-10 hours (quick wins), 8-12 hours (long-term)
```

---

### 7. HTTPS & Security Audit

**Purpose**: Ensure site is secure and trusted by browsers/users

**What to Audit**:
- HTTPS implementation
- Mixed content warnings
- SSL certificate validity
- Security headers
- Malware/blacklist status

**Output Format**:
```markdown
## HTTPS & Security Audit

### Current Security Status

**HTTPS Status**: ✅ Fully HTTPS / ⚠️ Partially HTTPS / ❌ No HTTPS
**SSL Certificate**: ✅ Valid / ❌ Expired / ⚠️ Self-signed
**Certificate Expiry**: [Date]

**Security Issues Found**: [X] issues

### Issues Identified

#### Issue 1: Mixed Content Warnings
- **Affected Pages**: [X] pages loading HTTP resources
- **Impact**: HIGH - Browser warnings, user trust issues
- **Fix Priority**: 🔴 CRITICAL
- **Difficulty**: MEDIUM
- **Current State**: HTTPS pages loading HTTP images/scripts
- **How to Fix**:
  1. Find all HTTP resources: Browser DevTools → Console → Check for mixed content warnings
  2. Update all HTTP URLs to HTTPS:
     - Images: `<img src="https://...">`
     - Scripts: `<script src="https://...">`
     - Stylesheets: `<link href="https://...">`
  3. Use protocol-relative URLs if source supports both:
     - `<img src="//example.com/image.jpg">`
  4. Verify no mixed content warnings remain
- **Expected Impact**: No browser warnings, improved user trust
- **Time to Fix**: 2-3 hours

#### Issue 2: No HTTP to HTTPS Redirect
- **Current State**: HTTP version accessible, not redirecting to HTTPS
- **Impact**: HIGH - Duplicate content, insecure version accessible
- **Fix Priority**: 🔴 CRITICAL
- **Difficulty**: EASY
- **How to Fix (Apache - .htaccess)**:
  ```apache
  RewriteEngine On
  RewriteCond %{HTTPS} off
  RewriteRule ^(.*)$ https://%{HTTP_HOST}%{REQUEST_URI} [L,R=301]
  ```
- **How to Fix (Nginx)**:
  ```nginx
  server {
    listen 80;
    server_name yourdomain.com www.yourdomain.com;
    return 301 https://yourdomain.com$request_uri;
  }
  ```
- **Expected Impact**: All traffic uses HTTPS, no duplicate content
- **Time to Fix**: 15 mins

#### Issue 3: Missing Security Headers
- **Impact**: MEDIUM - Vulnerability to certain attacks, lower security score
- **Fix Priority**: 🟡 LOW
- **Difficulty**: EASY
- **How to Fix (Add to .htaccess or server config)**:
  ```apache
  # Prevent clickjacking
  Header always set X-Frame-Options "SAMEORIGIN"

  # Prevent MIME type sniffing
  Header always set X-Content-Type-Options "nosniff"

  # Enable XSS protection
  Header always set X-XSS-Protection "1; mode=block"

  # Referrer policy
  Header always set Referrer-Policy "strict-origin-when-cross-origin"
  ```
- **Expected Impact**: Improved security score, protection against common attacks
- **Time to Fix**: 30 mins

### Security Summary

| Issue | Impact | Priority | Time to Fix |
|-------|--------|----------|-------------|
| Mixed content | HIGH | 🔴 | 2-3 hours |
| No HTTPS redirect | HIGH | 🔴 | 15 mins |
| Missing security headers | MEDIUM | 🟡 | 30 mins |

**Total estimated time**: 3-4 hours
```

---

### 8. URL Structure Audit

**Purpose**: Ensure clean, SEO-friendly URL structure

**What to Audit**:
- URL length and readability
- Special characters in URLs
- Duplicate URLs (with/without trailing slash, www vs non-www)
- Parameter-heavy URLs
- URL consistency

**Output Format**:
```markdown
## URL Structure Audit

### Current URL Structure

**URL Format**: [Good/Needs Improvement]
**Issues Found**: [X] issues

### Issues Identified

#### Issue 1: Inconsistent Trailing Slashes
- **Example**: `/services` vs `/services/` both accessible
- **Impact**: MEDIUM - Potential duplicate content
- **Fix Priority**: 🟠 MEDIUM
- **Difficulty**: EASY
- **How to Fix**:
  1. Choose one format (with or without trailing slash)
  2. Redirect all URLs to canonical format:
     ```apache
     # Force trailing slash
     RewriteCond %{REQUEST_FILENAME} !-f
     RewriteCond %{REQUEST_URI} !(.*)/$
     RewriteRule ^(.*)$ https://%{HTTP_HOST}/$1/ [L,R=301]
     ```
  3. Update internal links to use chosen format
  4. Update canonical tags to match
- **Expected Impact**: Consistent URLs, no duplicate content signals
- **Time to Fix**: 1-2 hours

#### Issue 2: Long, Keyword-Stuffed URLs
- **Examples**:
  - `/best-car-locksmith-services-in-essex-colchester-emergency-24-7/` (too long)
  - `/category/services/emergency/car/locksmith/essex/` (too deep)
- **Impact**: LOW-MEDIUM - Poor user experience, may look spammy
- **Fix Priority**: 🟡 LOW (for new pages), 🟠 MEDIUM (if widespread)
- **Difficulty**: MEDIUM (requires 301 redirects)
- **How to Fix**:
  1. Keep URLs concise: `/emergency-car-locksmith-essex/`
  2. Max 3-5 words in URL slug
  3. For existing pages: Set up 301 redirects from old to new URLs
  4. Update internal links
- **Expected Impact**: Cleaner URLs, better CTR, improved UX
- **Time to Fix**: 3-4 hours (if changing existing URLs)

#### Issue 3: Parameter-Heavy URLs
- **Examples**: `/services?id=123&category=locksmith&location=essex`
- **Impact**: MEDIUM - Harder to rank, poor UX, crawl inefficiency
- **Fix Priority**: 🟠 MEDIUM
- **Difficulty**: HIGH (requires URL rewriting)
- **How to Fix**:
  1. Implement URL rewriting to convert parameters to clean URLs:
     - Before: `/services?id=123`
     - After: `/services/car-locksmith-essex/`
  2. Set up 301 redirects from parameter URLs to clean URLs
  3. Update sitemap with clean URLs only
- **Expected Impact**: Better rankings, improved UX, cleaner site structure
- **Time to Fix**: 4-6 hours (developer required)

### URL Structure Recommendations

**Best Practices**:
- ✅ Short, descriptive URLs: `/spare-car-keys/`
- ✅ Include primary keyword: `/emergency-locksmith-essex/`
- ✅ Use hyphens, not underscores: `car-keys` not `car_keys`
- ✅ Lowercase only: `/Services/` → `/services/`
- ✅ Shallow hierarchy: `/service-name/` better than `/category/subcategory/service/`

**Total estimated time**: 4-8 hours (if changing existing URLs)
```

---

## Technical SEO Audit Summary & Prioritization

**Purpose**: Master checklist showing all issues prioritized by impact and effort

**Output Format**:
```markdown
## Technical SEO Audit: Master Priority List

### 🔴 CRITICAL Priority (Fix First - Week 1)

| Issue | Category | Impact | Difficulty | Time | Expected Outcome |
|-------|----------|--------|------------|------|------------------|
| Pages not indexed | Indexability | CRITICAL | EASY | 1 hour | [X] high-value pages indexed |
| Robots.txt blocking pages | Indexability | CRITICAL | EASY | 30 mins | [X] pages become crawlable |
| Mixed content warnings | Security | HIGH | MEDIUM | 2-3 hours | No browser warnings |
| Slow LCP (>4s mobile) | Core Web Vitals | CRITICAL | MEDIUM | 4-6 hours | LCP <2.5s |
| Text too small on mobile | Mobile Usability | HIGH | EASY | 30 mins | Better mobile UX |
| LocalBusiness schema missing | Schema | CRITICAL | EASY | 30 mins | Map Pack eligibility |

**Week 1 Total Time**: 9-13 hours
**Week 1 Expected Impact**: Major improvements in indexing, mobile UX, local visibility

---

### 🟠 HIGH Priority (Fix Second - Week 2-3)

| Issue | Category | Impact | Difficulty | Time | Expected Outcome |
|-------|----------|--------|------------|------|------------------|
| High CLS score | Core Web Vitals | HIGH | MEDIUM | 3-4 hours | CLS <0.1 |
| No HTTPS redirect | Security | HIGH | EASY | 15 mins | All traffic on HTTPS |
| Render-blocking resources | Site Speed | HIGH | MEDIUM | 3-4 hours | Faster page render |
| No browser caching | Site Speed | HIGH | EASY | 30 mins | Faster repeat visits |
| FAQPage schema missing | Schema | HIGH | EASY | 3-4 hours | FAQ rich results |
| Service schema missing | Schema | HIGH | EASY | 2-3 hours | Better service visibility |
| Orphan pages | Internal Linking | MEDIUM | EASY | 2-3 hours | Better page discovery |
| Broken internal links | Internal Linking | MEDIUM | EASY | 1-2 hours | Improved UX |

**Week 2-3 Total Time**: 15-22 hours
**Week 2-3 Expected Impact**: Significant speed improvements, rich results eligibility

---

### 🟡 MEDIUM Priority (Fix Third - Week 4-6)

| Issue | Category | Impact | Difficulty | Time | Expected Outcome |
|-------|----------|--------|------------|------|------------------|
| Slow TTFB | Site Speed | MEDIUM | MEDIUM | 2-4 hours | Faster initial load |
| No CDN | Site Speed | MEDIUM | EASY | 1-2 hours | 30-50% faster global |
| Redirect chains | Indexability | MEDIUM | MEDIUM | 2-3 hours | Better crawl efficiency |
| Incorrect canonicals | Indexability | MEDIUM | MEDIUM | 2-4 hours | Clearer indexing signals |
| HowTo schema missing | Schema | MEDIUM | EASY | 2-3 hours | HowTo rich results |
| Generic anchor text | Internal Linking | MEDIUM | MEDIUM | 3-4 hours | Better link context |
| Inconsistent trailing slashes | URL Structure | MEDIUM | EASY | 1-2 hours | No duplicate signals |

**Week 4-6 Total Time**: 13-22 hours
**Week 4-6 Expected Impact**: Further speed/crawling improvements, additional rich results

---

### 🔵 LONG-TERM (Month 2-3)

| Issue | Category | Impact | Difficulty | Time | Expected Outcome |
|-------|----------|--------|------------|------|------------------|
| No pillar/hub structure | Internal Linking | MEDIUM | HIGH | 8-12 hours | Topic authority |
| Long keyword-stuffed URLs | URL Structure | LOW | MEDIUM | 3-4 hours | Cleaner URLs |
| Missing security headers | Security | LOW | EASY | 30 mins | Better security score |

**Month 2-3 Total Time**: 12-17 hours
**Month 2-3 Expected Impact**: Long-term SEO improvements, better site structure

---

## Total Technical SEO Effort

**Critical + High Priority (Weeks 1-3)**: 24-35 hours
**Medium Priority (Weeks 4-6)**: 13-22 hours
**Long-Term (Month 2-3)**: 12-17 hours

**Grand Total**: 49-74 hours over 3 months

**Expected Overall Impact**:
- [X]+ pages indexed
- LCP improved from [X]s to <2.5s
- Mobile usability score: PASS
- [X] rich result types eligible
- [X]% faster page load times
- Clear site structure and hierarchy
```

---

## Integration with Workflow Stages

### **Stage 3: Gap Analysis**
- Stage 3.1 comes AFTER Stage 3, providing detailed technical diagnostics

### **Stage 3.5: Page-Level Recommendations**
- Technical issues inform which pages to prioritize (don't create new pages if existing ones can't be indexed)

### **Stage 7: Implementation Tasks**
- Technical fixes are integrated into 30/60/90 roadmap with priorities

### **Stage 9: Measurement Framework**
- Technical metrics (Core Web Vitals, index coverage) added to tracking

---

## Quality Gates

Before completing Stage 3.1, verify:

- [ ] **Core Web Vitals analyzed** with specific fix instructions for each failing metric
- [ ] **Indexability issues identified** with crawlability and sitemap problems diagnosed
- [ ] **Mobile usability audited** with all GSC mobile issues addressed
- [ ] **Site speed analyzed** with top 5 performance bottlenecks identified
- [ ] **Schema opportunities listed** with priority order and implementation code
- [ ] **Internal linking structure reviewed** with orphan pages and broken links identified
- [ ] **Security audit completed** with HTTPS and security header recommendations
- [ ] **Master priority list created** showing all issues ranked by impact/effort
- [ ] **Time estimates provided** for each fix (realistic developer/implementation time)
- [ ] **Expected outcomes specified** for each fix (what will improve and by how much)

---

## Example Output

See: `/speedy_keys_fresh_strategy/STAGE_3.1_TECHNICAL_SEO_AUDIT.md` (to be created in future strategy runs)

**This enhancement automatically generates**:
- Complete technical SEO audit across 8 categories
- Specific fix instructions (copy-paste ready code where applicable)
- Prioritized master checklist (Critical → High → Medium → Long-term)
- Time estimates for each fix
- Expected impact for each fix
- Integration with 30/60/90 roadmap

---

**END OF ENHANCEMENT: STAGE 3.1 TECHNICAL SEO AUDIT**
