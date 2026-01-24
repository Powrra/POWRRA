# HOW TO POINT POWWRA.ORG FROM MASTERMIND TO NETLIFY

Your domain `powwra.org` is currently hosted with Mastermind. Here's how to point it to your new Netlify site.

---

## WHAT YOU NEED TO DO

You need to update your DNS records at Mastermind to point to Netlify:

**DNS Records to Add:**
```
Type: A
Name: @
Value: 75.2.60.5

Type: CNAME
Name: www
Value: powwra.netlify.app
```

---

## STEP 1: Log Into Mastermind

**Mastermind** is a web hosting company - you should have login credentials from them.

1. **Go to:** Your Mastermind control panel
   - This is usually something like:
   - `https://yourdomain.mastermindhosting.com`
   - OR check your email for "Mastermind" to find the login link

2. **Log in** with your username and password

3. **If you don't know your login:**
   - Check your email for "Mastermind" or "powwra.org"
   - Look for account setup or welcome emails
   - Contact Mastermind support: support@mastermindhosting.com

---

## STEP 2: Find the DNS Management Section

Mastermind uses **cPanel** or a similar control panel. Look for:

- **"DNS Zone Editor"**
- **"DNS Management"**
- **"Domain Management"**
- **"Advanced DNS"**

The exact name depends on their control panel.

---

## STEP 3: Update DNS Records

### A Record (for main domain):

1. **Find existing A record** for `@` or `powwra.org`
2. **Click "Edit"** (or delete the old one and add new)
3. **Set:**
   - Type: `A`
   - Name: `@` (or leave blank, or `powwra.org`)
   - Value/Points to: `75.2.60.5`
   - TTL: `3600` (or 1 hour, or automatic)
4. **Click "Save"**

### CNAME Record (for www):

1. **Find existing CNAME record** for `www`
2. **Click "Edit"** (or delete old and add new)
3. **Set:**
   - Type: `CNAME`
   - Name: `www`
   - Value/Points to: `powwra.netlify.app`
   - TTL: `3600` (or 1 hour, or automatic)
4. **Click "Save"**

---

## STEP 4: Delete Old Records (If Needed)

If you see other A records or CNAME records pointing elsewhere, you may need to delete them:

- **Old A records** pointing to Mastermind's IP
- **Old CNAME records** for `www` pointing to Mastermind

**Keep these if you see them:**
- MX records (for email)
- TXT records (for verification)
- NS records (nameservers)

---

## STEP 5: Wait for DNS to Propagate

DNS changes take time:
- **Minimum:** 30 minutes
- **Average:** 2-4 hours
- **Maximum:** 48 hours

**Check if it's working:**
1. Go to https://dnschecker.org
2. Type: `powwra.org`
3. Select: `A` record type
4. Click "Search"
5. Look for `75.2.60.5` appearing worldwide (green checkmarks)

**Also check www:**
1. Type: `www.powwra.org`
2. Select: `CNAME` record type
3. Look for `powwra.netlify.app`

---

## STEP 6: Enable HTTPS in Netlify (After DNS Works)

Once DNS is propagated (you see the records at dnschecker.org):

1. **Go to:** https://app.netlify.com
2. **Click on your site**
3. **Click:** "Domain settings"
4. **Scroll to "HTTPS"**
5. **Click:** "Verify DNS configuration"
6. **Click:** "Provision certificate"
7. **Wait 1-2 minutes** for SSL to activate

**Result:** Your site works at `https://powwra.org` (secure!)

---

## TROUBLESHOOTING

### Problem: Can't find Mastermind login

**Solution:**
1. Check your email for "Mastermind" keywords
2. Look for emails from:
   - support@mastermindhosting.com
   - noreply@mastermindhosting.com
   - Or any email with "Mastermind" in it
3. Contact Mastermind support directly

### Problem: Don't have access to Mastermind account

**Solution:**
1. **Who set up the website originally?** They might have the login
2. **Contact Mastermind support:** Tell them you need access to DNS for powwra.org
3. They'll verify you own the domain (may ask for email proof or other verification)

### Problem: Mastermind won't let me change DNS

**Option 1: Transfer domain away from Mastermind**
1. Unlock the domain at Mastermind
2. Get an authorization code from Mastermind
3. Transfer to Netlify (or another registrar like Namecheap)
4. Takes 5-7 days

**Option 2: Cancel Mastermind hosting, keep domain elsewhere**
- If Mastermind is also your domain registrar, you can:
  - Cancel the hosting part (the old website)
  - Keep the domain registration active
  - Update DNS to point to Netlify

### Problem: Website still shows old Mastermind site

**Solution:**
1. Clear your browser cache (Ctrl+Shift+Delete or Cmd+Shift+Delete)
2. Try in incognito/private browsing mode
3. Try on a different device or mobile phone
4. Check dnschecker.org to see if DNS has fully propagated

---

## IMPORTANT NOTES

### About Email:
If you have email addresses at powwra.org (like contact@powwra.org), **be careful:**
- Moving DNS might affect email
- Make sure MX records (email records) stay pointing to wherever your email is hosted
- If email is at Mastermind, you may need to keep those MX records

### About Mastermind Hosting:
- You can cancel Mastermind hosting **after** DNS is working and pointing to Netlify
- Don't cancel it before DNS is updated, or your site will go down
- If Mastermind is also your domain registrar, you still need to keep paying them for the domain (or transfer it elsewhere)

---

## STEP-BY-STEP SUMMARY

**✅ CHECKLIST:**

- [ ] Upload `index.html` to Netlify (so site is ready when DNS points)
- [ ] Log into Mastermind control panel
- [ ] Find DNS Zone Editor or DNS Management
- [ ] Edit A record: `@` → `75.2.60.5`
- [ ] Edit CNAME record: `www` → `powwra.netlify.app`
- [ ] Save changes
- [ ] Wait 2-4 hours for DNS to propagate
- [ ] Check dnschecker.org to verify
- [ ] Enable HTTPS in Netlify
- [ ] Test: visit https://powwra.org
- [ ] Site works! 🎉

---

## ALTERNATIVE: HAVE MASTERMIND DO IT FOR YOU

If this is too complicated, you can contact Mastermind support and ask them to do it:

**Email template:**

```
Subject: DNS Update Request for powwra.org

Hi Mastermind Support,

I need to update the DNS records for my domain powwra.org to point to a new host.

Please update the following DNS records:

A Record:
- Name: @ (or powwra.org)
- Value: 75.2.60.5

CNAME Record:
- Name: www
- Value: powwra.netlify.app

Please keep all existing MX records (email) unchanged.

My account email is: [your email]
Domain: powwra.org

Thank you!
```

They should be able to do this for you within 1-2 business days.

---

## NEED HELP?

**Stuck at any step?**
1. Take a screenshot of what you're seeing in Mastermind
2. Let me know which step you're stuck on
3. I'll guide you through it

**Can't access Mastermind?**
- Let me know and I'll help you figure out who has access or how to recover it

---

**Once DNS is updated, powwra.org will show your new Netlify site!** 🚀
