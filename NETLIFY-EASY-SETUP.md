# Deploy POWWRA Site to Netlify - Super Easy Guide

Choose ONE of these methods:

---

## 🚀 METHOD 1: Drag & Drop (EASIEST - No GitHub Needed!)

**Time: 2 minutes**

### Step 1: Prepare Your Files

1. Open Finder
2. Go to `/Users/allie/projects/Water`
3. Select ALL files and folders (Cmd+A)
4. **Right-click → "Compress 40 items"**
5. You'll get a file called `Archive.zip`

### Step 2: Deploy to Netlify

1. Go to: https://app.netlify.com/drop
2. **Drag the `Archive.zip` file** onto the page
3. Wait 30 seconds...
4. **Done!** Your site is live!

You'll get a URL like: `https://random-name-123.netlify.app`

### Step 3: Enable CMS (Optional)

⚠️ **PROBLEM**: The CMS won't work with drag-and-drop because it needs Git.

**Solutions:**
- **Option A**: Use Method 2 below (connect GitHub)
- **Option B**: Skip the CMS and just edit JSON files manually

---

## 🔧 METHOD 2: Connect GitHub (Full CMS Support)

**Time: 10 minutes** (requires GitHub account)

### Prerequisites
- ✅ GitHub account created
- ✅ Code uploaded to GitHub (see `GITHUB-SETUP.md`)

### Step 1: Create Netlify Account

1. Go to: https://app.netlify.com/
2. Click **"Sign up"**
3. Choose **"Sign up with GitHub"**
4. Authorize Netlify to access GitHub

### Step 2: Deploy Your Site

1. Click **"Add new site"** → **"Import an existing project"**
2. Click **"Deploy with GitHub"**
3. Click **"Configure Netlify on GitHub"**
4. Choose: **"Only select repositories"**
5. Select: `powwra-site`
6. Click **"Save"**
7. Back in Netlify, click your repository: `powwra-site`
8. **Site settings:**
   - Branch to deploy: `main` ✓
   - Build command: (leave empty)
   - Publish directory: `/` or leave empty
9. Click **"Deploy site"**

**Wait 1 minute...** ⏳

Your site is now live! You'll get a URL like:
`https://adorable-unicorn-abc123.netlify.app`

### Step 3: Make the URL Pretty (Optional)

1. Click **"Site settings"** → **"Domain management"**
2. Click **"Options"** → **"Edit site name"**
3. Change to: `powwra` (if available)
4. Now your URL is: `https://powwra.netlify.app`

### Step 4: Enable CMS Login

This lets people edit content at `yoursite.netlify.app/admin`

1. In Netlify dashboard, click **"Identity"** (top menu)
2. Click **"Enable Identity"**
3. Scroll to **"Registration preferences"**
   - Choose: **"Invite only"**
4. Scroll to **"Services"** → **"Git Gateway"**
   - Click **"Enable Git Gateway"**
5. Scroll to top, click **"Invite users"**
6. Enter email addresses of editors
7. They'll get an invite email to set up login

### Step 5: Test the CMS

1. Go to: `https://your-site.netlify.app/admin`
2. Click the invite link from email
3. Set a password
4. **You're in!** Try editing the home page:
   - Click "Pages" → "Home Page"
   - Change the hero headline
   - Click "Publish"
   - Wait 30 seconds
   - Check your live site - it updated!

---

## 🎯 METHOD 3: Super Simple (Just HTML, No CMS)

**Don't want to deal with GitHub or CMS?**

### Option A: Use Netlify Drop
1. Zip your files
2. Drag to https://app.netlify.com/drop
3. Edit JSON files manually when you need changes
4. Re-upload the zip file

### Option B: Use Free Hosting
- **Neocities**: https://neocities.org (easiest)
- **Surge.sh**: https://surge.sh (simple command)
- **Vercel**: https://vercel.com (drag & drop)

---

## Comparison Table

| Method | GitHub? | CMS? | Free? | Difficulty |
|--------|---------|------|-------|------------|
| Drag & Drop | ❌ No | ❌ No | ✅ Yes | ⭐ Easy |
| GitHub + Netlify | ✅ Yes | ✅ Yes | ✅ Yes | ⭐⭐ Medium |
| Manual JSON Editing | ❌ No | ❌ No | ✅ Yes | ⭐ Easy |

---

## My Recommendation

**If you want the CMS (so others can edit easily):**
→ Use Method 2 (GitHub + Netlify)
→ Follow `GITHUB-SETUP.md` first, then come back here

**If you're okay editing JSON files yourself:**
→ Use Method 1 (Drag & Drop)
→ Skip the CMS completely

---

## Troubleshooting

### "Build failed"
- Make sure Publish directory is `/` or empty
- Make sure Build command is empty

### "Can't access /admin"
- Did you enable Identity AND Git Gateway?
- Try logging out and back in

### "Changes don't show up"
- Wait 30-60 seconds after publishing
- Hard refresh browser: Cmd+Shift+R

---

## What's Next?

After deploying:
- [ ] Test the site: `https://your-site.netlify.app`
- [ ] Test CMS: `https://your-site.netlify.app/admin`
- [ ] Invite editors
- [ ] (Optional) Connect custom domain

**Need help? Let me know which method you chose and where you're stuck!**
