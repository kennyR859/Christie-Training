# Day 11 - Topic 12: AI Search Testing & Visibility

## Overview

You can't improve what you don't measure. Testing your AI visibility regularly shows you exactly where you stand in AI recommendations, what's working, what's not, and where to focus your optimization efforts.

This guide provides the complete testing framework for measuring and improving your AI discoverability across ChatGPT, Gemini, Perplexity, and other AI search engines.

**Key Instructor:** Mark Sweethimer

**Related Topics:** Day11_05 (AI Optimization Framework), Day11_07 (NAP Standardization)

---

## Why Test AI Visibility

### What You Can't See, You Can't Fix

**Without Testing:**
- You assume AI finds you
- You don't know your ranking
- You can't measure improvement
- You waste effort on ineffective strategies

**With Regular Testing:**
- You know exactly where you rank
- You see what content AI references
- You identify gaps and opportunities
- You measure ROI of optimization efforts

---

### Testing Frequency

**Monthly Minimum:**
- Quick spot-checks
- Track ranking changes
- Monitor competitor activity

**Quarterly Deep Dive:**
- Comprehensive testing across all AI platforms
- Source analysis (what platforms AI pulls from)
- Competitive landscape assessment
- Strategy adjustment

---

## The 4 Major AI Platforms to Test

### 1. ChatGPT (OpenAI)

**Why Test Here:**
- Most popular AI assistant
- 100M+ weekly users
- Primary recommendation source for many clients

**Market Share:** ~60% of AI search traffic

---

### 2. Google Gemini

**Why Test Here:**
- Google's AI (prioritizes Google Business data)
- Integrated with Google search
- Growing adoption

**Market Share:** ~25% of AI search traffic

---

### 3. Perplexity AI

**Why Test Here:**
- Shows exact source citations
- Reveals which platforms AI pulls from
- Growing among tech-savvy users

**Market Share:** ~10% of AI search traffic

---

### 4. Microsoft Copilot (Bing AI)

**Why Test Here:**
- Integrated with Bing search
- Microsoft ecosystem users
- Underutilized by competitors

**Market Share:** ~5% of AI search traffic

---

## Testing Method 1: ChatGPT Temporary Chat

### Why Use Temporary Chat

**The Problem:**
Regular ChatGPT "remembers" you and your conversations

**The Solution:**
Temporary Chat mode = Clean slate, unbiased results

---

### How to Use Temporary Chat

**Step-by-Step:**

1. **Open ChatGPT**
2. **Click Profile Icon** (top right)
3. **Select "Temporary Chat"**
4. **Note:** This session won't train AI or remember you
5. **Run your test queries**
6. **Exit and results disappear**

---

### Test Queries to Run

**Query 1: Direct Area Search**
```
"Who is the best real estate agent in [Your Town]?"
```

**What to Look For:**
- Are you mentioned?
- What position (1st, 2nd, 3rd, not at all)?
- What information does AI share about you?
- What sources does it cite?

---

**Query 2: Specialty Search**
```
"I need a real estate agent who specializes in
[Your School District/Neighborhood]"
```

**What to Look For:**
- Does your hyper-local content pay off?
- Are you recommended for your niche?
- What specific expertise does AI mention?

---

**Query 3: Client Type Search**
```
"Recommend a real estate agent for first-time buyers
in [Your Area]"
```

**What to Look For:**
- Does your specialty positioning work?
- Are you matched to your target client?

---

**Query 4: Comparison Search**
```
"Who are the top 3 real estate agents in [Your County]
for [Your Specialty]?"
```

**What to Look For:**
- Are you in top 3?
- Who are your competitors?
- What makes them rank higher?

---

**Query 5: Direct Name Search**
```
"Tell me about [Your Full Name] real estate agent
in [Your Town]"
```

**What to Look For:**
- What information does AI have about you?
- Is it accurate?
- What sources is it pulling from?
- Are there gaps or errors?

---

### Documenting Results

**Create Testing Spreadsheet:**

| Date | Query | Platform | Mentioned? | Position | Info Accuracy | Sources Cited | Notes |
|------|-------|----------|------------|----------|---------------|---------------|-------|
| 11/6/24 | "Best agent Mahwah" | ChatGPT | ✅ | #3 | 90% | Google Business, Zillow | Missing school district expertise |
| 11/6/24 | "Ramapo school specialist" | ChatGPT | ✅ | #1 | 95% | Google, reviews | Excellent positioning |
| 11/6/24 | "First-time buyers Mahwah" | ChatGPT | ❌ | Not listed | N/A | N/A | Need more content on this |

---

## Testing Method 2: Have Someone Else Search

### Why This Works Better

**Advantages:**
- Completely clean search (AI doesn't know you)
- Most realistic to actual client experience
- Can test from different geographic locations
- Eliminates your personal AI "contamination"

---

### How to Recruit Testers

**Option 1: Friends/Family**
```
"Hey, can you do me a quick favor? Open ChatGPT and ask:
'Who is the best real estate agent in Mahwah?'

Screenshot what comes up and text it to me. Thanks!"
```

**Option 2: Virtual Assistants**
- Hire on Fiverr ($5-10)
- Request AI searches with screenshots
- Get multiple locations/devices

**Option 3: Colleague Exchange**
- Partner with agent in different market
- Test each other's AI visibility
- Share insights and strategies

---

### What to Have Them Test

**Basic Tests:**
1. "Best real estate agent in [Your Town]"
2. "[Your Name] realtor" (check info accuracy)
3. "Agent for [Your Specialty] in [Your Area]"

**Advanced Tests:**
4. Same searches on mobile vs desktop
5. Same searches in different browsers
6. Same searches from different locations
7. Comparison with top competitors

---

## Testing Method 3: Google Gemini Testing

### Why Gemini Is Different

**Key Differences:**
- Heavily prioritizes Google Business data
- Direct access to Google Maps
- Integrated with Google ecosystem

**Expected Result:** You should rank HIGHER on Gemini if your Google Business is optimized

---

### How to Test Gemini

1. **Go to gemini.google.com**
2. **Log out** (or use incognito mode)
3. **Run same queries** as ChatGPT tests
4. **Compare results** to ChatGPT

**Hypothesis:**
If Google Business is strong → Gemini ranking > ChatGPT ranking
If Google Business is weak → Gemini ranking ≈ or < ChatGPT ranking

---

### Gemini-Specific Queries

**Query 1: Map-Based**
```
"Show me the best real estate agents near
[Specific Landmark] in [Town]"
```

**Query 2: Google Review Focused**
```
"Real estate agents in [Town] with best reviews"
```

**Query 3: Local Business**
```
"Local real estate professionals in [Neighborhood]"
```

---

## Testing Method 4: Perplexity AI (Source Analysis)

### Why Perplexity Is Valuable

**Unique Feature:** Shows exact source citations

**What This Reveals:**
- Which platforms AI is pulling from
- Which of your profiles are strongest
- Where your information is inconsistent
- What competitors are doing right

---

### How to Test Perplexity

1. **Go to perplexity.ai**
2. **Run search queries**
3. **Click on source numbers** (e.g., [1], [2], [3])
4. **Analyze which sources AI uses**

**Example Result:**
```
"Based on reviews and local expertise [1][2], the
top agents in Mahwah include:

1. Jane Smith - Specializes in Ramapo school district
[1] Google Business Profile
[2] Zillow Reviews
[3] Patch.com article

2. John Doe - Luxury properties expert
[1] Realtor.com
[2] LinkedIn Profile
[3] The Real Deal article
```

---

### What to Learn from Sources

**If AI Cites:**

**Google Business** → Your Google optimization is working
**Zillow/Realtor.com** → Your real estate profiles are strong
**Published Articles** → Your authority building is paying off
**Social Media** → Your content strategy is visible
**Yelp/Reviews** → Your review collection is effective

**If AI Doesn't Cite You:**
- Those platforms need optimization
- Content isn't visible/complete
- Competitors dominate those sources

---

## Testing Your Competitors

### Competitive Intelligence

**Why Test Competitors:**
- See what's working in your market
- Identify gaps you can fill
- Benchmark your performance
- Find differentiation opportunities

---

### Competitor Testing Process

**Step 1: Identify Top 3-5 Competitors**
- Agents who appear in AI results
- Agents with similar specialties
- Top producers in your area

**Step 2: Test Their Visibility**
```
"Tell me about [Competitor Name] real estate agent"

ChatGPT response reveals:
- What platforms AI finds them on
- What expertise AI associates with them
- What content/reviews AI references
- How they position themselves
```

**Step 3: Analyze Gaps**

| Element | You | Competitor A | Competitor B | Gap/Opportunity |
|---------|-----|--------------|--------------|-----------------|
| Google Reviews | 8 | 25 | 15 | Need more reviews |
| School District Content | ✅ Strong | ❌ None | ⚠️ Weak | Your advantage |
| Published Articles | 2 | 0 | 5 | Opportunity to match B |
| YouTube Videos | 5 | 0 | 0 | Your unique advantage |

**Step 4: Develop Counter-Strategy**
- Double down on your advantages
- Fill critical gaps
- Differentiate where competitors are weak

---

## Monthly Testing Routine (15 minutes)

### Quick Monthly Check

**1st of Each Month:**

**5 Minutes: ChatGPT Test**
```
Temporary Chat:
1. "Best agent in [Town]" - Am I listed?
2. "[My Name] realtor" - Info accurate?
3. "[My Specialty] agent [Town]" - Do I rank?

Record: Position + any changes from last month
```

**5 Minutes: Gemini Test**
```
Same 3 queries on Gemini
Compare to ChatGPT results
Note any differences
```

**5 Minutes: Analysis**
```
Changes from last month?
▲ Improved ranking → What did I do differently?
▼ Dropped ranking → What changed? Competitor activity?
→ No change → Need to adjust strategy
```

---

## Quarterly Deep Dive (1 hour)

### Comprehensive Quarterly Assessment

**Every 3 Months:**

**Week 1: Comprehensive Testing (30 min)**
- All 4 AI platforms (ChatGPT, Gemini, Perplexity, Copilot)
- 10 different queries
- Competitor comparison
- Source analysis

**Week 2: Gap Analysis (15 min)**
- What improved?
- What got worse?
- What didn't change?
- Competitor movement?

**Week 3: Strategy Adjustment (15 min)**
- Focus areas for next quarter
- Content creation priorities
- Platform optimization needs
- Review collection goals

---

## Analyzing Your Results

### If You Don't Appear At All

**Possible Reasons:**
❌ Google Business not verified
❌ Profiles incomplete
❌ No recent content (recency bias)
❌ NAP data inconsistent
❌ No reviews
❌ Competitors have much stronger presence

**Action Steps:**
1. ✅ Verify Google Business immediately
2. ✅ Complete all profile fields
3. ✅ Post weekly for 4 weeks straight
4. ✅ Standardize NAP across all platforms
5. ✅ Get 5 reviews minimum
6. ✅ Test again in 30 days

---

### If You Appear But Info Is Wrong

**Common Errors:**
❌ Old phone number showing
❌ Previous office address
❌ Outdated bio
❌ Wrong specialties listed
❌ Conflicting information

**Action Steps:**
1. ✅ Find source of wrong information
2. ✅ Update all platforms with correct NAP
3. ✅ Request removal from old directories
4. ✅ Wait 2 weeks for AI to update
5. ✅ Test again

---

### If You Appear Low in Rankings

**Why This Happens:**
- Competitors have more reviews
- Competitors post more frequently
- Their content is more hyper-local
- They have published articles
- Their profiles are more complete

**Action Steps:**
1. ✅ Analyze top-ranking competitors
2. ✅ Match or exceed their review count
3. ✅ Post more frequently
4. ✅ Create more hyper-local content
5. ✅ Get an article published
6. ✅ Test monthly to track improvement

---

### If You Appear with Good Ranking

**Don't Stop! Maintain Position:**

**Maintenance Mode Actions:**
- ✅ Continue weekly posting
- ✅ Request 2-3 new reviews/month
- ✅ Keep all platforms updated
- ✅ Monitor competitor activity
- ✅ Test monthly to maintain position
- ✅ Expand into new neighborhoods/specialties

**Growth Mode Actions:**
- ✅ Increase posting frequency
- ✅ Add more hyper-local content
- ✅ Get more published articles
- ✅ Expand to additional platforms
- ✅ Target higher-value keywords

---

## Creating a Testing Dashboard

### Simple Google Sheet Template

**Sheet 1: Monthly Tests**

| Month | Platform | Query Type | Rank | Position Change | Notes |
|-------|----------|------------|------|-----------------|-------|
| Jan 24 | ChatGPT | General | #4 | N/A | Baseline |
| Feb 24 | ChatGPT | General | #3 | ▲ +1 | Added 3 reviews |
| Mar 24 | ChatGPT | General | #2 | ▲ +1 | Published article |

---

**Sheet 2: Competitor Tracking**

| Competitor | Jan | Feb | Mar | Trend | Their Strategy |
|------------|-----|-----|-----|-------|----------------|
| Jane Smith | #1 | #1 | #1 | → | 50+ reviews, weekly posts |
| Bob Jones | #2 | #3 | #4 | ▼ | Stopped posting |
| You | #4 | #3 | #2 | ▲ | Consistency paying off |

---

**Sheet 3: Source Analysis**

| Platform | Jan | Feb | Mar | Status | Next Action |
|----------|-----|-----|-----|--------|-------------|
| Google Business | ✅ | ✅ | ✅ | Strong | Maintain |
| Zillow | ⚠️ | ✅ | ✅ | Improved | Maintain |
| Published Articles | ❌ | ❌ | ✅ | Fixed | Add more |
| YouTube | ❌ | ⚠️ | ✅ | Growing | Increase frequency |

---

## Advanced Testing Techniques

### Geographic Testing

**Test from Multiple Locations:**

**Why:** AI may give different results based on searcher's location

**How:**
- Use VPN to test from different cities
- Have friends in neighboring towns test
- Check if you appear for adjacent markets

**Insights:**
- Are you visible beyond your primary town?
- Do you appear for neighboring areas?
- Should you expand service area keywords?

---

### Device Testing

**Mobile vs Desktop:**

**Why:** Results may vary by device

**How:**
- Test same query on phone and laptop
- Check voice search vs typed
- Compare app vs browser

---

### Time-Based Testing

**Test Same Query Over Time:**

**Why:** Track improvement and seasonal changes

**How:**
- Same 5 queries monthly
- Chart ranking changes
- Identify trends and patterns

---

## When to Escalate Efforts

### Warning Signs You Need More Optimization

**Red Flags:**
- ❌ 3 months of testing, still not appearing
- ❌ Ranking dropped 3+ positions
- ❌ New competitors dominating
- ❌ Wrong information persisting
- ❌ Only appearing for direct name search

**Action:** Run through entire AI Optimization Framework again (Day11_05)

---

### Success Indicators

**Green Lights:**
- ✅ Appearing in top 3 for general searches
- ✅ #1 for specialty/niche searches
- ✅ Accurate information across all platforms
- ✅ Cited in Perplexity sources
- ✅ Higher rank on multiple AI platforms
- ✅ Leads mentioning finding you via AI search

**Action:** Maintain current strategy, expand to new keywords

---

## Key Quotes

> "You're not trying to outsmart ChatGPT. You're trying to stay relevant to ChatGPT."

---

## Action Items

### This Week
- [ ] Run first ChatGPT test (5 queries, temporary chat)
- [ ] Test same queries on Gemini
- [ ] Document results in spreadsheet
- [ ] Identify top 3 competitors to track
- [ ] Ask friend to run independent test

### This Month
- [ ] Monthly testing routine (15 min on 1st)
- [ ] Test Perplexity for source analysis
- [ ] Analyze gaps vs competitors
- [ ] Adjust content strategy based on results
- [ ] Retest at end of month to measure progress

### This Quarter
- [ ] Comprehensive quarterly deep dive
- [ ] Test all 4 major AI platforms
- [ ] Full competitive analysis
- [ ] Strategy adjustment based on findings
- [ ] Set next quarter goals and benchmarks

---

## Summary

AI visibility testing is how you know if your optimization efforts are working. Monthly 15-minute tests keep you informed of your ranking and competitive position. Quarterly deep dives reveal strategic opportunities and necessary adjustments.

The key testing tools: ChatGPT Temporary Chat (unbiased results), Gemini (Google ecosystem), Perplexity (source analysis), and having others test (most realistic). Track your results, analyze competitors, and adjust your strategy based on data.

Within 3-6 months of consistent optimization and testing, you should see measurable improvement: moving from "not appearing" to "top 3 rankings" for your target searches. Test monthly, optimize continuously, and dominate your local market in AI search results.
