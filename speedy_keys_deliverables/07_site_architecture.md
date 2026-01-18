# Stage 3: Site Architecture & Content Planning - Speedy Keys

## Recommended Site Architecture

```
Homepage (/)
│
├── Services (/services/)
│   ├── Emergency Car Locksmith (/emergency-car-locksmith/)
│   ├── Car Key Replacement (/car-key-replacement/)
│   ├── Spare Car Keys (/spare-car-keys/)
│   ├── Car Lockout Service (/car-lockout-service/)
│   ├── Key Programming (/car-key-programming/)
│   ├── Transponder Keys (/transponder-key-replacement/)
│   └── Ignition Repair (/car-ignition-repair/)
│
├── 24/7 Emergency (/24-7-emergency-auto-locksmith-essex/) [PRIORITY PAGE]
│
├── Locations (/locations/)
│   ├── Colchester (/auto-locksmith-colchester/)
│   ├── Chelmsford (/auto-locksmith-chelmsford/) [PRIORITY]
│   ├── Southend (/auto-locksmith-southend/) [PRIORITY]
│   ├── Basildon (/auto-locksmith-basildon/) [PRIORITY]
│   ├── Brentwood (/auto-locksmith-brentwood/)
│   ├── Harlow (/auto-locksmith-harlow/)
│   └── Braintree (/auto-locksmith-braintree/)
│
├── Pricing (/auto-locksmith-pricing-essex/) [PRIORITY - Distinctive Asset]
│
├── Car Makes (by demand)
│   ├── BMW Key Replacement (/bmw-key-replacement-essex/)
│   ├── Mercedes Key Replacement (/mercedes-key-replacement-essex/)
│   ├── VW Key Replacement (/vw-key-replacement-essex/)
│   ├── Ford Key Replacement (/ford-key-replacement-essex/)
│   └── [Add top 10-15 makes by volume]
│
├── Guides & Comparison (/guides/) [AI VISIBILITY FOCUS]
│   ├── Locksmith vs Dealership (/locksmith-vs-dealership-car-keys/) [PRIORITY]
│   ├── Car Key Replacement Cost Guide (/car-key-replacement-cost-guide/)
│   ├── How Car Key Programming Works (/how-car-key-programming-works/)
│   └── Spare Key vs Lost Key Costs (/spare-key-vs-lost-key-cost/)
│
├── Blog (/blog/)
│   ├── Emergency Content
│   ├── Preventative Content
│   ├── Troubleshooting Content
│   └── Seasonal Content
│
├── About (/about/)
├── Contact (/contact/)
└── Reviews (/reviews/)
```

---

## URL Structure & Naming Conventions

**URL Principles**:
- Keep URLs short, descriptive, keyword-focused
- Use hyphens (not underscores)
- Include location or service type in URL
- Avoid dates, session IDs, unnecessary parameters

**URL Patterns**:

**Service pages**: `/{service}/`
- Example: `/emergency-car-locksmith/`, `/car-key-replacement/`

**Location pages**: `/auto-locksmith-{town}/`
- Example: `/auto-locksmith-chelmsford/`, `/auto-locksmith-southend/`
- **NOT**: `/locations/chelmsford/` (less keyword-rich)

**Make-specific pages**: `/{make}-key-replacement-essex/`
- Example: `/bmw-key-replacement-essex/`, `/mercedes-key-replacement-essex/`

**Guide/comparison pages**: `/{topic-guide}/` or `/{comparison}/`
- Example: `/locksmith-vs-dealership-car-keys/`, `/car-key-replacement-cost-guide/`

**Blog posts**: `/blog/{keyword-rich-slug}/`
- Example: `/blog/what-to-do-when-locked-out-of-car/`

---

## Internal Linking Strategy

### Hub & Spoke Model

**Hub 1: Emergency Services** (`/24-7-emergency-auto-locksmith-essex/`)
- **Spokes link TO hub**:
  - `/emergency-car-locksmith/` → `/24-7-emergency-auto-locksmith-essex/`
  - `/car-lockout-service/` → `/24-7-emergency-auto-locksmith-essex/`
  - All location pages → `/24-7-emergency-auto-locksmith-essex/`

- **Hub links TO spokes**:
  - `/24-7-emergency-auto-locksmith-essex/` → `/auto-locksmith-chelmsford/` (anchor: "24/7 emergency locksmith in Chelmsford")
  - `/24-7-emergency-auto-locksmith-essex/` → `/car-lockout-service/` (anchor: "locked out of your car")

**Hub 2: Transparent Pricing** (`/auto-locksmith-pricing-essex/`)
- **Spokes link TO hub**:
  - All service pages → `/auto-locksmith-pricing-essex/` (anchor: "view our transparent pricing")
  - All location pages → `/auto-locksmith-pricing-essex/`
  - Comparison page → `/auto-locksmith-pricing-essex/`

- **Hub links TO spokes**:
  - `/auto-locksmith-pricing-essex/` → `/spare-car-keys/` (anchor: "spare car key service")
  - `/auto-locksmith-pricing-essex/` → `/locksmith-vs-dealership-car-keys/` (anchor: "locksmith vs dealership cost comparison")

**Hub 3: Location Coverage** (`/locations/` or homepage if no index page)
- **Spokes link TO hub**:
  - Each town page → Homepage or `/locations/` (with breadcrumb)

- **Hub links TO spokes**:
  - Homepage → All 7 location pages (in coverage section)

**Hub 4: Comparison & Guides** (`/locksmith-vs-dealership-car-keys/` as pillar)
- **Spokes link TO hub**:
  - Service pages → `/locksmith-vs-dealership-car-keys/` (anchor: "locksmith vs dealership")
  - Pricing page → `/locksmith-vs-dealership-car-keys/`

- **Hub links TO spokes**:
  - Comparison page → `/car-key-replacement-cost-guide/`, `/how-car-key-programming-works/`

---

### Internal Linking Rules (MANDATORY for all pages)

1. **Homepage links**: Every page should link back to homepage (breadcrumb or footer)
2. **Service cross-linking**: Each service page links to 3-5 related services
   - Example: `/emergency-car-locksmith/` → `/car-lockout-service/`, `/24-7-emergency-auto-locksmith-essex/`, `/spare-car-keys/`
3. **Location cross-linking**: Each location page links to nearest locations
   - Example: `/auto-locksmith-chelmsford/` → `/auto-locksmith-colchester/`, `/auto-locksmith-braintree/`
4. **Pricing links**: All transactional pages (service, location) link to pricing page
5. **CTA links**: Every page has 2-3 conversion-focused internal links (contact, emergency service, pricing)

---

## Navigation Structure

### Primary Navigation (Main Menu)

**Desktop nav** (7 items max):
1. Home
2. Services [Dropdown]
3. Locations [Dropdown]
4. Pricing
5. 24/7 Emergency
6. About
7. Contact

**Services dropdown**:
- Emergency Car Locksmith
- Car Key Replacement
- Spare Car Keys
- Car Lockout Service
- Key Programming
- [Link to /services/ for full list]

**Locations dropdown**:
- Colchester
- Chelmsford
- Southend
- Basildon
- [Link to /locations/ for full list]

**Mobile nav**:
- Hamburger menu with same structure
- **Sticky CTA bar** (bottom of screen): "Call Now: [PHONE] - 24/7" (click-to-call)

---

### Secondary Navigation

**Footer nav** (4 columns):

**Column 1: Services**
- All 7 core services
- Link to full service list

**Column 2: Locations**
- All 7 town pages
- Link to full location list

**Column 3: Information**
- Pricing
- Locksmith vs Dealership Guide
- About
- Reviews
- Blog

**Column 4: Contact**
- Phone (click-to-call)
- Email
- Service hours: "24/7/365"
- Emergency CTA

---

## Breadcrumb Strategy

**All pages MUST have breadcrumbs** (schema markup + visual):

**Service page breadcrumb**:
```
Home > Services > Emergency Car Locksmith
```

**Location page breadcrumb**:
```
Home > Locations > Chelmsford
```

**Blog post breadcrumb**:
```
Home > Blog > What to Do When Locked Out of Car
```

**Guide page breadcrumb**:
```
Home > Guides > Locksmith vs Dealership Car Keys
```

---

## SXO Considerations (Navigation & Structure)

### Mobile-First Navigation

**Mobile UX requirements**:
- ✅ Hamburger menu loads in <0.5 seconds
- ✅ Tap targets: 48x48px minimum (no tiny links)
- ✅ Sticky bottom CTA: "Call Now: [PHONE]" (always visible, click-to-call)
- ✅ Max 2 levels deep in mobile menu (avoid complex nested dropdowns)

**Mobile content structure**:
- ✅ Most important info above fold (H1, primary CTA, trust signal)
- ✅ Short paragraphs (3-4 sentences max on mobile)
- ✅ Scannable headings every 200-300 words
- ✅ Bullet points > long paragraphs

### Conversion Flow Optimization

**User journey mapping**:

**Emergency user** (high urgency):
- Entry: Google Search "locked out of car Chelmsford 2am" → `/auto-locksmith-chelmsford/`
- Journey: See 24/7 CTA → Click to call → Conversion
- **Navigation priority**: Big, obvious "Call Now" button above fold, no friction

**Research user** (low urgency, comparison):
- Entry: Google Search "locksmith vs dealership" → `/locksmith-vs-dealership-car-keys/`
- Journey: Read comparison → Check pricing → Contact or save for later
- **Navigation priority**: Clear pricing link, "Save for Later" CTA (email/phone opt-in)

**Preventative user** (moderate urgency):
- Entry: Google Search "spare car key cost" → `/spare-car-keys/`
- Journey: Read pricing → Compare vs emergency cost → Book service
- **Navigation priority**: Clear pricing, savings calculator, booking CTA

---

## Content Hierarchy

### Priority Tier 1 (Create Month 1)
1. `/auto-locksmith-pricing-essex/` - Distinctive asset page
2. `/24-7-emergency-auto-locksmith-essex/` - Physical availability page
3. `/auto-locksmith-chelmsford/` - Geographic expansion
4. `/auto-locksmith-southend/` - Geographic expansion
5. `/auto-locksmith-basildon/` - Geographic expansion

### Priority Tier 2 (Create Month 2)
6. `/locksmith-vs-dealership-car-keys/` - AI visibility
7. `/spare-car-keys/` - Preventative entry point
8. `/car-key-replacement-cost-guide/` - AI visibility
9. `/auto-locksmith-brentwood/` - Geographic expansion
10. `/auto-locksmith-harlow/` - Geographic expansion
11. `/auto-locksmith-braintree/` - Geographic expansion
12. `/bmw-key-replacement-essex/` - Make-specific
13. `/mercedes-key-replacement-essex/` - Make-specific

### Priority Tier 3 (Create Month 3)
14. `/car-lockout-service-essex/` - Emergency scenario
15. `/vw-key-replacement-essex/` - Make-specific
16. `/ford-key-replacement-essex/` - Make-specific
17. Blog: "What to Do When Locked Out of Car"
18. Blog: "Why Car Keys Are So Expensive"

---

## Schema Markup Requirements

**ALL pages must have**:
- LocalBusiness schema (with service area, hours, phone)
- Breadcrumb schema

**Service/Location pages must have**:
- FAQPage schema (3-7 Q&A pairs)

**Guide pages should have** (if applicable):
- HowTo schema (for step-by-step guides)
- Article schema (for blog posts)

**Pricing/Comparison pages should have**:
- FAQPage schema
- Table markup (for comparison tables)

---

## Site Speed & Mobile Optimization

**Target**: All pages load in <3 seconds on mobile, <2 seconds on desktop

**Requirements**:
- Images compressed to <150KB each
- WebP format where supported
- Lazy loading for images below fold
- Mobile sticky CTA (bottom bar)
- Responsive tables (stack or horizontal scroll on mobile)
- Click-to-call on ALL phone numbers

---

## Next Stage

**Stage 3.5**: Page-Level Recommendations (MANDATORY) - Create prioritized Page Backlog with 15-25+ specific page recommendations, each mapped to keywords, intent, competitive context, Byron Sharp principles, and AI visibility tactics.
