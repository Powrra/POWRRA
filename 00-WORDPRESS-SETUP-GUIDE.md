# WORDPRESS SETUP GUIDE FOR POWWRA SITE

This guide will help you launch your new POWWRA website quickly using WordPress.

---

## Option 1: WordPress.com (Easiest, Fastest)

**Pros:**
- No technical setup required
- Hosting included
- Automatic updates and security
- Can be live in 1-2 hours

**Cons:**
- Monthly cost ($4-25/month depending on plan)
- Less customization on cheaper plans
- WordPress.com branding unless you upgrade

**Steps:**
1. Go to WordPress.com and create a free account
2. Choose a plan:
   - **Personal plan ($4/month)** is sufficient for a simple advocacy site
   - **Premium plan ($8/month)** if you want a custom domain (powwra.org)
3. Choose a clean, simple theme:
   - Recommended: "Seedlet," "Twenty Twenty-Four," or "Blockbase" (all free and professional)
4. Create pages using the content files I've provided (01-HOME-PAGE.md, etc.)
5. Set up navigation menu linking to your main pages

---

## Option 2: Self-Hosted WordPress (More Control)

**Pros:**
- Full control and customization
- Lower long-term cost (hosting ~$5-15/month)
- Can add any plugins you need

**Cons:**
- Requires a bit more technical setup
- You manage updates and security

**Steps:**
1. **Get hosting**: Recommended providers for non-technical users:
   - **Bluehost** ($2.95-7.99/month) – WordPress-optimized, good support
   - **SiteGround** ($3.99-14.99/month) – Fast, excellent support
   - **DreamHost** ($2.59-13.95/month) – Good for nonprofits

2. **Install WordPress**: Most hosts have 1-click WordPress installation

3. **Choose a theme**:
   - Free options: Astra, GeneratePress, Kadence
   - Premium (~$59 one-time): Divi, Avada (very flexible, drag-and-drop builders)

4. **Set up pages** (see "Creating Pages" below)

5. **Essential plugins** (all free):
   - **Contact Form 7** or **WPForms** (for contact and join forms)
   - **Yoast SEO** (helps with Google search visibility)
   - **UpdraftPlus** (automatic backups)

---

## Creating Pages in WordPress

### Step 1: Add a New Page
1. In WordPress admin, go to **Pages → Add New**
2. Enter the page title (e.g., "Home," "What's Happening to Our Water," etc.)
3. Copy the content from the corresponding .md file I created
4. Paste into the WordPress editor
5. Format headings, buttons, and links using the editor tools

### Step 2: Create Your Main Pages

Create these pages using the content files:

| WordPress Page Title | Content Source File | Set As |
|---------------------|---------------------|--------|
| Home | 01-HOME-PAGE.md | Homepage (see Settings → Reading) |
| What's Happening to Our Water? | 02-WHATS-HAPPENING.md | Regular page |
| Legal Argument & Treaty Evidence | 03-LEGAL-ARGUMENT.md | Regular page |
| Join & Donate | 04-JOIN-DONATE.md | Regular page |
| Resources | (Create later with PDF links) | Regular page |

### Step 3: Set Home Page
1. Go to **Settings → Reading**
2. Select "A static page" for homepage
3. Choose "Home" as your homepage

### Step 4: Create Navigation Menu
1. Go to **Appearance → Menus**
2. Create a new menu called "Main Menu"
3. Add these pages in this order:
   - Home
   - What's Happening to Our Water?
   - Legal Argument
   - Join & Donate
   - Resources
4. Set this menu as your "Primary Menu"

---

## Setting Up Forms (Contact & Join Form)

You'll need a plugin to create forms for the "Join & Donate" page.

### Option A: WPForms (Easiest)
1. Install **WPForms Lite** (free plugin)
2. Go to **WPForms → Add New**
3. Choose "Contact Form" template
4. Add custom fields based on the form in 04-JOIN-DONATE.md:
   - Name (text)
   - Email (email)
   - Phone (text, optional)
   - Property Address (text)
   - County (dropdown: Whatcom, etc.)
   - Water Use Type (checkboxes: Domestic well, Farm irrigation, etc.)
   - How to Help (checkboxes: Contribute, Volunteer, etc.)
   - Comments (textarea)
5. Copy the form shortcode and paste it into your "Join & Donate" page

### Option B: Contact Form 7 (More Flexible)
1. Install **Contact Form 7** plugin
2. Create a new form with custom fields
3. Requires a bit more manual setup but very powerful

---

## Adding Buttons and Call-to-Action Links

WordPress block editor makes it easy to add buttons:

1. In the editor, type `/button` and press Enter
2. Enter button text (e.g., "Am I Affected?")
3. Add link to the target page
4. Style the button (color, size) using the block settings

For the three buttons on the homepage:
- **"Am I Affected?"** → link to "What's Happening to Our Water?" page
- **"Join the Defense Fund"** → link to "Join & Donate" page
- **"Understand the Legal Argument"** → link to "Legal Argument" page

---

## Design Tips for Credibility

### Colors
Choose professional, trust-building colors:
- **Blue** (trust, stability) – good for primary color
- **Green** (land, environment) – good accent
- **Dark gray** or **navy** for text (avoid pure black)

### Typography
- Use 16-18px base font size (readable on mobile)
- Stick to 2 fonts max: one for headings, one for body text
- Recommended font pairs:
  - Headings: Montserrat or Raleway
  - Body: Open Sans or Lato

### Layout
- Keep paragraphs short (3-5 lines max)
- Use bullet points for lists
- Add white space between sections
- Make buttons prominent and action-oriented

### Mobile-Friendly
- Preview your pages on mobile before publishing
- Ensure text is readable without zooming
- Make sure buttons are easy to tap

---

## Adding PDFs for Download

You'll want to upload your existing PDF documents so visitors can download them.

1. Go to **Media → Add New**
2. Upload your PDFs (Understanding the Lawsuit, Treaty Defense Brief, etc.)
3. After upload, copy the file URL
4. In your page content, add a link:
   - Type the link text (e.g., "Download Treaty Defense Brief")
   - Highlight it and click "Insert Link"
   - Paste the PDF URL
   - (Optional) Add a 📄 emoji before the link for visual clarity

---

## Quick Launch Checklist

Before going live:

- [ ] All 4 main pages created and published
- [ ] Navigation menu working
- [ ] "Join & Donate" form set up and tested
- [ ] Contact email/form working
- [ ] PDF downloads uploaded and linked
- [ ] Mobile preview looks good
- [ ] Spell check all pages
- [ ] Legal disclaimer at bottom of key pages
- [ ] Domain name connected (if using custom domain like powwra.org)
- [ ] Site title and tagline set (Settings → General)

**Recommended site title**: "POWWRA – Property Owners Water Well Rights Advocates"

**Recommended tagline**: "Defending Water Rights in WRIA 1"

---

## Next Steps After Launch

1. **Add a Resources page** with:
   - Links to Ecology's adjudication page
   - Whatcom County WRIA resources
   - Your downloadable PDFs
   - Useful maps and timelines

2. **Create a blog/news section** (optional) for:
   - Case updates
   - Media coverage
   - Meeting announcements

3. **Set up email updates**:
   - Use a plugin like **MailPoet** or **Mailchimp for WordPress** to collect email signups and send newsletters

4. **Add social sharing**:
   - Plugin: **Social Warfare** or **AddToAny Share Buttons**
   - Makes it easy for visitors to share your content

5. **Analytics**:
   - Add Google Analytics (free) to track visitors
   - Plugin: **MonsterInsights** (easy Google Analytics setup)

---

## Need Help?

If you get stuck during setup:
- WordPress has extensive documentation at wordpress.org/support
- Most hosting providers (Bluehost, SiteGround) offer live chat support
- WordPress.com has built-in support if you go that route

---

## Cost Summary

**WordPress.com (Easiest)**
- Personal Plan: $4/month ($48/year)
- Premium Plan with custom domain: $8/month ($96/year)

**Self-Hosted WordPress**
- Hosting: $3-15/month ($36-180/year)
- Domain name (powwra.org): $12-15/year
- Premium theme (optional): $59 one-time
- **Total first year**: ~$107-254

Both options are affordable for a nonprofit advocacy site. WordPress.com Personal is the fastest path to launch if you want to go live today.

---

You now have all the content and guidance needed to launch your new POWWRA site. Let me know if you need help with any specific step!
