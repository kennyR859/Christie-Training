# Day 5 - Topic 03: Data Export & CRM Integration

**Topic:** Technical workflow for moving Remine data into Platform CRM
**Difficulty:** Beginner-Intermediate
**Time:** 30-45 minutes per export

---

## 🎯 Why This Matters

**Without CRM Integration:**
- ❌ Data sits in Excel doing nothing
- ❌ No way to track who you've called
- ❌ Manual tracking (spreadsheets, sticky notes)
- ❌ Forget to follow up
- ❌ Leads fall through cracks

**With CRM Integration:**
- ✅ Automatic follow-up reminders
- ✅ Track every touchpoint
- ✅ Send mass emails with personalization
- ✅ Segment by engagement level
- ✅ Measure ROI accurately

**Bottom Line:** Your CRM IS your business. Feed it quality data.

---

## 📤 Step 1: Exporting from Remine

### Pre-Export Checklist

**Before clicking "Export":**

✅ **Verify your filters** - Is this EXACTLY who you want?
✅ **Check property count** - Under 10,000?
✅ **Name your cart descriptively** - e.g., "Ridgewood_ARM_Nov2024"
✅ **Double-check geography** - Right town/zip codes?

---

### The Export Process (Detailed)

**Step 1: From Remine Map View**

After applying all filters:

1. Click **"Select All"** (checkbox at top of results list)
   - You'll see: "X properties selected"

2. Click **"Cart"** button (usually top right)

3. **Name your cart:**
   ```
   Good names:
   - Bergen_Downsizers_Nov2024
   - Ridgewood_ARM_Reset_Q4
   - Hoboken_Investors_December

   Bad names:
   - List1
   - Farm
   - Export
   ```

4. Click **"Create"** then **"Add to Cart"**

5. Wait for confirmation (green checkmark or success message)

---

**Step 2: Go to Cart View**

1. Click **"Cart"** or **"My Carts"** tab

2. Find your newly created cart

3. **Select the entire cart** (checkbox at top)
   - OR select specific properties within the cart

---

**Step 3: Export Configuration**

1. Click **"Export"** button

2. **IMPORTANT: Check ALL columns**

   Even if you think you don't need certain data, check it anyway. Examples:

   ✅ Owner Name
   ✅ Property Address
   ✅ Mailing Address (often different!)
   ✅ Phone Number(s)
   ✅ Email Address(es)
   ✅ Property Value
   ✅ Equity
   ✅ Loan Type
   ✅ Interest Rate
   ✅ Ownership Time
   ✅ Last Sale Date
   ✅ Last Sale Price
   ✅ Tax Assessment
   ✅ Annual Taxes
   ✅ Bedrooms/Bathrooms
   ✅ Square Footage
   ✅ Year Built

3. Click **"Export"** or **"Download"**

4. **Wait for processing** (15 seconds to 2 minutes)

5. **Download notification** appears
   - Top of screen OR
   - In "Alerts/Notifications" bell icon

6. Click **"Download"** when ready

---

**Step 4: Save Your File**

File downloads to your **Downloads** folder as:
- `Remine_Export_[Date].csv` or
- `CartName_Export.csv`

**Immediately:**
1. **Rename the file** to something descriptive:
   ```
   Ridgewood_ARM_Export_Nov5_2024.csv
   ```

2. **Move it to a dedicated folder:**
   ```
   Documents/RealEstate/Remine_Exports/
   ```

3. **Create backup copy** (store in cloud: Google Drive, Dropbox, OneDrive)

---

## 🧹 Step 2: Data Cleaning in Excel

### Opening the File Correctly

**Method 1: Direct Open (can cause formatting issues)**
- Double-click CSV file
- Opens in Excel with default formatting
- ⚠️ May lose leading zeros in zip codes
- ⚠️ Phone numbers may show as scientific notation

**Method 2: Import Wizard (better control)**

1. Open **blank Excel workbook**

2. Go to **Data → Get External Data → From Text/CSV**

3. Select your Remine CSV file

4. **Import settings:**
   - File origin: Windows (ANSI) or UTF-8
   - Delimiter: Comma
   - **Text columns:** Zip Code, Phone Number (prevents auto-formatting)

5. Click **Load**

---

### Common Formatting Fixes

**Fix 1: Phone Numbers**

**Problem:**
```
Shows as: 2.01555E+11
Should be: 201-555-1234
```

**Solution:**
1. Select phone number column (entire column)
2. Right-click → **Format Cells**
3. Choose **"Text"** (NOT "Number")
4. If already messed up, use formula:
   ```
   =TEXT(A2,"000-000-0000")
   ```

---

**Fix 2: Zip Codes**

**Problem:**
```
Shows as: 7450
Should be: 07450
```

**Solution:**

**Option A: Format as Text First**
1. Before opening, import as text (see Method 2 above)

**Option B: Fix After Opening**
1. Select zip code column
2. Format as Text
3. Use formula to add leading zero:
   ```
   =IF(LEN(A2)=4,"0"&A2,A2)
   ```

---

**Fix 3: Remove Invalid Data**

**Common Invalid Entries:**

```
Phone: 000-000-0000 → DELETE
Phone: 123-456-7890 → DELETE (fake number)
Email: noemail@gmail.com → DELETE
Email: test@test.com → DELETE
Name: (blank) → Try to find from other sources or DELETE row
```

**How to Clean:**
1. Sort by Phone column
2. Scroll to find patterns of 000-000-0000
3. Select those rows
4. Right-click → Delete rows

Repeat for email, name fields.

---

**Fix 4: Standardize Formatting**

**Name Capitalization:**
```
Original: JOHN SMITH or john smith
Better: John Smith
```

**Excel Formula:**
```
=PROPER(A2)
```
This converts to Title Case.

**Address Standardization:**
```
Original: 123 main street
Better: 123 Main Street
```

Use `=PROPER(B2)` on address column too.

---

### Adding Custom Columns

**Essential Custom Columns to Add:**

**1. Source**
```
Column Header: Source
Value: Remine - ARM Farm Nov 2024
Why: Know where this lead came from later
```

**2. Lead Score**
```
Column Header: Lead Score
Value: 1-10 (based on motivation indicators)
Why: Prioritize who to call first
```

**Example Scoring:**
```
ARM + High Equity + 20+ years ownership = 9/10
ARM + Low Equity + 5 years ownership = 5/10
```

**3. Status**
```
Column Header: Status
Value: Not Contacted (initial)
Why: Track progress through pipeline
```

**4. Notes**
```
Column Header: Notes
Value: (blank initially)
Why: Add context after calls
```

**5. Last Contact Date**
```
Column Header: Last Contact
Value: (blank initially)
Why: Track when you last reached out
```

**6. Next Action**
```
Column Header: Next Action
Value: (blank or "Initial Call")
Why: Know what to do next
```

---

### Remove Duplicates

**Why Duplicates Happen:**
- Same owner, multiple properties
- Data errors in source
- Accidentally exported same cart twice

**How to Remove:**

1. Select **all data** (Ctrl+A)

2. Go to **Data → Remove Duplicates**

3. **Choose unique identifier:**
   - Primary: Property Address
   - Secondary: Owner Name

4. Click **OK**

5. Excel shows: "X duplicate values found and removed"

---

## 📥 Step 3: Importing to Platform CRM

### Pre-Import Preparation

**1. Map Your Fields (Know Before You Import)**

```
Excel Column → Platform CRM Field
-----------------------------------
Owner Name → Contact: First Name + Last Name
Property Address → Property: Address
Mailing Address → Contact: Mailing Address
Phone → Contact: Phone
Email → Contact: Email
Property Value → Property: Estimated Value
Equity → Property: Equity
Loan Type → Property: Loan Type
etc.
```

**2. Decide on Import Strategy**

**Option A: Create New Contacts**
- For brand new farm
- No existing contacts in CRM from this group

**Option B: Update Existing Contacts**
- If you've imported similar data before
- Updates info for existing, creates new for rest

**Recommendation for First Time:** Option A (Create New)

---

### Platform CRM Import Steps

**Step 1: Access Import Tool**

1. Log into **Platform** (www.platform.christies.com or your CRM URL)

2. Navigate to **Contacts → Import Contacts**

3. Click **"Import from File"** or **"Upload CSV"**

---

**Step 2: Upload Your File**

1. Click **"Choose File"** or **"Browse"**

2. Select your **cleaned Excel file**
   - Save Excel as CSV first if needed: File → Save As → CSV

3. Click **"Upload"** or **"Next"**

4. Wait for upload (5-30 seconds depending on size)

---

**Step 3: Map Fields**

This is **THE MOST IMPORTANT STEP**. Take your time.

**Platform shows you:**
- Left side: Your Excel columns
- Right side: Platform CRM fields (dropdown)

**You need to match them up:**

```
Excel Column          →  Platform Field
-----------------------------------------
Owner Name            →  Contact Name (or First/Last separate)
Property Address      →  Property Address
Mailing Address       →  Mailing Address
Phone                 →  Phone (choose type: Mobile, Home, Work)
Email                 →  Email
Property Value        →  Custom Field: Property Value
Equity                →  Custom Field: Equity
Loan Type             →  Custom Field: Loan Type
Source                →  Lead Source
Lead Score            →  Custom Field: Lead Score
Status                →  Contact Status
```

**⚠️ Common Mapping Mistakes:**

❌ **Wrong:** Property Address → Contact Address
✅ **Right:** Property Address → Property Address (separate field)

❌ **Wrong:** Owner Name → Company Name
✅ **Right:** Owner Name → Contact Name

---

**Step 4: Set Import Options**

**Duplicate Handling:**
- ✅ **Skip duplicates** (don't import if email/phone already exists)
- OR
- ☐ Update existing contacts (overwrites old data)

**Recommendation:** Skip duplicates (safer for first import)

---

**Tags:**
- ✅ **Create new tag** for this import
  - Tag name: "Remine_ARM_Nov2024"
  - Why: Easy to find these contacts later

**Assignment:**
- ✅ **Assign to:** You (your name)
- Why: These are YOUR leads

**List/Group:**
- ✅ **Add to list:** "ARM Farm" or create new list
- Why: Can send mass emails to this list

---

**Step 5: Review & Confirm**

Platform shows **preview** of first 5-10 rows.

**Check:**
- ✅ Names look correct
- ✅ Addresses formatted properly
- ✅ Phone numbers have area codes
- ✅ Emails look valid

**If anything looks wrong:** Go back to Step 3, fix mapping.

**If everything looks good:** Click **"Import"** or **"Confirm"**

---

**Step 6: Wait for Import Processing**

**Small import (under 100):** 10-30 seconds
**Medium (100-500):** 1-2 minutes
**Large (500-1000+):** 5-10 minutes

**Don't close browser** during this process.

---

**Step 7: Verify Import Success**

**After processing completes:**

1. Go to **Contacts → All Contacts**

2. **Filter by tag:** "Remine_ARM_Nov2024" (or whatever you named it)

3. **Count results:** Should match your import count

4. **Spot check 5-10 random contacts:**
   - Click to open detail view
   - Verify all fields imported correctly
   - Check property data is attached

**If anything is wrong:**
- Delete the import (select all with tag → Delete)
- Fix the CSV file
- Re-import

---

## 🏷️ Step 4: Organizing in CRM

### Creating Smart Lists/Segments

**Why Segment?**

Not all 200 leads are equal. You want to prioritize.

**Segment 1: Hot Prospects**

**Criteria:**
- Lead Score: 8-10
- ARM loan + High equity + Long ownership

**Actions:**
- Call these FIRST
- More frequent touchpoints
- Personal outreach (not just mass email)

---

**Segment 2: Warm Prospects**

**Criteria:**
- Lead Score: 5-7
- ARM loan but lower motivation signals

**Actions:**
- Call after Hot Prospects
- Mix of personal + automated touches
- Monitor for engagement signals

---

**Segment 3: Cold/Nurture**

**Criteria:**
- Lead Score: 1-4
- Data is incomplete OR low motivation

**Actions:**
- Automated email campaigns only
- Quarterly check-ins
- Watch for status changes

---

### Setting Up Automated Workflows

**Workflow 1: Welcome Sequence (First 30 Days)**

```
Day 1: Import → Auto-send welcome email
     Subject: "Your Neighborhood Market Update"
     Content: Market analysis, your value prop

Day 7: Auto-send educational email
     Subject: "ARM Resets: What You Need to Know"
     Content: Explanation + link to calculator

Day 14: Task created → "Call [Name]"
     You manually call and update status

Day 21: Auto-send case study
     Subject: "How the Johnsons Saved $2,000/Month"
     Content: Client success story

Day 30: Task created → "Second call attempt"
```

---

**Workflow 2: Engagement-Based**

```
IF contact opens 3+ emails
  → Tag as "Engaged"
  → Create task: "Priority call - engaged prospect"
  → Send personal video message

IF contact clicks link in email
  → Tag as "Hot Lead"
  → Immediate alert to you
  → Call same day

IF contact doesn't open any emails in 60 days
  → Tag as "Cold"
  → Remove from frequent emails
  → Add to quarterly nurture only
```

---

### Tracking Call Activity

**After Every Call, Update CRM:**

**Fields to Update:**

1. **Last Contact Date:** Today's date (auto or manual)

2. **Call Status:**
   - Answered
   - No answer (left voicemail)
   - No answer (no voicemail)
   - Wrong number
   - Do not call

3. **Notes:** Brief summary
   ```
   Example:
   "Spoke with owner. Interested in market value but not ready to
   sell yet. Kids finish school in June. Follow up April."
   ```

4. **Next Action:**
   - Follow up April 1
   - Send market analysis
   - Schedule listing appointment
   - Remove from list (not interested)

5. **Lead Score:** Adjust based on conversation
   - Increase if more interested than expected
   - Decrease if less motivated

---

**Set Reminders:**

If they say "Call me in 3 months":
- Create task for 3 months from today
- Add to calendar
- CRM will remind you

---

## 📊 Step 5: Measuring & Reporting

### Key Metrics to Track

**Volume Metrics:**

```
Total Contacts in Farm: 200
Contacted (attempted): 180 (90%)
Reached (actually spoke to): 95 (48% contact rate)
```

**Engagement Metrics:**

```
Email open rate: 35% (good is 25-40%)
Email click rate: 8% (good is 5-10%)
Market analysis requests: 12 (6% of total)
Appointments set: 4 (2% of total)
```

**Conversion Metrics:**

```
Listing appointments: 4
Listings taken: 1
Listings sold: 0 (too soon)
Gross Commission (potential): $15,000
```

**ROI Metrics:**

```
Investment: $500 setup + $900 marketing (3 months) = $1,400
Return: $15,000 (one listing)
ROI: 971%
Time to first listing: 90 days
```

---

### Platform CRM Reports

**Built-In Reports to Use:**

**1. Contact Activity Report**
- Shows all touches per contact
- See who you've contacted most/least
- Identify who needs follow-up

**2. Email Performance Report**
- Open rates by campaign
- Click rates by email
- Best-performing subject lines

**3. Pipeline Report**
- Contacts by status
- How many in each stage
- Average time in each stage

**4. Source Report**
- Leads by source (Remine, UPCity, referrals, etc.)
- Conversion rate by source
- ROI by source

---

### Creating Custom Dashboards

**Your ARM Farm Dashboard:**

**Top Section:**
- Total contacts: 200
- Hot leads: 18
- Appointments this month: 2
- Listings YTD: 1

**Middle Section:**
- Calls made this week: 35
- Emails sent this week: 200 (automated)
- Responses this week: 8

**Bottom Section:**
- Next 5 follow-up tasks (today's to-do list)
- Upcoming appointments
- Recent activity feed

**Update:** Daily or weekly to stay on track

---

## 🔄 Step 6: Ongoing Maintenance

### Monthly Data Refresh

**Why:**
- Property values change
- Owners move/sell
- Phone numbers change
- Equity positions shift

**How:**

**Each Month:**

1. **Re-export from Remine** with same filters

2. **Compare to existing CRM data**
   - Who sold? (remove from farm)
   - Who's new? (add to farm)
   - What changed? (update fields)

3. **Update CRM**
   - Import new contacts
   - Update changed contacts
   - Archive sold properties

---

### Quarterly Deep Clean

**Every 3 Months:**

**Task 1: Remove Dead Leads**
- Wrong numbers → Delete
- Do Not Call requests → Archive
- Sold with another agent → Archive
- Moved out of area → Archive

**Task 2: Re-Score Leads**
- Who's more engaged now? → Increase score
- Who never responds? → Decrease score
- New data from Remine → Adjust based on equity/rate changes

**Task 3: Audit Data Quality**
- Missing emails → Research and add
- Missing info → Fill in gaps
- Duplicate contacts → Merge

---

## ⚠️ Common Mistakes & How to Avoid

### Mistake 1: Importing Without Cleaning

**Problem:**
```
Import 500 contacts with bad data
→ 200 wrong phone numbers
→ 100 invalid emails
→ Waste time calling wrong numbers
→ Emails bounce (hurts sender reputation)
```

**Solution:**
**ALWAYS clean data in Excel BEFORE importing.**

---

### Mistake 2: Not Tagging on Import

**Problem:**
```
Import 200 ARM leads with no tag
→ They mix with your 5,000 other contacts
→ Can't find them later
→ Can't measure ROI
→ Can't send targeted campaigns
```

**Solution:**
**ALWAYS create unique tag for each import.**

---

### Mistake 3: Importing Without Strategy

**Problem:**
```
Import data → Don't call anyone for 3 months
→ Data goes stale
→ Miss the timing window (ARM resets happen)
→ Wasted effort
```

**Solution:**
**Have outreach plan BEFORE importing:**
- When will you call?
- What's your script?
- What's your follow-up sequence?

---

### Mistake 4: Not Updating After Calls

**Problem:**
```
Call 50 people
→ Don't update CRM
→ 2 months later, can't remember who said what
→ Call same person twice (awkward)
→ Miss follow-up opportunities
```

**Solution:**
**Update CRM immediately after EVERY call.**

Make it a rule: No call = no update = didn't happen.

---

## 📋 Complete Integration Checklist

**✅ Before Import**
- [ ] Remine data exported with all columns
- [ ] File saved with descriptive name
- [ ] Backup copy created
- [ ] Data cleaned in Excel (phone, zip, names)
- [ ] Invalid entries removed
- [ ] Custom columns added (Source, Lead Score, Status)
- [ ] Duplicates removed

**✅ During Import**
- [ ] Platform CRM logged in
- [ ] Import tool accessed
- [ ] CSV uploaded successfully
- [ ] Fields mapped correctly (double-checked)
- [ ] Duplicate handling set (Skip duplicates)
- [ ] Tag created (unique name)
- [ ] Assigned to me
- [ ] Added to list/group
- [ ] Preview checked

**✅ After Import**
- [ ] Import count verified
- [ ] Spot-checked 5-10 contacts
- [ ] All data fields present
- [ ] Tag applied to all
- [ ] Segments created (Hot/Warm/Cold)
- [ ] Automated workflows activated
- [ ] First batch of calls scheduled
- [ ] Dashboard created for tracking

**✅ Ongoing**
- [ ] Update after every call
- [ ] Weekly: Review engagement
- [ ] Monthly: Data refresh from Remine
- [ ] Quarterly: Deep clean and re-score

---

## 🎓 Practice Exercise

**Your Assignment:**

**Step 1:** Export 50-100 properties from Remine (any filter strategy)

**Step 2:** Open in Excel and clean:
- Fix phone formatting
- Fix zip codes
- Remove bad data
- Add custom columns

**Step 3:** Import to Platform CRM:
- Create unique tag
- Map all fields
- Verify import successful

**Step 4:** Create 3 segments:
- Hot (top 20%)
- Warm (middle 60%)
- Cold (bottom 20%)

**Step 5:** Make 5 practice calls, update CRM after each

**Bring to class tomorrow:** Screenshot of your CRM showing imported contacts

---

## 🎯 Key Takeaways

**Data Export & CRM Integration:**

✅ **Clean data = Better results** (garbage in = garbage out)
✅ **Always tag imports** (for tracking and segmentation)
✅ **Update in real-time** (CRM only works if you use it)
✅ **Segment by priority** (not all leads are equal)
✅ **Measure everything** (what gets measured gets managed)

**Success Formula:**

```
Quality Data (from Remine)
+ Clean Import Process
+ Proper Tagging & Segmentation
+ Consistent Updates
+ Tracking & Measurement
= Predictable Results
```

---

**End of Topic 03**

**Next:** Day5_04 - UPCity Lead Generation Overview (automated inbound leads)
