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

**Browser Agent Prompt:**

```
Go to [client website URL] and analyze the tone of voice used across:
- Homepage copy
- About page
- Service descriptions
- Blog posts (if available)

Analyze and describe:
1. Formality level: Is it casual/friendly, professional, or formal?
2. Language complexity: Simple/conversational or technical/expert?
3. Personality traits: Direct, warm, no-nonsense, empathetic, confident?
4. What they avoid: Corporate jargon, over-promising, technical terms?

Provide 3-5 example sentences from their website that demonstrate their tone.

Format as:
- Tone of Voice: [description in 1-2 sentences]
- Key Attributes: [list 3-5]
- Example phrases: [3-5 actual sentences from their site]
```

**What to do:**
1. Paste the browser agent prompt with the client's website URL
2. Review the extracted tone of voice
3. Copy into your briefing document

**Note**: If the website has inconsistent tone or poor copy, use: "Professional, clear, helpful - avoids corporate jargon"

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

#### **Option 1: Client Has Ahrefs/SEMrush Access** (BEST)

**What to do:**
1. Ask client to export their keyword data as CSV/Excel
2. Client sends you the file
3. **Done!** Attach to briefing

---

#### **Option 2: Client Has Google Search Console Access** (GOOD)

**Browser Agent Prompt (if client grants access):**

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

#### **Option 3: Automated Keyword Research** (OKAY)

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

**Note**: This option is less accurate than real keyword data, but works if client has no tools.

---

### **Part E: Current Performance** (3 minutes - OPTIONAL but helpful)

**Browser Agent Prompt (if client provides GSC access):**

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

**Alternative: Use Third-Party Tools**

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
1. Use whichever data source is available
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

### **Part G: Customer Insights** (5 minutes - OPTIONAL but makes content 10x better)

**Browser Agent Prompt:**

```
Analyze [client website URL] and related sources to extract customer insights:

1. Common Customer Questions:
   - Check FAQ page (if exists)
   - Check blog posts for question-based content
   - Search "[business name] + reviews" and analyze Google Reviews, Trustpilot, etc.
   - Look for "People Also Ask" on Google for their main keywords

Extract 5-10 common questions customers ask.

2. Common Objections:
   - Analyze reviews for negative feedback or concerns
   - Look for content addressing objections (e.g., "Why choose us", "Our guarantee")
   - Check competitor reviews to find industry-wide objections
   - Common objections: price concerns, trust issues, quality worries, timing/availability

Extract 3-5 common objections.

Format as:
**Common Questions:**
1. [Question 1]
2. [Question 2]
[etc.]

**Common Objections:**
1. [Objection 1] - [evidence/source]
2. [Objection 2] - [evidence/source]
[etc.]
```

**What to do:**
1. Paste the browser agent prompt
2. Review extracted questions and objections
3. Copy into briefing document

**Pro Tip**: This section makes content WAY better. Push to extract this data if possible.

---

## 🤖 STEP 2: Feed Information to the Agent

Now you have all the extracted client info. Here's how to give it to the agent.

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

KEYWORD DATA
[One of these]:
- ATTACHED: Ahrefs/GSC export file
- OR LIST:
  1. [Keyword 1]
  2. [Keyword 2]
  3. [Keyword 3]
  [etc. to 10-20 keywords]

CURRENT PERFORMANCE (if known)
- Monthly clicks: [X]
- Monthly impressions: [X]
- Top keywords: [List]

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

### **Issue 1: Browser Agent Can't Extract Keyword Data**

**What to do:**
- Option 1: Request keyword data export directly from client (Ahrefs/GSC CSV)
- Option 2: Use browser agent to suggest keywords based on industry (Part D, Option 3)
- Option 3: Tell SEO agent: "No keyword data available. Please suggest 20-30 keywords based on industry and services."
- Note: Strategy will be less accurate without real data, but still usable

---

### **Issue 2: Website Has Poor/Inconsistent Tone of Voice**

**What to do:**
- If browser agent finds inconsistent tone, use default: "Professional, clear, helpful - avoids corporate jargon"
- Alternatively, manually review 2-3 pages and describe the tone yourself
- SEO agent will apply consistent TOV in all generated content

---

### **Issue 3: Browser Agent Can't Access GSC or Ahrefs**

**What to do:**
- Ask client to export data themselves and send CSV file
- Or use free tools like Ubersuggest, AnswerThePublic for keyword research
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

**SHOULD HAVE** (makes strategy 2x better):
- [ ] Current performance data - clicks, impressions, top keywords (Part E)
- [ ] Competitor URLs - at least 3 (Part F)
- [ ] Customer questions - at least 5 (Part G)
- [ ] Customer objections - at least 3 (Part G)

**If you have all MUST HAVE items, you're ready to generate the strategy!**

**Pro Tip**: The more data you extract using browser agents (Parts E-G), the better and more accurate the strategy will be.

---

## 💡 PRO TIPS

### **Tip 1: Real Keyword Data = Better Strategy**
The quality of the strategy depends heavily on keyword data. Always try to get Ahrefs or GSC exports from the client first. Browser agent suggested keywords work, but are less accurate than real data.

### **Tip 2: Run All Browser Agent Prompts in Parallel**
Don't run prompts one-by-one. Open multiple browser agent windows and run Parts A-G simultaneously. Total extraction time: 10-15 minutes instead of 30+.

### **Tip 3: Customer Insights (Part G) = 10x Better Content**
Parts E-F-G are "optional" but make HUGE difference. Spend extra 5 minutes extracting customer questions and objections. The SEO agent will use these to create much more persuasive content.

### **Tip 4: Verify Tone of Voice Extraction**
Quickly scan the TOV that browser agent extracted from the website. If it seems off or generic, manually review 2-3 pages yourself and write a 1-sentence TOV description. This affects ALL content the SEO agent creates.

### **Tip 5: One Primary Goal Only**
When browser agent suggests a business goal (Part C), stick to ONE. If client wants multiple goals (e.g., conversions + awareness), pick the most important one. Focused strategy > scattered strategy.

### **Tip 6: Save Browser Agent Prompts as Templates**
Copy Parts A-G prompts into a document. For each new client, just replace "[client website URL]" and "[industry]" placeholders. Speeds up your workflow significantly.

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

**You don't need to**:
- Be an SEO expert
- Speak to clients (unless clarification needed)
- Manually research keywords or competitors
- Create any content yourself

**You DO need to**:
- Run 7 browser agent prompts (Parts A-G)
- Compile extracted data into briefing document
- Feed briefing to SEO agent
- Quality check the final strategy

**Time Investment**: 10-15 minutes of browser agent work = Complete 30/60/90 day SEO strategy

**Questions? Ask your team lead or technical team.** 🚀
