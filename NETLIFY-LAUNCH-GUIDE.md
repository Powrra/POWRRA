# HOW TO LAUNCH YOUR POWWRA SITE ON NETLIFY
## Complete Guide - Takes 30 Minutes

Your `index.html` file is ready to go live. Here's how to put it online for FREE.

---

## STEP 1: CREATE NETLIFY ACCOUNT (5 minutes)

1. **Go to:** https://www.netlify.com
2. **Click:** "Sign up" (top right)
3. **Choose:** Sign up with email (or GitHub/GitLab if you have it)
4. **Enter:**
   - Email address
   - Password
5. **Verify email** (check your inbox)
6. **Done!** You now have a Netlify account

**Cost:** FREE forever for your site

---

## STEP 2: PREPARE YOUR FILES (2 minutes)

1. **Find the file:** `index.html` in your `/Users/allie/projects/Water/` folder
2. **Create a new folder on your Desktop** called `powwra-site`
3. **Copy `index.html` into that folder**

**Your folder structure:**
```
powwra-site/
└── index.html
```

**That's it!** Just one file.

---

## STEP 3: DEPLOY TO NETLIFY (2 minutes)

### Option A: Drag-and-Drop (Easiest)

1. **Go to:** https://app.netlify.com/drop
2. **Drag the `powwra-site` folder** onto the page
3. **Wait 10 seconds** while it uploads
4. **DONE!** Your site is live

You'll get a URL like: `https://random-name-12345.netlify.app`

### Option B: Via Netlify Dashboard (More Control)

1. **Log into Netlify:** https://app.netlify.com
2. **Click:** "Add new site" → "Deploy manually"
3. **Drag your `powwra-site` folder** into the upload area
4. **Click:** "Deploy site"
5. **DONE!** Your site is live

---

## STEP 4: CUSTOMIZE YOUR SITE NAME (5 minutes)

Your site URL is currently something random like `random-name-12345.netlify.app`. Let's make it `powwra.netlify.app`:

1. **In Netlify dashboard,** click on your site
2. **Click:** "Site settings"
3. **Click:** "Change site name"
4. **Enter:** `powwra` (or `powwra-water-rights` if taken)
5. **Click:** "Save"

**Your new URL:** `https://powwra.netlify.app`

---

## STEP 5: SET UP STRIPE & VENMO (10 minutes)

Your site has placeholders for donation links. Let's add the real ones:

### 5A: Set Up Stripe

1. **Follow:** `DONATION-SETUP-GUIDE.md` in your Water folder
2. **Complete Stripe setup** (takes 10 minutes)
3. **Copy your Stripe payment link** - looks like:
   ```
   https://buy.stripe.com/abc123xyz
   ```

### 5B: Set Up Venmo

1. **Use your Venmo username** (e.g., `@POWWRA`)
2. **Write it down**

### 5C: Update index.html with Real Links

1. **Open `index.html`** in a text editor (TextEdit on Mac, Notepad on Windows, or VS Code)
2. **Find these lines** (near the top of the `<script>` section):
   ```javascript
   const STRIPE_LINK = "https://buy.stripe.com/YOUR-STRIPE-LINK";
   const VENMO_USERNAME = "POWWRA";
   ```
3. **Replace with your actual links:**
   ```javascript
   const STRIPE_LINK = "https://buy.stripe.com/abc123xyz"; // Your real Stripe link
   const VENMO_USERNAME = "YourActualVenmoUsername"; // Your real Venmo username
   ```
4. **Save the file**
5. **Re-upload to Netlify** (drag the folder again - it will update the site)

---

## STEP 6: CONNECT CUSTOM DOMAIN (Optional - Do Later)

If you own `powwra.org`:

1. **In Netlify dashboard:** Domain settings
2. **Click:** "Add custom domain"
3. **Enter:** `powwra.org`
4. **Follow instructions** to update your domain's DNS settings
5. **Wait 24-48 hours** for DNS to propagate

**Your site will then be at:** `https://powwra.org`

---

## STEP 7: SET UP FORM SUBMISSIONS (5 minutes)

Your contact form currently shows an alert. Let's make it actually send emails:

### Option A: Netlify Forms (Free, Easy)

1. **Open `index.html`** in text editor
2. **Find this line:**
   ```html
   <form class="space-y-4" onsubmit="handleFormSubmit(event)">
   ```
3. **Change to:**
   ```html
   <form name="contact" method="POST" data-netlify="true" class="space-y-4">
   ```
4. **Add name attributes to each input field:**
   ```html
   <input type="text" name="full_name" required ...>
   <input type="email" name="email" required ...>
   ```
5. **Save and re-upload to Netlify**

**Now form submissions go to your Netlify dashboard!**

**To get email notifications:**
1. **In Netlify:** Site settings → Forms → Form notifications
2. **Add email notification** with your email address
3. **Done!** You'll get an email every time someone submits

### Option B: Formspree (Alternative)

1. **Go to:** https://formspree.io
2. **Create free account**
3. **Create new form**
4. **Get your form endpoint**
5. **Update form action in HTML**

---

## YOUR SITE IS LIVE! 🎉

**Your URL:** `https://powwra.netlify.app` (or your custom domain)

**Share it with:**
- Property owners in WRIA 1
- County officials
- Media contacts
- Social media

---

## NEXT STEPS

1. **Test everything:**
   - Click all buttons
   - Try the donation links
   - Submit the contact form
   - View on your phone

2. **Share your URL** with your team

3. **Read the TEAM-UPDATE-GUIDE.md** so others can help update the site

---

## COSTS

**Netlify:**
- FREE for your site (no credit card needed)
- Unlimited bandwidth
- Free SSL certificate (https)
- Free site hosting

**Stripe:**
- FREE to set up
- 2.9% + $0.30 per donation

**Venmo:**
- FREE

**Total ongoing cost:** $0/month (just donation processing fees)

---

## SUPPORT

**If something goes wrong:**
- Netlify docs: https://docs.netlify.com
- Netlify support: https://www.netlify.com/support
- Netlify community forum: https://answers.netlify.com

**For quick help:**
- Most issues are solved by re-uploading your folder to Netlify
- Make sure you're uploading the FOLDER (powwra-site), not just the file

---

## QUICK REFERENCE

**Your Netlify login:** https://app.netlify.com

**To update the site:**
1. Edit `index.html`
2. Save
3. Drag `powwra-site` folder to Netlify (it will update automatically)

**Your site URLs:**
- Netlify: `https://powwra.netlify.app`
- Custom domain (if added): `https://powwra.org`

---

You did it! Your site is live and completely FREE to host. 🚀
