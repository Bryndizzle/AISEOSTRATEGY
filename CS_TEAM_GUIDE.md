# How to Use the AI SEO Strategy Agent - CS Team Guide

**Purpose**: This guide shows you how to use browser agent prompts to extract client information and create comprehensive SEO strategies.

**Time Required**: 10-15 minutes to extract info using browser agents, agent creates strategy in minutes

**No SEO expertise required** - just use the browser agent prompts below.

---

## 📋 STEP 1: Extract Client Information Using Browser Agents

You'll use browser agent prompts to automatically extract information from the client's website and online presence.

### **Part A: Business Basics** (3 minutes)

**Browser Agent Prompt:**

```
Go to [client website URL] and extract the following information:
1. Business name (from homepage/header/about page)
2. Industry and what they do (from homepage/about section)
3. Service area/location (from contact page/footer/service pages)
4. Top 3-5 main services or products (from services menu/homepage)
5. Confirm the website URL

Format the response as:
- Business Name: [name]
- Industry: [industry]
- Location: [service area]
- Services: [list 3-5 services]
- Website: [URL]
```

**What to do:**
1. Paste the browser agent prompt with the client's website URL
2. Copy the extracted information into your briefing document

---

### **Part B: Brand Tone of Voice** (3 minutes)

**Step 1: Get Auto-Generated TOV from Hike**

Hike platform auto-generates TOV.

**What to do:**
1. Check Hike platform for the client's auto-generated TOV
2. **Sense check it** - does it feel accurate based on what you know?

**Step 2: Verify with Social Channels (Browser Agent)**

Run this browser agent prompt to check their social media tone:

```
Analyze the tone of voice across [client's] social channels and compare to website:

Check:
- Facebook posts (if available)
- Instagram captions (if available)
- LinkedIn posts (if B2B)
- Twitter/X posts (if available)

Look for:
1. How do they speak to customers? (Casual/professional/friendly?)
2. Language style (emojis, slang, technical terms, straight-talking?)
3. Personality traits (warm, direct, humorous, serious?)
4. Any phrases they use repeatedly

Compare social tone to website tone and note:
- Is it consistent across channels?
- Which channel best represents their "true" voice?
- Any notable differences?

Format as:
- Social Media TOV: [description]
- Most authentic channel: [platform name]
- Example posts/phrases: [2-3 examples]
- Consistent with website? [Yes/No + brief note]
```

**What to do:**
1. Paste the browser agent prompt
2. Compare social TOV to Hike's auto-generated TOV
3. **If different**: Note which feels more authentic
4. **Use the most accurate TOV** for briefing document

**Note**: If no social presence or inconsistent tone, use Hike's auto-generated TOV or default: "Professional, clear, helpful - avoids corporate jargon"

---

### **Part C: Business Goal** (2 minutes)

**Browser Agent Prompt:**

```
Go to [client website URL] and analyze their business model to infer their primary SEO goal:

Look for signals:
- Strong CTAs, contact forms, quote requests = CONVERSIONS (get leads/sales)
- Blog-heavy, resource content, guides = AWARENESS (get traffic)
- Case studies, credentials, awards, thought leadership = AUTHORITY (build reputation)

Check:
- Homepage CTAs (what's the main action?)
- Navigation structure (services vs blog vs resources)
- Content types (service pages vs educational content)

Recommend ONE primary goal:
- Conversions (if transactional, service-based, local business)
- Awareness (if informational, content-heavy, broad audience)
- Authority (if expertise-based, high-value services, B2B)

Format as:
- Primary Goal: [Conversions/Awareness/Authority]
- Reasoning: [1-2 sentences explaining why]
```

**What to do:**
1. Paste the browser agent prompt with the client's website URL
2. Review the recommended goal
3. **If uncertain**, default to **Conversions** (most common for local/service businesses)
4. Copy into your briefing document

---

### **Part D: Keyword Data** (5 minutes) ⚠️ **CRITICAL**

**This is the most important part.** You need keyword data.

#### **Option 1: Use Hike Platform** (BEST - Most Common)

**What to do:**
1. Check if client is connected to Hike
2. Use browser agent to access Hike and export keyword reports:

**Browser Agent Prompt:**

```
Access Hike platform for [client name/website]:
1. Navigate to keyword data/rankings section
2. Export keyword report (CSV or Excel format)
3. Include: keywords, search volume, current position, difficulty

If available in Hike:
- GSC data (Hike connects to GSC in most cases)
- Ahrefs data (if integrated)

Format as CSV export or list top 50 keywords with:
- Keyword
- Search volume
- Current position
- Search intent
```

**What to do:**
1. Use browser agent to export Hike keyword report
2. **Done!** Attach to briefing

**Note**: GSC is connected to Hike in most cases - you don't need separate GSC access.

---

#### **Option 2: Client Has Standalone Ahrefs/SEMrush Access** (GOOD)

**What to do:**
1. Use browser agent to access Ahrefs/SEMrush and export keyword data
2. Or ask client to export their keyword data as CSV/Excel
3. Attach to briefing

---

#### **Option 3: GSC Not Connected to Hike** (If Needed)

**Only if GSC is NOT connected to Hike:**

**Browser Agent Prompt:**

```
Go to Google Search Console for [website URL]:
1. Navigate to Performance → Search Results
2. Set date range to "Last 12 months"
3. Export the data as CSV
4. List the top 50 queries by impressions

Format as:
[Provide CSV data or list of queries with impressions, clicks, position]
```

**What to do:**
1. Client provides GSC access OR exports data themselves
2. Attach CSV file to briefing OR copy query list

---

#### **Option 4: Automated Keyword Research** (FALLBACK - if no tools available)

**Browser Agent Prompt:**

```
Research keyword opportunities for [client website URL]:

1. Analyze their current service pages and extract target keywords
2. For their industry [industry] in [location], suggest 20-30 relevant keywords including:
   - Service + location keywords (e.g., "plumber Essex")
   - Service + problem keywords (e.g., "emergency plumber")
   - Service + comparison keywords (e.g., "plumber vs heating engineer")
   - Question keywords (e.g., "how much does plumber cost")

3. Check their existing page titles and H1s for target keywords

Format as a list of 20-30 keywords categorized by:
- High commercial intent (service-based)
- Medium intent (comparison/consideration)
- Informational intent (questions/guides)
```

**What to do:**
1. Paste the browser agent prompt
2. Review the suggested keywords
3. Copy the list into your briefing document

**Note**: This option is less accurate than real keyword data (Hike/Ahrefs/GSC), but works if client has no tools connected.

---

### **Part E: Current Performance** (3 minutes - OPTIONAL but helpful)

#### **Option 1: Use Hike Platform** (BEST - Most Common)

**Browser Agent Prompt:**

```
Access Hike platform for [client name/website] and extract current performance:

1. Last 3 months performance (from GSC connected to Hike):
   - Total clicks
   - Total impressions
   - Average CTR
   - Average position

2. Top 10 keywords they currently rank for (by impressions)

3. Top 5 performing pages (by clicks)

4. If Ahrefs is integrated in Hike, also get:
   - Domain Rating (DR)
   - Number of backlinks
   - Organic traffic estimate

Format as:
- Monthly clicks: [X]
- Monthly impressions: [X]
- Average CTR: [X%]
- Average position: [X]
- Top ranking keywords: [list with positions]
- Top pages: [list with URLs]
- Domain Rating: [X] (if available)
```

**What to do:**
1. Use browser agent to extract Hike performance report
2. Copy extracted data into briefing

**Note**: In most cases, GSC is connected to Hike, so you don't need separate GSC access.

---

#### **Option 2: GSC Not Connected to Hike** (If Needed)

**Only if GSC is NOT connected to Hike:**

**Browser Agent Prompt:**

```
Access Google Search Console for [website URL] and extract:

1. Last 3 months performance:
   - Total clicks
   - Total impressions
   - Average CTR
   - Average position

2. Top 10 keywords they currently rank for (by impressions)

3. Top 5 performing pages (by clicks)

Format as:
- Monthly clicks: [X]
- Monthly impressions: [X]
- Average CTR: [X%]
- Average position: [X]
- Top ranking keywords: [list with positions]
- Top pages: [list with URLs]
```

---

#### **Option 3: Use Standalone Ahrefs/SEMrush**

**Browser Agent Prompt:**

```
Go to Ahrefs Site Explorer or SEMrush and analyze [website URL]:
- Organic search traffic estimate
- Number of ranking keywords
- Domain rating/authority score
- Top 10 organic keywords

Format as:
- Estimated monthly traffic: [X]
- Ranking keywords: [X]
- Domain authority: [X]
- Top keywords: [list]
```

**What to do:**
1. Use whichever data source is available (Hike preferred)
2. **If no data available**: Skip this section (agent will work without it)
3. Copy extracted data into briefing

---

### **Part F: Competitors** (3 minutes - OPTIONAL but helpful)

**Browser Agent Prompt:**

```
Find the top 3 SEO competitors for [client website URL]:

Method 1: Google Search Analysis
Search for their main service keywords (e.g., "[service] [location]") and identify the top 3 ranking competitors (exclude directories like Yell, Google Maps).

Method 2: Ahrefs/SEMrush
Use Ahrefs "Competing Domains" or SEMrush "Competitors" feature for [website URL] and list top 3 organic competitors.

For each competitor provide:
- Company name
- Website URL
- Why they're a strong competitor (e.g., "Ranks #1 for 'plumber Essex'")

Format as:
1. [Competitor name] - [URL] - [reason]
2. [Competitor name] - [URL] - [reason]
3. [Competitor name] - [URL] - [reason]
```

**What to do:**
1. Paste the browser agent prompt
2. Review the identified competitors
3. Copy competitor URLs into briefing document

**If browser agent can't find competitors**: Skip this section (agent will identify competitors during analysis).

---

### **Part G: Customer Insights** (10 minutes - OPTIONAL but makes content 10x better) ⭐ **HIGHLY VALUABLE**

**⚠️ This is one of the most valuable parts. Spend time on this.**

**Browser Agent Prompt:**

```
Analyze [client website URL], [industry], and [location] to extract deep customer insights:

1. Common Customer Questions:
   - Check FAQ page on client website (if exists)
   - Check blog posts for question-based content
   - Search "[business name] + reviews" and analyze Google Reviews, Trustpilot, etc.
   - Look for "People Also Ask" on Google for their main service keywords
   - **Search Reddit**: "[industry] [location] reddit" and "[service] recommendations reddit"

Extract 5-10 common questions customers ask.

2. Common Objections:
   - Analyze reviews for negative feedback or concerns
   - Look for content addressing objections (e.g., "Why choose us", "Our guarantee")
   - Check competitor reviews to find industry-wide objections
   - **Search Reddit threads**: Look for complaints, concerns, hesitations about [industry]
   - Common objections: price concerns, trust issues, quality worries, timing/availability, "can I DIY this?", "is it worth it?"

Extract 3-5 common objections with evidence/quotes.

3. **Category Entry Points (Buying Triggers)** ⭐ **CRITICAL**:
   - **What situations trigger customers to need this service?**
   - Search Reddit for: "[industry] when do you need" OR "[service] emergency" OR "had to call [service]"
   - Look for phrases like: "I needed X when...", "You should call them if...", "I wish I'd known about this when..."
   - Examples:
     * Locksmith CEPs: Lost keys, locked out, moving house, car key stopped working, break-in
     * Plumber CEPs: Burst pipe, boiler breakdown in winter, moving into new house, renovation
     * Dentist CEPs: Toothache, broken tooth, wedding coming up, job interview prep

Extract 5-10 category entry points (buying situations).

4. **Reddit Deep Dive** (Most Authentic Customer Voice):
   - Search Reddit for:
     * "r/[location] [service] recommendations"
     * "[industry] reddit" and sort by top posts
     * "[service] horror stories reddit" (to find pain points)
     * "[service] vs [alternative] reddit" (to find objections)
   - Extract actual customer quotes (verbatim) that show:
     * What they were worried about before buying
     * What made them choose one provider over another
     * What they wish they'd known
     * Common complaints about the industry

Extract 5-10 Reddit quotes with context.

Format as:
**Common Questions:**
1. [Question 1]
2. [Question 2]
[etc.]

**Common Objections:**
1. [Objection 1] - [evidence/source]
2. [Objection 2] - [evidence/source]
[etc.]

**Category Entry Points (Buying Triggers):**
1. [Trigger/situation 1]
2. [Trigger/situation 2]
[etc.]

**Reddit Customer Quotes:**
1. "[Quote 1]" - r/[subreddit] - [context: what they were discussing]
2. "[Quote 2]" - r/[subreddit] - [context]
[etc.]
```

**What to do:**
1. Paste the browser agent prompt
2. **Spend extra time on Reddit scraping** - this is gold for content creation
3. Review extracted questions, objections, CEPs, and Reddit quotes
4. Copy ALL sections into briefing document

**Why This Matters**:
- Reddit shows the REAL customer voice (not filtered/polished like reviews)
- Category Entry Points help you target the right buying situations in content
- Reddit quotes can be used verbatim in content to sound authentic
- This makes content 10x more persuasive and relatable

**Pro Tip**: If you find a particularly active subreddit (e.g., r/Essex, r/UKPersonalFinance, industry-specific subs), spend 5 extra minutes reading top threads. This insight is worth it.

---

## 🤖 STEP 2: Feed Information to the Agent

Now you have all the extracted client info. Here's how to give it to the agent.

### **⚠️ CRITICAL: Attach Actual Files from SaaS Tools**

**DO NOT just copy-paste data summaries. ATTACH THE ACTUAL EXPORT FILES.**

When you extract data from Hike, Ahrefs, or GSC, you MUST attach the CSV/Excel files to your briefing. The SEO agent needs the raw data, not summaries.

**What to Attach:**
- ✅ Hike keyword export (CSV/Excel)
- ✅ GSC performance export (CSV/Excel) - if not in Hike
- ✅ Ahrefs export (CSV/Excel) - if standalone
- ✅ Any other relevant data exports

**Why This Matters:**
- Raw data = more accurate strategy
- Agent can analyze full dataset, not just top 10-20 keywords
- Enables proper opportunity scoring and prioritization

---

### **Create a Briefing Document**

Copy and paste this template, filling in the information extracted from browser agents:

```
CLIENT: [Business name]

BUSINESS BASICS
- Industry: [What they do]
- Location: [Service area]
- Services:
  1. [Service 1]
  2. [Service 2]
  3. [Service 3]
  4. [Service 4]
  5. [Service 5]
- Website: [URL]

TONE OF VOICE
[How they described their brand personality]

BUSINESS GOAL
[Conversions / Awareness / Authority]

⚠️ ATTACHED FILES (CRITICAL - DO NOT SKIP):
- [ ] Hike keyword export.csv (Part D)
- [ ] Hike performance report.csv (Part E) - if available
- [ ] GSC export.csv (Part D/E) - if not in Hike
- [ ] Ahrefs export.csv (Part D/E) - if standalone
- [ ] Any other relevant data exports

KEYWORD DATA
⚠️ FILE MUST BE ATTACHED ABOVE - do not just list keywords here
If no file available, list 20-30 keywords:
  1. [Keyword 1]
  2. [Keyword 2]
  3. [Keyword 3]
  [etc. to 20-30 keywords]

CURRENT PERFORMANCE (if known)
⚠️ FILE SHOULD BE ATTACHED ABOVE if available
Summary:
- Monthly clicks: [X]
- Monthly impressions: [X]
- Average position: [X]
- Domain Rating: [X]

COMPETITORS (if known)
1. [Competitor 1 URL]
2. [Competitor 2 URL]
3. [Competitor 3 URL]

CUSTOMER INSIGHTS (if known)
Common questions:
- [Question 1]
- [Question 2]
- [Question 3]

Common objections:
- [Objection 1]
- [Objection 2]

Category Entry Points (buying triggers):
- [Trigger/situation 1]
- [Trigger/situation 2]
- [Trigger/situation 3]

Reddit customer quotes:
- "[Quote 1]" - r/[subreddit] - [context]
- "[Quote 2]" - r/[subreddit] - [context]
- "[Quote 3]" - r/[subreddit] - [context]
```

---

### **Send to the Agent**

**Paste the briefing into the agent and say:**

> "Please create a complete AI SEO strategy for this client. Follow the full workflow from Stage 0 to Stage 9."

**That's it!** The agent will now:
1. Validate the information (Stage 0)
2. Create strategic analysis (Stage 1)
3. Define framework (Stage 2)
4. Identify top keywords (Stage 2.5)
5. Do technical audit (Stage 3.1)
6. Recommend pages to create (Stage 3.5)
7. Create 30/60/90 day roadmap (Stage 4)
8. Generate copy examples (Stage 5)
9. Create full page drafts (Stage 6)
10. Quality check (Stage 6.5 - E-E-A-T)
11. Create link building strategy (Stage 7.5)
12. Document everything (Stage 9)

---

## ✅ STEP 3: What You'll Receive

The agent will create a complete strategy including:

### **Documents You'll Get**:
1. ✅ **Executive Summary** (2-3 pages for client)
2. ✅ **Keyword Priorities** (Top 20 keywords + "The Big One")
3. ✅ **Technical SEO Audit** (Issues to fix + how to fix them)
4. ✅ **Page Recommendations** (15-25 pages to create/optimize)
5. ✅ **30/60/90 Day Roadmap** (Week-by-week action plan)
6. ✅ **Copy Examples** (Title tags, meta descriptions, FAQs)
7. ✅ **Full Page Drafts** (3-5 complete pages ready to publish)
8. ✅ **Link Building Strategy** (50-100 targets + email templates)

### **What to Do With the Strategy**:

**Option A: Client Implements Themselves**
- Give them the strategy documents
- They follow the roadmap week by week

**Option B: You/Agency Implements**
- Use the strategy as implementation blueprint
- Follow the roadmap and checklists

**Option C: Hybrid**
- Client does some tasks (easy wins)
- You/agency does complex tasks (technical, link building)

---

## ⚠️ COMMON ISSUES & HOW TO FIX

### **Issue 1: Browser Agent Can't Access Hike Platform**

**What to do:**
- Option 1: Check if client is connected to Hike - may need to add them to platform first
- Option 2: Request keyword data export directly from client (CSV from Ahrefs/GSC/Hike)
- Option 3: Access Ahrefs or GSC directly if client has separate logins
- Option 4: Use browser agent to suggest keywords based on industry (Part D, Option 4)
- Last resort: Tell SEO agent: "No keyword data available. Please suggest 20-30 keywords based on industry and services."
- Note: Strategy will be less accurate without real data, but still usable

---

### **Issue 1a: GSC Not Connected to Hike**

**What to do:**
- Check if client has standalone GSC access
- Request GSC export directly from client
- Or proceed without GSC data (Part E is optional)
- Use Ahrefs data from Hike if available

---

### **Issue 2: Website Has Poor/Inconsistent Tone of Voice**

**What to do:**
- If browser agent finds inconsistent tone, use default: "Professional, clear, helpful - avoids corporate jargon"
- Alternatively, manually review 2-3 pages and describe the tone yourself
- SEO agent will apply consistent TOV in all generated content

---

### **Issue 3: Can't Extract Performance Data from Hike**

**What to do:**
- Check if GSC is connected to Hike (most common issue)
- If not connected: Request standalone GSC access or ask client to export CSV
- Check if Ahrefs is integrated in Hike platform
- Use free tools like Ubersuggest, AnswerThePublic for basic keyword research
- Or proceed without performance data (Part E is optional)
- Tell SEO agent: "No current performance data available"

---

### **Issue 4: Client Website Has No FAQ or Reviews**

**What to do:**
- Browser agent won't find customer insights (Part G)
- Skip Part G entirely, or
- Manually search "[business name] reviews" on Google and extract insights yourself
- Or tell SEO agent: "No customer insights available. Please use industry-standard objections and questions."

---

### **Issue 5: SEO Agent Says Information is Missing**

**What to do:**
- Check which required fields are empty (Business Basics, TOV, Goal, Keywords)
- Re-run specific browser agent prompt to extract missing data
- If data genuinely doesn't exist, tell SEO agent: "Client doesn't have [X data], please proceed with assumptions"

---

### **Issue 6: Strategy Seems Too Technical for Client**

**What to do:**
- Ask SEO agent: "Please create a simplified version of the executive summary suitable for a business owner with no SEO knowledge"
- Agent will create jargon-free version
- Focus client on the 30/60/90 roadmap (most actionable)

---

### **Issue 7: Forgot to Attach CSV/Excel Files** ⚠️

**What to do:**
- SEO agent will produce less accurate strategy without raw data
- Go back and export files from Hike/Ahrefs/GSC
- Re-submit briefing WITH files attached
- DO NOT just copy-paste 10-20 keywords - agent needs full dataset

**Why this matters:**
- Agent analyzes 100s-1000s of keywords from CSV, not just top 20
- Opportunity scoring requires search volume + position data
- Summary data loses critical information

---

### **Issue 8: Browser Agent Not Taking Over Window**

**If browser agent doesn't automatically control the browser, manually follow these steps:**

**For Hike Platform:**
1. Open browser and navigate to Hike platform manually
2. Log in to client's account
3. Navigate to: Keywords/Rankings section
4. Click "Export" → Select CSV or Excel format
5. Download file and attach to briefing
6. Repeat for Performance/GSC section if needed

**For Ahrefs:**
1. Open browser and navigate to Ahrefs Site Explorer
2. Enter client's website URL
3. Go to: Organic Keywords section
4. Click "Export" → Select all keywords → Download CSV
5. Attach file to briefing

**For GSC (if not in Hike):**
1. Open browser and navigate to Google Search Console
2. Select client's property
3. Go to: Performance → Search Results
4. Date range: Last 12 months
5. Click "Export" → Download CSV
6. Attach file to briefing

**Pro Tip:** Keep browser windows open while running browser agent prompts. Sometimes the agent needs manual assistance to complete exports.

---

## 🤖 QUICK REFERENCE: Browser Agent Workflow

**Use this workflow for every new client:**

---

**Step-by-Step Process:**

1. **Get client website URL** (this is all you need to start)

2. **Run 7 browser agent prompts** (from Step 1 above):
   - Part A: Business Basics
   - Part B: Tone of Voice
   - Part C: Business Goal
   - Part D: Keyword Data
   - Part E: Current Performance (optional)
   - Part F: Competitors (optional)
   - Part G: Customer Insights (optional)

3. **Compile briefing document** (copy-paste template from Step 2)

4. **Feed to SEO Strategy Agent** with prompt:
   > "Please create a complete AI SEO strategy for this client. Follow the full workflow from Stage 0 to Stage 9."

5. **Receive complete strategy** within minutes

6. **Quality check** (use checklist from bottom of guide)

7. **Package and deliver** to client

**Total Time**: 10-15 minutes of browser agent work → Complete strategy

---

## ✅ CHECKLIST: Before Sending to SEO Agent

Before you paste the briefing to the SEO agent, check you have extracted:

**MUST HAVE** (required for strategy):
- [ ] Business name, industry, location, services (Part A)
- [ ] Website URL
- [ ] Tone of voice - even if basic default (Part B)
- [ ] Business goal - conversions/awareness/authority (Part C)
- [ ] Keyword data - Ahrefs/GSC export OR browser agent suggested list of 20-30 keywords (Part D)
- [ ] **⚠️ CRITICAL: CSV/Excel files attached from Hike/Ahrefs/GSC** (not just summaries)

**SHOULD HAVE** (makes strategy 2x better):
- [ ] Current performance data - clicks, impressions, top keywords (Part E)
- [ ] Competitor URLs - at least 3 (Part F)
- [ ] Customer questions - at least 5 (Part G)
- [ ] Customer objections - at least 3 (Part G)
- [ ] **Category Entry Points - at least 5 buying triggers (Part G)** ⭐
- [ ] **Reddit customer quotes - at least 5 verbatim quotes (Part G)** ⭐

**If you have all MUST HAVE items, you're ready to generate the strategy!**

**Pro Tip**: Parts E-F-G (especially Reddit scraping in Part G) make the strategy 10x better. Reddit provides the most authentic customer voice and buying triggers. Worth the extra 10 minutes.

---

## 💡 PRO TIPS

### **Tip 1: Start with Hike Platform**
Most clients are connected to Hike. Always check Hike first for keyword data, GSC data, and TOV. This is faster than accessing multiple tools separately. Use browser agent to export relevant Hike reports.

### **Tip 2: Real Keyword Data = Better Strategy**
The quality of the strategy depends heavily on keyword data. Priority order:
1. Hike keyword exports (includes GSC + Ahrefs if integrated)
2. Standalone Ahrefs/SEMrush exports
3. Manual GSC exports (if not connected to Hike)
4. Browser agent suggested keywords (least accurate, but works)

### **Tip 3: Sense Check Hike's Auto-Generated TOV**
Hike auto-generates TOV, but always sense check it. Run browser agent on their social channels (Facebook, Instagram, LinkedIn) to verify the tone is accurate. Social media often shows the "real" brand voice.

### **Tip 4: Run Browser Agent Prompts in Parallel**
Don't run prompts one-by-one. Open multiple browser agent windows and run Parts A-G simultaneously. Total extraction time: 10-15 minutes instead of 30+.

### **Tip 5: Reddit Scraping (Part G) = Gold for Content**
Part G is "optional" but makes HUGE difference. **Reddit is the most valuable source** - real customer voice, unfiltered opinions, authentic language. Spend 10 minutes on Reddit scraping:
- Search "[industry] [location] reddit" for local discussions
- Look for buying trigger threads ("when do you need...", "had to call...")
- Extract verbatim quotes - use these in content to sound authentic
- Category Entry Points help target the right buying situations
The SEO agent will use these Reddit insights to create much more persuasive, relatable content.

### **Tip 6: One Primary Goal Only**
When browser agent suggests a business goal (Part C), stick to ONE. If client wants multiple goals (e.g., conversions + awareness), pick the most important one. Focused strategy > scattered strategy.

### **Tip 7: Save Browser Agent Prompts as Templates**
Copy Parts A-G prompts into a document. For each new client, just replace "[client website URL]" and "[industry]" placeholders. Speeds up your workflow significantly.

### **Tip 8: ALWAYS Attach CSV/Excel Files** ⚠️ **CRITICAL**
Never submit briefing without attaching the actual export files from Hike/Ahrefs/GSC. The SEO agent needs raw data (100s-1000s of keywords), not summaries (top 10-20 keywords). Files to attach:
- Hike keyword export.csv
- Hike performance report.csv (if available)
- GSC queries export.csv (if not in Hike)
- Ahrefs keywords export.csv (if standalone)

**Without files = Less accurate strategy. With files = 10x better strategy.**

---

## 🆘 NEED HELP?

**If you get stuck:**

1. **Browser agent not extracting data properly** - Try rephrasing the prompt or extract manually from website
2. **SEO agent needs more info** - Re-run specific browser agent prompt (Parts A-G) to get missing data
3. **Can't access tools** - Ask client to export and send CSV files directly
4. **Escalate to technical team** - If browser agents or SEO agent aren't working correctly

**Common Browser Agent Issues**:

- **"Can't access this website"** → Website may have bot protection; extract manually
- **"No data found"** → Website may not have the info (e.g., no FAQ page); skip that section
- **"Extraction incomplete"** → Re-run prompt with more specific instructions
- **"Browser not taking over window"** → See Issue 8 above for manual export steps from Hike/Ahrefs/GSC
- **"Can't export files"** → Manually navigate to tool, click Export button, download CSV, and attach to briefing

**Common SEO Agent Commands**:

- "Please create a complete SEO strategy for this client. Follow workflow Stages 0-9."
- "Client doesn't have [keyword data/performance data/etc.], please proceed with assumptions"
- "Please simplify this for a non-technical business owner"
- "Please create a 1-page executive summary"
- "Please explain [specific section] in simpler terms"

---

## ✅ SUCCESS CHECKLIST

After you receive the strategy from the agent:

- [ ] Check the strategy is complete (all stages 0-9)
- [ ] Check the tone of voice matches what client described
- [ ] Check the 30/60/90 roadmap is clear and actionable
- [ ] Check the keyword priorities include "The Big One"
- [ ] Check the page drafts match the client's brand voice
- [ ] Package everything into client-ready documents
- [ ] Schedule follow-up call to present strategy

---

**END OF CS TEAM GUIDE**

---

## 📝 SUMMARY

**Your Role**: Use browser agents to extract client information → Feed to SEO agent → Deliver complete strategy

**Primary Tools**:
- **Hike Platform** (for keyword data, GSC data, TOV auto-generation, Ahrefs integration)
- **Browser Agents** (for social channel analysis, competitor research, customer insights)

**You don't need to**:
- Be an SEO expert
- Speak to clients (unless clarification needed)
- Manually research keywords or competitors
- Create any content yourself

**You DO need to**:
1. Check Hike platform for client data (keyword data, GSC, TOV)
2. Run 7 browser agent prompts (Parts A-G) to extract/verify additional info
3. Sense check Hike's auto-generated TOV with social channels
4. Compile extracted data into briefing document
5. Feed briefing to SEO agent
6. Quality check the final strategy

**Time Investment**: 10-15 minutes of browser agent work + Hike exports = Complete 30/60/90 day SEO strategy

**Questions? Ask your team lead or technical team.** 🚀
