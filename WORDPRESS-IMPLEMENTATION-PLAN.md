# WORDPRESS IMPLEMENTATION PLAN FOR POWWRA
## Complete Step-by-Step Guide to Launch Your Site

This guide brings together everything we've created: your content strategy, donation setup, and WordPress implementation.

---

## PHASE 1: CHOOSE YOUR WORDPRESS OPTION (15 minutes)

You have two good options:

### Option A: WordPress.com (RECOMMENDED FOR YOU)

**Why this is best for you:**
- Multiple people can have login accounts (different permission levels)
- No technical maintenance (automatic updates, security, backups)
- Built-in support
- Can't break the site by accident
- Easy donation plugin installation

**Cost:**
- **Personal Plan: $4/month** ($48/year) - Good for basic site
- **Premium Plan: $8/month** ($96/year) - Better if you want custom domain immediately

**Steps:**
1. Go to WordPress.com
2. Click "Start your website"
3. Answer their questions:
   - **What kind of site?** "Blog" or "Business"
   - **Name:** POWWRA
   - **Goal:** Share information and collect donations
4. Choose **Personal** or **Premium** plan
5. You'll have a site at: `powwra.wordpress.com` (can add custom domain later)

### Option B: Self-Hosted WordPress

**Better if:**
- You want full control
- You have someone technical on your team
- You want to save money long-term

**Cost:** $5-15/month for hosting + $12/year for domain

**Best hosts for beginners:**
- **Bluehost:** $2.95-7.99/month (WordPress-optimized)
- **SiteGround:** $3.99-14.99/month (excellent support)

**I recommend WordPress.com Personal plan for you** - easier for your multi-person team.

---

## PHASE 2: INITIAL WORDPRESS SETUP (30 minutes)

Once you have WordPress running:

### Step 1: Choose a Theme

**Recommended free themes:**

1. **Kadence** (BEST FOR YOU)
   - Clean, professional
   - Great for advocacy/nonprofit sites
   - Drag-and-drop page builder included
   - Works perfectly with donation plugins

2. **Astra**
   - Very popular
   - Fast and flexible
   - Good templates

3. **Blocksy**
   - Modern
   - Easy to customize

**How to install:**
1. In WordPress admin, go to **Appearance → Themes**
2. Click **Add New**
3. Search for "Kadence"
4. Click **Install**, then **Activate**

### Step 2: Install Essential Plugins

Go to **Plugins → Add New** and install these (all FREE):

#### For Donations:
- **GiveWP** (donation management)
  - OR **WPForms Lite** (simpler, just forms)

#### For Functionality:
- **Contact Form 7** (if you don't use WPForms)
- **Yoast SEO** (helps with Google)
- **UpdraftPlus** (automatic backups)

#### Optional but Useful:
- **Elementor** (drag-and-drop page builder - if Kadence's isn't enough)

**How to install:**
1. Plugins → Add New
2. Search for plugin name
3. Click "Install Now"
4. Click "Activate"

---

## PHASE 3: CREATE YOUR PAGES (2-3 hours)

Use the content files I created. Create these pages:

### Page 1: HOME

1. **Pages → Add New**
2. **Title:** Home
3. **Copy content from:** `01-HOME-PAGE.md`
4. **Format it:**

```
[Large heading] Defending Our Wells and Property Rights in WRIA 1

[Regular text - copy the main message section]

[Add "The Core Problem" as heading, copy that section]

[Add "What's At Stake" as heading, copy that section]

[Add "Our Strategy" as heading, copy that section]

[Add 3 buttons:]
Button 1: "Am I Affected?" → Link to "What's Happening" page
Button 2: "Join the Defense Fund" → Link to "Join & Donate" page
Button 3: "Understand the Legal Argument" → Link to "Legal Argument" page
```

5. **Add a featured image** (optional):
   - Find a professional photo of Whatcom County farmland or Nooksack River
   - Free sources: Unsplash.com, Pexels.com
   - Search: "Washington farm," "well water," "rural property"

6. **Publish**

### Page 2: WHAT'S HAPPENING TO OUR WATER?

1. **Pages → Add New**
2. **Title:** What's Happening to Our Water?
3. **Copy content from:** `02-WHATS-HAPPENING.md`
4. **Structure:**

```
[Heading] What Is a Water Adjudication?
[Copy that section]

[Heading] Timeline: How We Got Here
[Format as a table or bullet list with dates]

[Heading] What Does the Summons Mean?
[Copy that section]

[Heading] The Core Legal Claims at Issue
[Copy that section - use bold for "Ecology claims:" and "POWWRA's position:"]

[Heading] What This Means for Your Well
[Copy that section]

[Heading] What Should You Do?
[Make this a numbered list]

[Heading] Key Resources
[Add these as clickable links]
```

5. **Add visual timeline** (optional - see Phase 5 for how)

6. **Publish**

### Page 3: LEGAL ARGUMENT & TREATY EVIDENCE

1. **Pages → Add New**
2. **Title:** Legal Argument & Treaty Evidence
3. **Copy content from:** `03-LEGAL-ARGUMENT.md`
4. **Structure:**

```
[Intro section - copy Overview]

[Heading] The Central Question
[Copy that section - use blockquote for the question]

[Heading] Our Legal Foundations
[Copy each numbered section with sub-headings]

[Heading] Why Jurisdiction Matters
[Copy that section - use blockquote for the key question]

[Heading] Our Litigation Strategy
[Copy as numbered list]

[Heading] Case Law & Authority
[Copy the list of cases]

[Box/Callout] Download the Full Brief
[Add download button - see Phase 4]

[Legal disclaimer at bottom]
```

5. **Formatting tips:**
   - Use headings (H2, H3) to break up sections
   - Use blockquotes for key questions and treaty text
   - Bold important phrases
   - Use bullet lists where appropriate

6. **Publish**

### Page 4: JOIN & DONATE (MOST IMPORTANT)

1. **Pages → Add New**
2. **Title:** Join & Donate
3. **Copy content from:** `04-JOIN-DONATE.md`
4. **Structure:**

```
[Heading] Join the Defense Fund

[Heading] Why We Need Your Support
[Copy that section]

[Heading] What Your Contribution Funds
[Copy as numbered list]

[Heading] How to Contribute
[Add your Stripe and Venmo buttons - see Step 5 below]

[Heading] Join POWWRA - Contact Form
[Add contact form - see Step 6 below]

[Heading] Transparency & Accountability
[Copy that section]

[Heading] Other Ways to Help
[Copy that section]
```

5. **ADD DONATION BUTTONS:**

After you set up Stripe and Venmo (following DONATION-SETUP-GUIDE.md):

**For Stripe button:**
- Add a **Button** block
- Text: "Donate with Credit/Debit Card"
- Link: Your Stripe payment link
- Style: Orange background, white text, large size
- Add text above: "For donations $25 and up - includes automatic receipt"

**For Venmo button:**
- Add another **Button** block
- Text: "Quick Donate via Venmo"
- Link: Your Venmo link (`https://venmo.com/POWWRA`)
- Style: Blue background (#3D95CE - Venmo color), white text
- Add text above: "For quick donations under $50"

**Example layout:**
```
[Heading] Contribute to the Legal Defense

[Text] We accept donations via:

[Two columns:]
┌─────────────────────────────┐  ┌─────────────────────────────┐
│ Credit/Debit Card (Stripe)  │  │ Venmo (Quick Donate)        │
│ Best for $25+               │  │ Best for under $50          │
│ Automatic receipt           │  │ Free, instant               │
│ [DONATE WITH CARD] button   │  │ [VENMO DONATE] button       │
└─────────────────────────────┘  └─────────────────────────────┘
```

6. **ADD CONTACT/JOIN FORM:**

**If using WPForms:**
1. Go to **WPForms → Add New**
2. Choose "Contact Form" template
3. Add/modify fields based on 04-JOIN-DONATE.md:
   - Name (text)
   - Email (email - required)
   - Phone (text - optional)
   - Property Address (text)
   - County (dropdown: Whatcom, Skagit, Other)
   - Type of Water Use (checkboxes):
     - Domestic well
     - Farm irrigation
     - Livestock
     - Small business
     - Other
   - How You Want to Help (checkboxes):
     - Contribute financially
     - Volunteer/organize
     - Share my story
     - Just want updates
   - Comments/Questions (textarea)
4. **Save** the form
5. **Copy the shortcode** (looks like `[wpforms id="123"]`)
6. **Paste into your Join & Donate page** under "Join POWWRA" heading

**If using Contact Form 7:**
- Similar process, but requires more manual setup
- I can provide the exact form code if needed

7. **Publish**

### Page 5: RESOURCES (Create Later)

This page will have:
- Your PDF downloads (Treaty Defense Brief, Understanding the Lawsuit, etc.)
- Links to Ecology, Whatcom County resources
- Media coverage
- Maps and documents

You can add this after the main site is live.

---

## PHASE 4: UPLOAD YOUR PDF DOCUMENTS

You have three PDFs in your Water folder:
1. Treaty Defense FALSE CLAIMS.pdf
2. Water rights Understanding the lawsuit.pdf
3. Possible summary___ For web page Printout.pdf

**How to upload and link them:**

1. **Go to:** Media → Add New
2. **Upload** each PDF
3. **After upload, click on each PDF** and copy its URL
4. **In your Legal Argument page:**
   - Add text: "Download the Full Brief"
   - Highlight it and click "Insert Link"
   - Paste the PDF URL
   - (Optional) Add a 📄 emoji before the link

**Example:**
```
📄 [Download: Treaty Defense - Why Ecology's Claims Are False (PDF)]
📄 [Download: Understanding the Water Rights Lawsuit (PDF)]
```

---

## PHASE 5: SET UP NAVIGATION MENU

1. **Go to:** Appearance → Menus
2. **Create new menu:** "Main Menu"
3. **Add pages in this order:**
   - Home
   - What's Happening to Our Water?
   - Legal Argument & Treaty Evidence
   - Join & Donate
   - Resources (when you create it)
4. **Set location:** Primary Menu (or Header Menu)
5. **Save**

---

## PHASE 6: CONFIGURE HOMEPAGE SETTINGS

1. **Go to:** Settings → Reading
2. **Select:** "A static page" (instead of blog posts)
3. **Homepage:** Choose "Home"
4. **Save**

Now when people visit your site, they see your Home page first.

---

## PHASE 7: ADD VISUAL ELEMENTS (Optional - Makes it Look Like the HTML)

The HTML file you had has nice visual elements. You can recreate some in WordPress:

### Add the 5,000 → 350 GPD Visual Impact

**Using Kadence Blocks (free):**

1. On your Home page, **add a Kadence Row Block**
2. **Set background:** Red (#E53E3E)
3. **Add white text**
4. **Create this layout:**

```
┌─────────────────────────────────────────────────┐
│         CRITICAL IMPACT (white text)            │
│                                                 │
│  ┌──────────────┐         ┌──────────────┐    │
│  │   5,000      │    →    │     350      │    │
│  │Gallons Per Day│        │Gallons Per Day│   │
│  └──────────────┘         └──────────────┘    │
│                                                 │
│  Tribal governments requesting 50% increase    │
│  in allocation - reducing property owners'     │
│  rights to provide for their claims.           │
└─────────────────────────────────────────────────┘
```

2. Use **Advanced Text** blocks with custom CSS classes for styling

### Add Timeline Visual

**Simple version** (no JavaScript needed):

Create a table or formatted list:

| Year | Event |
|------|-------|
| 2019 | Legislature directs assessment |
| 2024 | Ecology files lawsuit - 35,000 subpoenas |
| 2025 | Summons being served |
| 2026 | **Claim deadline - CRITICAL** |

**Fancy version** (with plugin):

1. Install **Timeline Express** (free plugin)
2. Create timeline entries
3. Add to your "What's Happening" page

---

## PHASE 8: FINAL TOUCHES

### Add Legal Disclaimer to Footer

1. **Go to:** Appearance → Customize → Footer
2. **Add text:**
```
Legal Disclaimer: We are not attorneys. Information provided is based
on analysis of treaties, case law, and legal documents. Property owners
should consult qualified water rights attorneys about their specific
situations.
```

### Add Contact Information

1. **Create a footer widget** with:
   - Email: contact@powwra.org (or your email)
   - (Optional) Phone number
   - Social media links if you have them

### Set Up Email Forwarding

So form submissions come to you:
1. In **WPForms**, go to form **Settings → Notifications**
2. **Send to Email Address:** Your email
3. **Subject:** "New POWWRA Contact Form Submission"

---

## PHASE 9: LAUNCH CHECKLIST

Before going public:

- [ ] All 4 main pages created and published
- [ ] Navigation menu working
- [ ] Donation buttons (Stripe + Venmo) tested
- [ ] Contact form tested (submit a test and make sure you receive it)
- [ ] PDFs uploaded and linked
- [ ] Mobile preview looks good (use WordPress preview)
- [ ] Spell-check all pages
- [ ] Legal disclaimer in footer
- [ ] Site title set: "POWWRA - Property Owners Water Well Rights Advocates"
- [ ] Tagline set: "Defending Water Rights in WRIA 1"

**To test:**
- View site on your phone
- Click every button and link
- Submit the contact form
- Try to donate (you can cancel before completing)

---

## PHASE 10: ADDING TEAM MEMBERS

Once the site is live, you can add other people:

1. **Go to:** Users → Add New
2. **Enter their:**
   - Username
   - Email
   - Name
3. **Choose role:**
   - **Administrator:** Full control (for trusted leaders)
   - **Editor:** Can edit all content but can't change settings
   - **Author:** Can only edit their own posts
4. **Send them the login info**

They can now log in at: `yoursite.com/wp-admin`

---

## PHASE 11: ONGOING UPDATES

### Adding Case Updates (Monthly)

1. **Posts → Add New** (use Posts for updates, not Pages)
2. **Title:** "Case Update: [Date]"
3. **Write the update**
4. **Publish**
5. Updates will show on a blog page

**Or** create an "Updates" page and edit it each month.

### Sending Email Updates to Donors

**Option 1: Use MailChimp** (free for up to 500 contacts)
1. Install **MailChimp for WordPress** plugin
2. Add signup form to your Join page
3. Send updates through MailChimp

**Option 2: Manual**
- Keep a spreadsheet of donor emails
- Send BCC emails with updates

---

## COST SUMMARY

**WordPress.com Personal Plan:**
- $4/month = $48/year
- **OR** WordPress.com Premium: $8/month = $96/year

**Stripe:**
- Free to set up
- 2.9% + $0.30 per donation

**Venmo:**
- FREE (personal accounts)

**Total first-year cost:** $48-96

---

## SUPPORT RESOURCES

**If you get stuck:**
- WordPress.com has built-in live chat support
- WordPress.org documentation: wordpress.org/support
- Plugin-specific help: Each plugin has its own support forum
- YouTube: Search "WordPress how to [your question]"

---

## NEXT STEPS - START HERE

1. **Go to WordPress.com** and create your account
2. **Choose Personal plan** ($4/month)
3. **Install Kadence theme**
4. **Create your Home page** using 01-HOME-PAGE.md
5. **Set up Stripe** using DONATION-SETUP-GUIDE.md
6. **Message me when you're ready** and I'll help with any specific questions

You've got all the content, all the guides, and a clear roadmap. You can do this!

---

**Questions or stuck on something?** Let me know which phase you're on and what specific issue you're facing.
