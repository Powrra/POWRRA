# Static CMS Setup Guide for POWWRA Site

You now have Decap CMS (formerly Netlify CMS) installed. This lets non-technical users edit website content through a user-friendly interface at `yoursite.com/admin`.

## What Was Added

1. **Content Files** (`/content` folder)
   - `site-settings.json` - Organization info, contact details, donation links
   - `home-page.json` - All home page content (editable sections)
   - `timeline-page.json` - Events, meetings, deadline info

2. **Admin Interface** (`/admin` folder)
   - `index.html` - The CMS login page
   - `config.yml` - Configuration for what content can be edited

## Quick Start: Deploy to Netlify (Free)

### Step 1: Create GitHub Repository

```bash
cd /Users/allie/projects/Water
git init
git add .
git commit -m "Initial POWWRA site with CMS"
```

Then create a repo on GitHub and push:
```bash
git remote add origin https://github.com/YOUR-USERNAME/powwra-site.git
git branch -M main
git push -u origin main
```

### Step 2: Deploy to Netlify

1. Go to https://app.netlify.com/
2. Click "Add new site" → "Import an existing project"
3. Choose GitHub and select your repository
4. Build settings:
   - Build command: (leave empty)
   - Publish directory: `/`
5. Click "Deploy site"

### Step 3: Enable Netlify Identity (for CMS login)

1. In Netlify dashboard, go to **Site settings → Identity**
2. Click "Enable Identity"
3. Under **Registration preferences**, select "Invite only"
4. Under **External providers**, enable GitHub or Google (optional)
5. Under **Services → Git Gateway**, click "Enable Git Gateway"

### Step 4: Invite Users

1. Go to **Identity** tab in Netlify
2. Click "Invite users"
3. Enter email addresses of people who should edit the site
4. They'll receive an invite link to set up their login

### Step 5: Access the CMS

Once deployed, anyone with an account can go to:
```
https://your-site-name.netlify.app/admin
```

They'll see a login screen, and after logging in can edit:
- Organization settings (contact info, donation links)
- Home page content (hero text, core problem, impact numbers)
- Events and meetings

## How Editing Works

1. User logs in at `/admin`
2. Chooses what to edit (e.g., "Home Page")
3. Edits content in a visual editor
4. Clicks "Publish"
5. Changes are automatically saved to GitHub
6. Netlify auto-deploys the updated site (30 seconds)

## What They Can Edit

### Site Settings
- Organization name, address, contact email
- Social media links
- Stripe and Venmo donation links

### Home Page
- Hero headline and description
- Core problem statements
- Impact numbers (5,000 → 350 gallons)
- What's at stake cards
- Strategy steps

### Timeline/Events Page
- Deadline date and warning text
- Upcoming events and meetings
- Event details (date, time, venue, description)

## Important Notes

- **They CANNOT break the site** - the CMS only allows editing content, not code
- **Changes are versioned** - you can revert to any previous version via GitHub
- **Images**: Users can upload images through the CMS (stored in `/images`)
- **No coding required** - the interface is like editing a Word document

## Alternative: Use Decap CMS Locally (Testing)

To test the CMS before deploying:

1. Install Node.js if not already installed
2. Run a local server:
```bash
cd /Users/allie/projects/Water
npx decap-server
```

3. In another terminal:
```bash
npx http-server -p 8080
```

4. Open http://localhost:8080/admin/
5. You can now test editing without deploying

## Need More Editable Sections?

To add more editable content:

1. Create a new JSON file in `/content`
2. Edit `/admin/config.yml` to add the new content type
3. Update `index.html` to load from the new JSON file

## Troubleshooting

**"Can't access /admin"**
- Make sure you've enabled Netlify Identity and Git Gateway

**"Changes not showing"**
- Check Netlify deploy log to see if build succeeded
- Hard refresh browser (Cmd+Shift+R)

**"Login not working"**
- User must accept invite email from Netlify
- Check spam folder for invite

## Cost

- **Netlify hosting**: Free (up to 100GB bandwidth/month)
- **Decap CMS**: Free and open source
- **Total**: $0/month

## Support

For help with:
- Netlify setup: https://docs.netlify.com/
- Decap CMS: https://decapcms.org/docs/
- This specific setup: Contact the developer who set this up

---

**Next Step**: Follow "Step 1: Create GitHub Repository" above to get started!
