# TEAM UPDATE GUIDE - HOW TO UPDATE THE POWWRA WEBSITE
## For Non-Technical Team Members

This guide shows you how to update text, add case news, and keep the website current **without breaking anything**.

---

## WHO SHOULD USE THIS GUIDE?

Anyone on the POWWRA team who needs to:
- Update case information
- Add news or announcements
- Change contact information
- Update donation goals
- Fix typos

**You DO NOT need to know how to code.** Just follow these steps carefully.

---

## IMPORTANT RULES (READ FIRST!)

### ✅ SAFE TO CHANGE:
- Text inside quote marks `"like this"`
- Numbers (donation amounts, dates, etc.)
- Email addresses and contact info
- Links (URLs)

### ❌ NEVER CHANGE:
- Anything with `<` or `>` symbols (HTML tags)
- Lines that start with `//` (comments)
- Anything with `function`, `const`, `let`, `var` (code)
- Indentation (spaces/tabs)
- Curly braces `{ }` or parentheses `( )`

### 🛡️ GOLDEN RULE:
**If you're not sure, DON'T change it. Ask for help.**

---

## STEP 1: GET THE FILE (Every Time You Update)

1. **Go to Netlify:** https://app.netlify.com
2. **Log in** (use team login credentials)
3. **Click on the POWWRA site**
4. **Click:** "Deploys" tab
5. **Find the latest deploy** (top of list)
6. **Click:** The three dots (•••) → "Download deploy"
7. **Unzip the file** on your computer
8. **Find `index.html`** inside

**OR** if your team leader has set up a shared folder:
- Just open the shared `index.html` file

---

## STEP 2: OPEN THE FILE FOR EDITING

### On Mac:
1. **Right-click** `index.html`
2. **Choose:** "Open With" → "TextEdit"
3. **If it shows weird code:** TextEdit → Preferences → Open and Save → Uncheck "Display HTML files as HTML code"

### On Windows:
1. **Right-click** `index.html`
2. **Choose:** "Open With" → "Notepad"

### Best Option (All Computers):
Download **VS Code** (free): https://code.visualstudio.com
- Easier to see code
- Color-codes everything
- Shows line numbers
- Hard to accidentally break things

---

## STEP 3: FIND WHAT YOU WANT TO CHANGE

Press **Ctrl+F** (Windows) or **Cmd+F** (Mac) to search for text.

### Examples:

**Want to change "5,000 GPD"?**
- Search for: `5000` or `Gallons Per Day`

**Want to change contact email?**
- Search for: `contact@powwra.org`

**Want to update a page heading?**
- Search for the exact text you see on the website

---

## COMMON UPDATES (WITH EXAMPLES)

### Update #1: Change Contact Email

**SEARCH FOR:**
```
mailto:contact@powwra.org
```

**CHANGE TO:**
```
mailto:newemail@powwra.org
```

**Also search for:**
```
contact@powwra.org
```
(May appear in multiple places - change all of them)

---

### Update #2: Change Donation Goal/Appeal Text

**SEARCH FOR:**
```
Support POWWRA's legal challenge by contributing
```

**You'll find something like:**
```html
<p class="mb-8 text-blue-100">Support POWWRA's legal challenge by contributing to our defense fund. Every donation helps fund attorney fees, expert witnesses, and documentary research.</p>
```

**SAFE TO CHANGE:** The text between `>` and `</p>`

**EXAMPLE:**
```html
<p class="mb-8 text-blue-100">We've raised $5,000 so far! Help us reach our $25,000 goal to fund expert legal representation.</p>
```

**DON'T TOUCH:** The `<p class=...>` and `</p>` parts

---

### Update #3: Add a Case Update

**This is the MOST COMMON update you'll make.**

**SEARCH FOR:**
```
Timeline: How We Got Here
```

**You'll see a section with timeline events. To add a new update:**

**FIND THIS SECTION:**
```javascript
const events = {
    '2019': { title: "Legislative Assessment", desc: "...", icon: "fa-landmark" },
    'Jul 2024': { title: "Ecology Files Adjudication", desc: "...", icon: "fa-gavel" },
    'Early 2025': { title: "Summons Served", desc: "...", icon: "fa-file-invoice" },
    '2026': { title: "Claim Deadline", desc: "...", icon: "fa-skull-crossbones" }
};
```

**ADD A NEW LINE** (copy the format exactly):
```javascript
const events = {
    '2019': { title: "Legislative Assessment", desc: "...", icon: "fa-landmark" },
    'Jul 2024': { title: "Ecology Files Adjudication", desc: "...", icon: "fa-gavel" },
    'Early 2025': { title: "Summons Served", desc: "...", icon: "fa-file-invoice" },
    'Feb 2025': { title: "First Court Hearing", desc: "POWWRA filed motion to dismiss on jurisdictional grounds. Hearing scheduled for March 2025.", icon: "fa-gavel" },
    '2026': { title: "Claim Deadline", desc: "...", icon: "fa-skull-crossbones" }
};
```

**CRITICAL:**
- Keep the same format: `'Date': { title: "...", desc: "...", icon: "..." },`
- Don't forget the comma at the end
- Use quotes around all text
- Choose an icon from this list:
  - `fa-gavel` (court/legal)
  - `fa-file-invoice` (documents)
  - `fa-landmark` (government)
  - `fa-exclamation-triangle` (warning)
  - `fa-check-circle` (success)

---

### Update #4: Update Stripe or Venmo Links

**SEARCH FOR:**
```
const STRIPE_LINK =
```

**You'll see:**
```javascript
const STRIPE_LINK = "https://buy.stripe.com/YOUR-STRIPE-LINK";
const VENMO_USERNAME = "POWWRA";
```

**CHANGE TO YOUR REAL LINKS:**
```javascript
const STRIPE_LINK = "https://buy.stripe.com/abc123xyz";
const VENMO_USERNAME = "YourRealVenmoUsername";
```

---

### Update #5: Change Text on Home Page

**SEARCH FOR:** The exact text you want to change

**Example - Change the hero heading:**

**SEARCH FOR:**
```
Defending Our Wells and Property Rights in WRIA 1
```

**You'll find:**
```html
<h1 class="text-3xl md:text-5xl font-bold mb-6 tracking-tight">Defending Our Wells and Property Rights in WRIA 1</h1>
```

**SAFE TO CHANGE:** Text between `>` and `</h1>`

**CHANGE TO:**
```html
<h1 class="text-3xl md:text-5xl font-bold mb-6 tracking-tight">Fighting for Water Rights in Whatcom County</h1>
```

---

## STEP 4: SAVE YOUR CHANGES

1. **File → Save** (or Ctrl+S / Cmd+S)
2. **Close the editor**

---

## STEP 5: PREVIEW YOUR CHANGES (OPTIONAL BUT RECOMMENDED)

**Before uploading, check if you broke anything:**

1. **Double-click `index.html`** (it will open in your web browser)
2. **Look at the site**
3. **Does everything look right?**
   - Yes → Go to Step 6
   - No → Undo your changes (Ctrl+Z / Cmd+Z) and try again

**Common problems if something looks broken:**
- You deleted a `"` or `'` quote mark
- You deleted a `<` or `>` symbol
- You forgot a comma

**Solution:** Undo (Ctrl+Z) until it looks right again

---

## STEP 6: UPLOAD UPDATED FILE TO NETLIFY

### Method 1: Drag-and-Drop (Easiest)

1. **Put your updated `index.html`** back in the `powwra-site` folder
2. **Go to:** https://app.netlify.com
3. **Click on your site**
4. **Click:** "Deploys" tab
5. **Drag the `powwra-site` folder** onto the page (where it says "Need to update your site?")
6. **Wait 30 seconds** for it to deploy
7. **Click "Published"** when it appears
8. **Your site is updated!**

### Method 2: Manual Deploy

1. **Go to:** https://app.netlify.com
2. **Click on your site**
3. **Click:** "Deploys" tab
4. **Scroll down** to "Deploy settings"
5. **Drag your `powwra-site` folder** into the upload area
6. **Done!**

---

## STEP 7: CHECK THE LIVE SITE

1. **Go to:** `https://powwra.netlify.app` (or your custom domain)
2. **Refresh the page** (Ctrl+R or Cmd+R)
3. **Check your changes** - do they look right?

**If something is broken:**
1. **Don't panic**
2. **Go back to Netlify**
3. **Deploys tab**
4. **Find the previous working deploy**
5. **Click:** The three dots (•••) → "Publish deploy"
6. **This restores the old version** while you fix the problem

---

## EMERGENCY: "I BROKE THE SITE!"

### Step 1: Don't Panic

Netlify keeps all old versions. You can always go back.

### Step 2: Restore Previous Version

1. **Go to Netlify:** https://app.netlify.com
2. **Click on your site**
3. **Click:** "Deploys" tab
4. **Find the last working deploy** (before your changes)
5. **Click:** The three dots (•••) → "Publish deploy"
6. **Your site is back to normal**

### Step 3: Ask for Help

**Message your team leader:** "I tried to update [what you changed] and something broke. I restored the previous version. Can you help me make this change correctly?"

---

## TIPS FOR SUCCESS

### ✅ DO:
- Make one small change at a time
- Test after each change (preview in browser)
- Save the original file as backup before editing
- Use Ctrl+F / Cmd+F to find exactly what you want to change
- Ask for help if unsure

### ❌ DON'T:
- Make multiple big changes at once
- Delete entire sections without understanding them
- Change anything with `<`, `>`, `{`, `}`, `(`, `)` unless you know what it is
- Upload without previewing first
- Forget to save your changes

---

## COMMON TASKS CHEAT SHEET

| Task | Search For | What to Change |
|------|-----------|----------------|
| Update email | `contact@powwra.org` | Replace with new email |
| Change phone number | Your current phone | Replace with new number |
| Update donation text | `Support POWWRA` | Change text between `>` and `</p>` |
| Add case news | `const events = {` | Add new line following the format |
| Fix typo | The typo text | Fix it (but don't touch HTML tags) |
| Update Stripe link | `const STRIPE_LINK` | Replace URL in quotes |
| Update Venmo username | `const VENMO_USERNAME` | Replace username in quotes |

---

## WHO TO ASK FOR HELP

**For simple text changes:** [Team leader name/email]

**For broken code or technical issues:** [Technical person name/email]

**For Netlify login issues:** [Account owner name/email]

---

## UPDATING SCHEDULE

**Recommended:**
- Check for updates needed: Weekly
- Make updates: As needed
- Test the site: After every update

**Who is responsible:**
- [Person 1]: Case updates and news
- [Person 2]: Contact info and general text
- [Person 3]: Donation tracking and appeals

---

## QUICK START CHECKLIST

**Before you start:**
- [ ] Download current `index.html` from Netlify
- [ ] Make a backup copy (save as `index-backup.html`)
- [ ] Open in text editor

**While editing:**
- [ ] Search for exact text you want to change (Ctrl+F / Cmd+F)
- [ ] Only change text inside quotes or between tags
- [ ] Don't touch HTML tags `<like this>`
- [ ] Save frequently (Ctrl+S / Cmd+S)

**Before uploading:**
- [ ] Preview by double-clicking the file
- [ ] Does everything look right?
- [ ] All buttons still work?
- [ ] Text makes sense?

**After uploading:**
- [ ] Go to live site and refresh
- [ ] Check your changes
- [ ] If broken, restore previous deploy

---

## EXAMPLE: COMPLETE UPDATE PROCESS

**Task:** Update the homepage to announce we raised $10,000

**Step-by-step:**

1. **Download `index.html` from Netlify**
2. **Open in TextEdit/Notepad/VS Code**
3. **Search for:** `Support POWWRA's legal challenge`
4. **Find the line:**
   ```html
   <p class="mb-8 text-blue-100">Support POWWRA's legal challenge by contributing to our defense fund...</p>
   ```
5. **Change to:**
   ```html
   <p class="mb-8 text-blue-100">We've raised $10,000! Help us reach our $50,000 goal for expert legal representation and court costs.</p>
   ```
6. **Save the file** (Ctrl+S)
7. **Preview:** Double-click `index.html` - looks good!
8. **Upload to Netlify:** Drag `powwra-site` folder to Deploys tab
9. **Wait 30 seconds**
10. **Check live site:** https://powwra.netlify.app - looks great!
11. **Done!**

---

## REMEMBER

**You can't permanently break anything.** Netlify keeps all old versions, so you can always go back.

**When in doubt, ask.** It's better to ask than to accidentally break something.

**Start small.** Make one small change, upload, test. Then make another.

---

**You've got this! Welcome to the POWWRA web team.** 🚀
