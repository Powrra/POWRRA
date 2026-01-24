# GitHub Setup for Beginners - POWWRA Site

Follow these steps **in order**. Don't skip any!

---

## ✅ STEP 1: Create GitHub Account

1. Open browser: https://github.com
2. Click **"Sign up"** (top right corner)
3. Enter your email
4. Create a password
5. Pick a username
6. Complete the puzzle
7. Check your email and verify

**✓ Done? Continue to Step 2**

---

## ✅ STEP 2: Create a New Repository

A repository = a folder on GitHub for your project

1. **Login to GitHub** (if not already)
2. **Click the green "New" button** on the left side
   - Or go directly to: https://github.com/new
3. **Fill in the form:**
   - Repository name: `powwra-site`
   - Description: `POWWRA water rights advocacy website`
   - Choose: ⚫ **Public**
   - ✅ **DO NOT** check "Add a README file"
   - ✅ **DO NOT** check "Add .gitignore"
   - ✅ **DO NOT** choose a license
4. **Click "Create repository"**

You'll see a page that says "Quick setup" at the top. **KEEP THIS PAGE OPEN!**

**✓ Done? Continue to Step 3**

---

## ✅ STEP 3: Upload Your Site to GitHub

On the GitHub page you just created, look for a section that says:
**"…or push an existing repository from the command line"**

You'll see something like:
```
git remote add origin https://github.com/YOUR-USERNAME/powwra-site.git
git branch -M main
git push -u origin main
```

**Copy YOUR version** (it will have your username in it)

---

## ✅ STEP 4: Run Commands in Terminal

Now open your **Terminal** and run these commands **one at a time**:

### Command 1: Go to your project folder
```bash
cd /Users/allie/projects/Water
```

### Command 2: Connect to GitHub
Replace `YOUR-USERNAME` with your actual GitHub username:
```bash
git remote add origin https://github.com/YOUR-USERNAME/powwra-site.git
```

Example:
```bash
git remote add origin https://github.com/allie123/powwra-site.git
```

### Command 3: Set main branch
```bash
git branch -M main
```

### Command 4: Upload files
```bash
git push -u origin main
```

**If it asks for credentials:**
- Username: (your GitHub username)
- Password: **You need a Personal Access Token** (see Step 5)

---

## ✅ STEP 5: Create GitHub Personal Access Token (if needed)

If Step 4 asked for a password and rejected your GitHub password, you need a token:

1. Go to: https://github.com/settings/tokens
2. Click **"Generate new token"** → **"Generate new token (classic)"**
3. Note: "Upload POWWRA site"
4. Expiration: Choose "No expiration"
5. Check the box: ✅ **repo** (this checks all sub-boxes)
6. Scroll down, click **"Generate token"**
7. **COPY THE TOKEN** (you can't see it again!)
8. Use this token as your "password" when running `git push`

**Alternative (easier):** Use GitHub Desktop app instead (see Step 6)

---

## ✅ STEP 6: Alternative Method - GitHub Desktop (Easier!)

If the terminal commands are confusing, use GitHub Desktop app instead:

1. **Download GitHub Desktop**: https://desktop.github.com/
2. **Install and open it**
3. **Sign in** with your GitHub account
4. **Click "Add" → "Add existing repository"**
5. **Browse to**: `/Users/allie/projects/Water`
6. **Click "Publish repository"**
7. Make sure "Keep this code private" is **UNCHECKED**
8. **Click "Publish repository"**

Done! Your code is now on GitHub.

---

## ✅ STEP 7: Verify It Worked

Go to: `https://github.com/YOUR-USERNAME/powwra-site`

You should see all your files:
- index.html
- admin/
- content/
- CMS-SETUP-GUIDE.md
- etc.

**✓ Success!** Your code is on GitHub.

---

## What's Next?

Now that your code is on GitHub, you can:

1. **Deploy to Netlify** (follow `NETLIFY-EASY-SETUP.md`)
2. Your site will be live at a free URL
3. Enable the CMS admin panel
4. Let others edit content

---

## Troubleshooting

### "git: command not found"
You need to install Git first:
```bash
xcode-select --install
```
Then try again.

### "Permission denied"
You need to set up authentication. Use GitHub Desktop instead (Step 6).

### "Repository already exists"
Run this first:
```bash
git remote remove origin
```
Then try Step 4 again.

---

**Stuck? Let me know which step you're on!**
