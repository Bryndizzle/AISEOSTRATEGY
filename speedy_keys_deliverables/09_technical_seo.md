# Stage 7: Technical & On-Page Optimization - Speedy Keys

## Technical SEO Priorities (SXO-Integrated)

### Core Web Vitals Optimization

**Goal**: Meet Google's Core Web Vitals targets for better rankings + user experience

| Metric | Current [ASSUMPTION] | Target | Priority | Fix |
|--------|---------------------|--------|----------|-----|
| **LCP (Largest Contentful Paint)** | 3.5s | <2.5s | **CRITICAL** | Compress images, lazy load below fold, optimize hero image |
| **FID (First Input Delay)** | 150ms | <100ms | **HIGH** | Minimize JavaScript on landing pages, defer non-critical JS |
| **CLS (Cumulative Layout Shift)** | 0.15 | <0.1 | **MEDIUM** | Reserve space for images (width/height attributes), avoid layout shifts |

**Specific fixes**:

1. **Image optimization** (affects LCP):
   - Compress all images to <150KB (use TinyPNG or similar)
   - Convert to WebP format (60-80% smaller than JPG)
   - Lazy load all images below fold
   - Hero image on homepage: Optimize to <50KB, preload
   - **Impact**: 1-2 second faster load time on mobile

2. **JavaScript optimization** (affects FID):
   - Defer non-critical JS (analytics, chat widgets)
   - Minimize JavaScript on service/location pages (emergency pages should load FAST)
   - **Impact**: Faster interaction, better mobile experience

3. **Layout stability** (affects CLS):
   - Add width/height attributes to all images
   - Reserve space for ads/widgets (if any)
   - Avoid inserting content above existing content
   - **Impact**: No layout "jumps" when page loads

**Tools to measure**:
- PageSpeed Insights (Google's official tool)
- GTmetrix
- WebPageTest

**Target**: All pages "Good" (green) on PageSpeed Insights within Month 1

---

### Mobile-First Optimization (SXO Critical)

**Context**: 60-70% of traffic will be mobile [ASSUMPTION: Typical for local emergency services]

**Mobile UX audit**:

1. **Tap targets** (finger-friendly):
   - [ ] All buttons minimum 48x48px
   - [ ] Spacing between links minimum 8px
   - [ ] Phone number CTA: Large, thumb-accessible

2. **Text readability**:
   - [ ] Base font size: 16px minimum (no tiny text)
   - [ ] Line height: 1.5-1.6 (easy reading on small screens)
   - [ ] Contrast: AA standard minimum (4.5:1 for body text)

3. **Content structure**:
   - [ ] Short paragraphs (3-4 sentences max on mobile)
   - [ ] Scannable headings every 200-300 words
   - [ ] Bullet points for lists (easier to scan than paragraphs)

4. **Sticky mobile CTA** (CRITICAL for conversions):
   - [ ] Bottom sticky bar: "Call Now: [PHONE]" (always visible)
   - [ ] Click-to-call: `<a href="tel:[phone]">` on all phone numbers
   - [ ] CTA button color contrasts with page (stands out)
   - [ ] **Impact**: 10-20% increase in mobile conversion rate [ASSUMPTION: Industry benchmark for sticky CTAs]

5. **Table responsiveness**:
   - [ ] Pricing tables: Stack columns on mobile or horizontal scroll
   - [ ] Maximum 3 columns on mobile view
   - [ ] **Impact**: Tables readable on mobile (critical for pricing page)

**Mobile-first checklist**:
- [ ] Test all pages on mobile device (iPhone, Android)
- [ ] Verify click-to-call works on all phone numbers
- [ ] Verify forms work on mobile (if using quote forms)
- [ ] Verify navigation menu opens/closes smoothly
- [ ] No horizontal scrolling (except intentional table scroll)

---

### Schema Markup (Critical for AI Visibility + Rich Snippets)

**Priority 1: LocalBusiness Schema** (ALL pages)

```json
{
  "@context": "https://schema.org",
  "@type": "Locksmith",
  "name": "Speedy Keys",
  "image": "[logo URL]",
  "address": {
    "@type": "PostalAddress",
    "streetAddress": "[PLACEHOLDER: Insert street address]",
    "addressLocality": "Colchester",
    "addressRegion": "Essex",
    "postalCode": "[PLACEHOLDER: Insert postcode]",
    "addressCountry": "GB"
  },
  "telephone": "[PLACEHOLDER: Insert phone number]",
  "priceRange": "££",
  "openingHoursSpecification": {
    "@type": "OpeningHoursSpecification",
    "dayOfWeek": ["Monday", "Tuesday", "Wednesday", "Thursday", "Friday", "Saturday", "Sunday"],
    "opens": "00:00",
    "closes": "23:59"
  },
  "areaServed": [
    "Colchester", "Chelmsford", "Southend-on-Sea", "Basildon", "Brentwood", "Harlow", "Braintree", "Essex"
  ],
  "geo": {
    "@type": "GeoCoordinates",
    "latitude": "[PLACEHOLDER: Insert latitude]",
    "longitude": "[PLACEHOLDER: Insert longitude]"
  },
  "url": "https://www.speedykeys.co.uk",
  "sameAs": [
    "[Facebook URL]",
    "[Google Business Profile URL]",
    "[Checkatrade URL]"
  ],
  "aggregateRating": {
    "@type": "AggregateRating",
    "ratingValue": "4.8",
    "reviewCount": "85"
  }
}
```

**Update monthly**: `reviewCount` (as reviews grow)

---

**Priority 2: FAQPage Schema** (Pricing, Emergency, Comparison, Location pages)

Add to ALL pages with FAQ blocks:

```json
{
  "@context": "https://schema.org",
  "@type": "FAQPage",
  "mainEntity": [
    {
      "@type": "Question",
      "name": "How much does car key replacement cost in Essex?",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "Spare keys cost £99-£150 if you have a working key. Emergency replacement (lost only key) costs £180-£250 depending on your car make and key type."
      }
    },
    {
      "@type": "Question",
      "name": "Do you charge a callout fee?",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "No. We include mobile service in our quoted price. Whether you're in Colchester, Chelmsford, Southend, or anywhere across Essex, there's no additional callout charge."
      }
    }
  ]
}
```

**Pages requiring FAQPage schema**:
- Pricing page (7 FAQs)
- 24/7 emergency page (4 FAQs)
- Locksmith vs dealership page (5 FAQs)
- All location pages (4 FAQs each)
- Spare keys page (3 FAQs)

**Impact**: Rich snippets in Google search (higher CTR), ChatGPT/AI citations

---

**Priority 3: HowTo Schema** (if applicable)

For "How Car Key Programming Works" guide:

```json
{
  "@context": "https://schema.org",
  "@type": "HowTo",
  "name": "How Car Key Programming Works",
  "step": [
    {
      "@type": "HowToStep",
      "text": "Connect OBD diagnostic tool to car's port under dashboard"
    },
    {
      "@type": "HowToStep",
      "text": "Access immobilizer system using manufacturer software"
    },
    {
      "@type": "HowToStep",
      "text": "Program new key's transponder chip to match car's system"
    },
    {
      "@type": "HowToStep",
      "text": "Test key (ignition, remote locking, all functions)"
    }
  ]
}
```

**Impact**: HowTo rich snippets, helpful for AI answer engines

---

### Site Speed Optimization

**Target**: All pages load in <3 seconds on mobile, <2 seconds on desktop

**Optimizations** (in order of impact):

1. **Image compression** (biggest impact):
   - Compress all images to <150KB
   - Use WebP format where supported
   - Lazy load images below fold
   - **Tools**: TinyPNG, Squoosh, Cloudinary

2. **Minimize HTTP requests**:
   - Combine CSS files
   - Combine JavaScript files
   - Use CSS sprites for icons (if multiple small images)

3. **Enable caching**:
   - Set browser cache headers (1 year for static assets)
   - Use CDN for faster global delivery (Cloudflare free tier)

4. **Minify code**:
   - Minify CSS (remove whitespace, comments)
   - Minify JavaScript
   - Minify HTML
   - **Tools**: Most hosting platforms do this automatically, or use build tools

5. **Remove render-blocking resources**:
   - Defer non-critical CSS
   - Async load JavaScript
   - Inline critical CSS (above-fold styles)

**Testing tools**:
- Google PageSpeed Insights (official)
- GTmetrix (detailed breakdown)
- Pingdom (speed test from multiple locations)

---

### Indexability & Crawlability

**robots.txt check**:
```
User-agent: *
Allow: /

Sitemap: https://www.speedykeys.co.uk/sitemap.xml
```

**Sitemap.xml**:
- [ ] All pages included in XML sitemap
- [ ] Submit to Google Search Console
- [ ] Update monthly as new pages added
- [ ] Priority settings:
  - Homepage: 1.0
  - Service pages: 0.9
  - Location pages: 0.8
  - Blog posts: 0.6

**Canonical tags** (prevent duplicate content):
- [ ] Every page has self-referencing canonical tag
- [ ] Location pages don't duplicate (e.g., /colchester/ and /colchester-locksmith/ = choose one URL)

**Internal linking**:
- [ ] Every page has 3-5 internal links (see Stage 3)
- [ ] All links use descriptive anchor text (not "click here")
- [ ] No broken links (audit monthly)

---

## On-Page SEO Checklist (Per Page)

**For EVERY page created, ensure**:

### Title Tag Optimization:
- [ ] 50-60 characters
- [ ] Primary keyword near start
- [ ] Includes location (Essex, Colchester, etc.)
- [ ] Compelling (not just keyword stuffing)
- [ ] Example: "Auto Locksmith Chelmsford | 24/7 Car Key Replacement - Speedy Keys"

### Meta Description:
- [ ] 150-160 characters
- [ ] Answers query + soft CTA
- [ ] Includes primary keyword naturally
- [ ] Includes phone number if emergency service
- [ ] Example: "Lost your car keys in Chelmsford? We're here 24/7 with 30-min response. Same-day service, transparent pricing. Call now: 01206 XXX XXX"

### Header Structure:
- [ ] One H1 (primary keyword near start)
- [ ] 3-7 H2s (at least 2 as questions)
- [ ] H3s/H4s for sub-points
- [ ] Logical hierarchy (H1 → H2 → H3, never skip levels)

### Keyword Optimization:
- [ ] Primary keyword in H1
- [ ] Primary keyword in first 100 words
- [ ] Primary keyword in 1-2 H2s naturally
- [ ] 2-4 semantic variants throughout
- [ ] Keyword density 0.5-1.5% (natural, not stuffed)

### Content Quality:
- [ ] 1,200+ words for service/location pages
- [ ] 1,800+ words for comparison/guide pages
- [ ] Zero filler sentences (every paragraph adds value)
- [ ] Customer language (not corporate jargon)
- [ ] Scannable (short paragraphs, bullet points, subheadings)

### FAQ Block:
- [ ] 3-7 FAQ questions included
- [ ] Questions are actual user queries (check "People Also Ask" in Google)
- [ ] Answers are 40-60 words (concise, direct)
- [ ] FAQPage schema markup added

### Tables:
- [ ] At least one data table if numbers provided (pricing, comparison, response times)
- [ ] Mobile-responsive (stack or horizontal scroll)
- [ ] Clear headers

### Internal Links:
- [ ] 3-5 internal links to related pages
- [ ] Descriptive anchor text (not "click here")
- [ ] Links to higher authority pages (service pages → homepage)
- [ ] Links from lower authority pages (blog → service pages)

### CTAs:
- [ ] Primary CTA above fold (call now, get quote)
- [ ] Secondary CTA mid-content
- [ ] Final CTA at end of content
- [ ] Mobile sticky CTA (bottom bar with phone number)

### Images:
- [ ] At least 1 relevant image (van, technician, key programming)
- [ ] Alt text on ALL images (descriptive, includes keyword where natural)
- [ ] Image file names descriptive (e.g., "auto-locksmith-chelmsford-van.webp" not "IMG_1234.jpg")
- [ ] Compressed to <150KB each

### Schema Markup:
- [ ] LocalBusiness schema on all pages
- [ ] FAQPage schema if FAQ block present
- [ ] HowTo schema if instructional content

---

## Technical SEO Tools & Monitoring

**Essential tools**:
1. **Google Search Console** (FREE - CRITICAL)
   - Monitor indexing status
   - See actual search queries
   - Identify crawl errors
   - Submit sitemaps

2. **Google Analytics 4** (FREE)
   - Track traffic, conversions, user behavior
   - Set up goals (phone clicks, form submissions)

3. **Hike SEO** (PAID - recommended)
   - Page-level SEO audit
   - Keyword tracking
   - AI visibility monitoring
   - Competitor tracking

4. **Screaming Frog** (FREE up to 500 URLs)
   - Crawl site to find broken links
   - Audit title tags/meta descriptions
   - Find duplicate content

5. **Google PageSpeed Insights** (FREE)
   - Core Web Vitals monitoring
   - Mobile/desktop speed scores

**Monthly technical audit checklist**:
- [ ] Check Search Console for crawl errors
- [ ] Update sitemap.xml with new pages
- [ ] Run Screaming Frog crawl to find issues
- [ ] Check Core Web Vitals (all pages "Good"?)
- [ ] Review top 20 pages in GA4 (any performance drops?)
- [ ] Test mobile experience on real device
- [ ] Verify all forms/CTAs working

---

## Priority Technical Tasks (Month 1)

**Week 1-2** (Developer - 10-12 hours):
- [ ] Add LocalBusiness schema to all pages
- [ ] Add FAQPage schema to 5 Month 1 pages (pricing, 24/7 emergency, 3 locations)
- [ ] Implement mobile sticky CTA bar
- [ ] Optimize all images (<150KB, WebP, lazy loading)
- [ ] Set up click-to-call on ALL phone numbers

**Week 3-4** (SEO Specialist - 6-8 hours):
- [ ] Create and submit XML sitemap to Search Console
- [ ] Verify all pages indexed
- [ ] Run initial PageSpeed Insights audit
- [ ] Fix any critical Core Web Vitals issues
- [ ] Set up Google Analytics Goals (phone clicks, form submissions)

---

## Expected Technical SEO Results

**Month 1**:
- All pages load <3 seconds on mobile
- All pages "Good" on Core Web Vitals
- 5 pages with FAQPage schema
- Mobile sticky CTA active
- All phone numbers click-to-call

**Month 3**:
- 18 pages with FAQPage schema
- PageSpeed Insights score: 85+ mobile, 95+ desktop
- Zero indexing errors
- Mobile conversion rate: 8-10%

**Month 6**:
- All pages optimized for mobile (100% mobile-friendly)
- Rich snippets showing for 10+ keywords (FAQ schema)
- Core Web Vitals: 100% pages "Good"
- Mobile conversion rate: 10-12%

---

## Next Stage

**Stage 8**: Implementation Guidance - Who does what, when, with what tools. Roles, responsibilities, week-by-week tasks, and troubleshooting.
