# HOW TO POINT YOUR DOMAIN TO NETLIFY

You need to point your domain (like powwra.org) to your Netlify site so people see your site when they visit your domain.

---

## STEP 1: Find Out Where Your Domain Is Registered

Your domain could be registered with:
- **GoDaddy** (most common)
- **Namecheap**
- **Google Domains** (now Squarespace Domains)
- **Hover**
- **Network Solutions**
- **Other registrar**

**How to find out:**
1. Go to https://lookup.icann.org
2. Enter your domain name (e.g., powwra.org)
3. Look for "Registrar" - that's who you registered with

---

## STEP 2: Add Your Domain in Netlify

1. **Go to:** https://app.netlify.com
2. **Click on your site**
3. **Click:** "Domain settings" (in the menu)
4. **Click:** "Add domain alias" or "Add custom domain"
5. **Enter:** your domain (e.g., `powwra.org`)
6. **Click:** "Add domain"

Netlify will show you what DNS records to add. **Write these down!**

You'll see something like:
```
Type: A
Name: @
Value: 75.2.60.5

Type: CNAME
Name: www
Value: yoursite.netlify.app
```

---

## STEP 3: Update DNS Settings (Where Your Domain Is Registered)

### If Your Domain Is With **GODADDY**:

1. **Go to:** https://account.godaddy.com
2. **Log in**
3. **Click:** "My Products"
4. **Find your domain** → Click "DNS"
5. **Add/Edit Records:**
   - **A Record:**
     - Type: A
     - Name: @
     - Value: `75.2.60.5` (Netlify's IP)
     - TTL: 1 Hour
   - **CNAME Record:**
     - Type: CNAME
     - Name: www
     - Value: `yoursite.netlify.app` (your Netlify URL)
     - TTL: 1 Hour
6. **Click:** "Save"

---

### If Your Domain Is With **NAMECHEAP**:

1. **Go to:** https://ap.www.namecheap.com
2. **Log in**
3. **Click:** "Domain List"
4. **Find your domain** → Click "Manage"
5. **Click:** "Advanced DNS" tab
6. **Add/Edit Records:**
   - **A Record:**
     - Type: A Record
     - Host: @
     - Value: `75.2.60.5`
     - TTL: Automatic
   - **CNAME Record:**
     - Type: CNAME Record
     - Host: www
     - Value: `yoursite.netlify.app`
     - TTL: Automatic
7. **Click:** "Save All Changes"

---

### If Your Domain Is With **GOOGLE DOMAINS** (Now Squarespace):

1. **Go to:** https://domains.google.com or https://domains.squarespace.com
2. **Log in**
3. **Click on your domain**
4. **Click:** "DNS" in the left menu
5. **Scroll to "Custom resource records"**
6. **Add Records:**
   - **A Record:**
     - Name: @
     - Type: A
     - TTL: 1h
     - Data: `75.2.60.5`
   - **CNAME Record:**
     - Name: www
     - Type: CNAME
     - TTL: 1h
     - Data: `yoursite.netlify.app`
7. **Click:** "Add"

---

## STEP 4: Wait for DNS to Propagate

**DNS changes take time to spread across the internet:**
- Minimum: 30 minutes
- Average: 2-4 hours
- Maximum: 48 hours

**To check if it's working:**
1. Go to https://dnschecker.org
2. Enter your domain name
3. Select "A" for record type
4. Click "Search"
5. If you see `75.2.60.5` appearing in green, it's working!

---

## STEP 5: Enable HTTPS in Netlify (After DNS Works)

Once your domain is pointing to Netlify:

1. **Go back to Netlify:** https://app.netlify.com
2. **Click on your site**
3. **Click:** "Domain settings"
4. **Scroll to "HTTPS"**
5. **Click:** "Verify DNS configuration"
6. **Click:** "Provision certificate"
7. **Wait 1-2 minutes** for the SSL certificate to activate

**Result:** Your site will work at `https://powwra.org` (secure!)

---

## TROUBLESHOOTING

### Problem: "Domain already registered on Netlify"
**Solution:** The domain is already claimed by another Netlify account. You need to:
1. Remove it from the old account, OR
2. Use a subdomain like `new.powwra.org`

### Problem: DNS not working after 24 hours
**Solution:**
1. Check you entered Netlify's IP correctly: `75.2.60.5`
2. Check you entered your Netlify URL correctly (ends in `.netlify.app`)
3. Make sure you saved the changes in your domain registrar
4. Contact your domain registrar support

### Problem: "www" works but main domain doesn't (or vice versa)
**Solution:** You need BOTH records:
- A record for `@` (main domain)
- CNAME record for `www` (www subdomain)

---

## WHAT IF YOU DON'T KNOW YOUR DOMAIN LOGIN?

**Option 1: Password Reset**
- Go to your domain registrar's website
- Click "Forgot Password"
- Use the email address the domain was registered with

**Option 2: Contact Registrar Support**
- Call or email your registrar (GoDaddy, Namecheap, etc.)
- Prove you own the domain (they'll ask verification questions)
- They can reset your login

**Option 3: Transfer Domain to Netlify**
- You can transfer your domain TO Netlify
- Netlify will manage it for you ($15-20/year)
- Go to Netlify → Domain settings → "Transfer your domain"

---

## SUMMARY CHECKLIST

- [ ] Upload `index.html` to Netlify (fixes 404 error)
- [ ] Find out where domain is registered (ICANN lookup)
- [ ] Add domain in Netlify (get DNS records)
- [ ] Log into domain registrar
- [ ] Add A record: `@` → `75.2.60.5`
- [ ] Add CNAME record: `www` → `yoursite.netlify.app`
- [ ] Save changes
- [ ] Wait 2-4 hours for DNS propagation
- [ ] Check with dnschecker.org
- [ ] Enable HTTPS in Netlify
- [ ] Test: visit https://powwra.org

---

## NEED HELP?

**Can't figure out where your domain is registered?**
- Email me the domain name and I can look it up

**Can't access your domain account?**
- Contact your domain registrar's support

**Domain pointing not working?**
- Send me a screenshot of your DNS settings
- I'll help troubleshoot

---

**Once your domain is pointed, people will see your new Netlify site when they visit powwra.org!** 🎉
