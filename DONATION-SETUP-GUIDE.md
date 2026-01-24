# STRIPE + VENMO DONATION SETUP GUIDE

Complete step-by-step instructions for setting up both donation methods for POWWRA.

---

## PART 1: STRIPE SETUP (15 minutes)

Stripe is perfect for formal donations - professional, sends receipts, accepts all credit/debit cards.

### Step 1: Create Stripe Account

1. **Go to:** https://stripe.com
2. **Click:** "Start now" (top right)
3. **Enter:**
   - Email address
   - Password
   - Country: United States
4. **Click:** "Create account"

### Step 2: Complete Business Profile

Stripe will ask for:
- **Business name:** Property Owners Water Well Rights Advocates (or POWWRA)
- **Business type:**
  - If you're a registered nonprofit (501c3/501c4): Select "Nonprofit"
  - If you're an unincorporated association: Select "Individual/Sole proprietor"
- **Tax ID:**
  - If you have an EIN: Enter it
  - If not: Can use SSN for now (can update later)
- **Bank account:** Where donation money will be deposited
  - Routing number
  - Account number

**Note:** You can start without completing everything - Stripe lets you create payment links before full verification.

### Step 3: Create Payment Link for Donations

1. **In Stripe Dashboard, go to:** "Payment Links" (left sidebar)
2. **Click:** "New payment link"
3. **Configure:**

   **Product name:** Legal Defense Fund Contribution

   **Amount:** Select "Customer chooses amount"
   - Set minimum: $10 (or $5, your choice)
   - Add suggested amounts: $25, $50, $100, $250, $500

   **Description (optional):**
   ```
   Support POWWRA's legal defense against the WRIA 1 water rights
   adjudication. Funds support attorney fees, expert witnesses, and
   documentary research.
   ```

   **After payment:**
   - Select "Show confirmation page"
   - Add custom message:
     ```
     Thank you for supporting POWWRA! We'll send you email updates
     on the case. For questions, contact [your email].
     ```

4. **Click:** "Create link"

5. **Copy the link** - looks like:
   ```
   https://buy.stripe.com/abc123xyz
   ```

### Step 4: Get Your Donation Link

**Your Stripe donation link is now ready!**

Example: `https://buy.stripe.com/test_abc123xyz`

You can:
- Share this link directly
- Add it as a button on your website
- Put it in emails and social media

**Fees:** 2.9% + $0.30 per donation
**Example:** $100 donation = you receive $96.80

---

## PART 2: VENMO SETUP (2 minutes)

Venmo is perfect for quick, casual donations from local supporters.

### Step 1: Set Up Venmo Account

**If you already have Venmo:**
- Just decide which account to use (personal or create a new one for POWWRA)

**If you need to create one:**
1. Download Venmo app (iPhone/Android)
2. Sign up with email
3. Choose username: **@POWWRA** (or @POWWRAorg if taken)
4. Link to your bank account

### Step 2: Get Your Venmo Link

Your Venmo donation link is simply:
```
https://venmo.com/POWWRA
```
(Replace POWWRA with your actual username)

**Or use a QR code:**
- In Venmo app, go to your profile
- Tap the QR code icon
- Screenshot it
- Add to your website/flyers

**Note:** Venmo is FREE for personal accounts (no fees on donations)

---

## PART 3: ADD TO YOUR WEBSITE

Now you have:
- ✅ Stripe link: `https://buy.stripe.com/abc123xyz`
- ✅ Venmo link: `https://venmo.com/POWWRA`

### Option A: For the HTML File

I'll update the HTML file to include both buttons with your actual links.

### Option B: For WordPress

1. **Edit the "Join & Donate" page**
2. **Add a button block:**
   - Click "+" to add block
   - Search for "Button"
   - Enter text: "Donate via Stripe"
   - Add your Stripe link
   - Style: Orange background, white text

3. **Add second button for Venmo:**
   - Same process
   - Text: "Quick Donate via Venmo"
   - Add your Venmo link
   - Style: Blue background (Venmo color)

---

## PART 4: BEST PRACTICES

### Donation Page Layout

**Recommended structure:**

```
[Heading] Support the Legal Defense

[Text] Your contribution helps fund:
• Expert water rights attorneys
• Federal Indian law specialists
• Expert witnesses and research
• Court filing fees and discovery costs

[Two buttons side by side:]
[Donate with Card (Stripe)] [Quick Venmo Donation]

[Text] All donations go directly to legal defense costs.
We provide regular updates to contributors.
```

### Transparency

**On your donation page, include:**

1. **What funds are used for:**
   - Attorney retainer fees
   - Expert witness costs
   - Documentary research
   - Court filing fees

2. **Organizational status:**
   - If you're a registered nonprofit: "POWWRA is a 501(c)(4) nonprofit"
   - If not: "POWWRA is an unincorporated association of property owners"

3. **Tax deductibility:**
   - If 501(c)(3): "Donations are tax-deductible"
   - If 501(c)(4) or informal: "Donations are not tax-deductible"
   - If unsure: "Please consult your tax advisor"

4. **Updates:**
   - "Contributors receive regular email updates on the case"

### Email Confirmation

**After someone donates, send them:**

Subject: Thank you for supporting POWWRA

```
Dear [Name],

Thank you for your contribution of $[amount] to the Property Owners
Water Well Rights Advocates legal defense fund.

Your support helps us fight the WRIA 1 water rights adjudication and
defend property owners' constitutional rights.

What happens next:
• We'll add you to our email update list
• You'll receive monthly case updates
• We'll notify you of important deadlines and developments

How your donation helps:
• Retaining experienced water rights and federal Indian law attorneys
• Funding expert witnesses and technical analysis
• Obtaining historical documents and legal research
• Filing motions and defending property owners in court

Questions? Reply to this email or contact [phone/email].

With gratitude,
POWWRA Leadership Team

---
Tax information: [Your 501(c) status and tax deductibility info]
```

---

## PAYMENT COMPARISON

| Feature | Stripe | Venmo |
|---------|--------|-------|
| **Best for** | Formal donations $50+ | Quick donations $10-50 |
| **Fees** | 2.9% + $0.30 | FREE (personal accounts) |
| **Payment types** | All credit/debit cards | Bank transfer, debit card |
| **Receipt** | Automatic email | Venmo transaction record |
| **Professional** | ✅ Very | ⚠️ Casual |
| **Tax receipt** | ✅ Can provide | ⚠️ Manual |
| **Donor info** | ✅ Full details | ⚠️ Limited |

**Strategy:**
- Promote **Stripe** for larger, serious contributions
- Offer **Venmo** as a quick, easy option for smaller amounts

---

## NEXT STEP

**Send me your actual links once you have them:**

1. Your Stripe payment link: `https://buy.stripe.com/___________`
2. Your Venmo username: `@___________`

**Then I'll:**
- Add professional donation buttons to your website
- Include both options with clear descriptions
- Add the transparency language
- Make it ready to accept donations immediately

---

## LEGAL REMINDER

**Before accepting donations, confirm:**

1. **Organizational structure** - Are you:
   - A registered nonprofit (501c3, 501c4)?
   - An unincorporated association?
   - Informal group?

2. **Tax status** - This affects:
   - Whether donations are tax-deductible
   - What you tell donors
   - Your reporting requirements

3. **Bank account** - Is it:
   - In POWWRA's name?
   - A personal account designated for this use?

**Recommendation:** Consult with an accountant or attorney about your organizational structure before raising significant funds. This protects you legally and gives donors clarity.

---

You're ready to set up both donation methods! Let me know when you have the links and I'll integrate them into your site.
