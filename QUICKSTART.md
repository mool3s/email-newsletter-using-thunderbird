# Quick Start Guide - Send Your First Newsletter in 10 Minutes

This guide will help you send your first email newsletter quickly. Follow these steps to get started right away.

## Prerequisites Check

Before starting, ensure you have:
- ✅ Thunderbird installed
- ✅ Email account configured in Thunderbird
- ✅ Mail Merge extension installed

**Don't have these?** See [Setup Guide](docs/SETUP-GUIDE.md) for installation instructions.

## Step 1: Test Your Setup (2 minutes)

1. Open Thunderbird
2. Click **"Write"** to compose a new message
3. Look for **"Mail Merge"** button in the toolbar
   - ✅ If you see it → Continue to Step 2
   - ❌ If not → Install Mail Merge extension (see [Setup Guide](docs/SETUP-GUIDE.md))

## Step 2: Prepare Test Recipients (1 minute)

For your first test, we'll send to your own email addresses.

1. Open `data/subscribers-basic.csv` in a spreadsheet program (Excel, Google Sheets, etc.)
2. Replace the sample email addresses with 2-3 of your own email addresses
3. Update the names and other details
4. Save the file

**Example:**
```csv
Email,FirstName,LastName,Company,City,State,ZIP,Address,WebsiteURL
your.email@gmail.com,Your,Name,TestCorp,YourCity,CA,12345,123 Test St,https://example.com
your.email2@yahoo.com,Test,User,TestCo,TestCity,NY,54321,456 Demo Ave,https://example.com
```

## Step 3: Open Template in Thunderbird (2 minutes)

1. Navigate to the `templates/` folder in this project
2. Open `newsletter-basic.html` in a text editor or browser
3. **Copy the entire HTML content** (Ctrl+A, Ctrl+C)
4. In Thunderbird, click **"Write"** to create a new message
5. In the compose window:
   - Click **Insert → HTML...**
   - **Paste** the template content
   - Click **Insert**

You should now see the newsletter template in the compose window.

## Step 4: Configure Mail Merge (3 minutes)

1. In the compose window, click the **"Mail Merge"** button
2. In the Mail Merge dialog:

   **Source Tab:**
   - Select **"Comma Separated (.csv)"**
   - Click **"Browse"** and select your edited `subscribers-basic.csv`
   - Click **"Preview"** to verify data loaded correctly

   **Delivery Tab:**
   - Select **"Send Later"** (recommended for first test)
   - Set delay: **3 seconds** between emails
   - Leave other options as default

3. **Subject Line:**
   - Enter: `Test Newsletter for {{FirstName}}`
   
4. **Review:**
   - Verify your CSV data appears in the preview
   - Check that the template is visible in the compose window

## Step 5: Send Test (2 minutes)

1. Click **"OK"** in the Mail Merge dialog
2. Thunderbird will queue the emails in your **Outbox**
3. To send them:
   - Go to **File → Send Unsent Messages**
   - Or wait for Thunderbird's automatic send

4. **Monitor:**
   - Check your **Sent** folder to verify emails were sent
   - Watch for the emails to arrive in your inbox

## Step 6: Verify Results (1 minute)

Check the emails you received:

- ✅ Did personalization work? (Your name appears correctly)
- ✅ Is the formatting correct?
- ✅ Do links work?
- ✅ Does it look good on mobile?

## Success! What's Next?

### Option 1: Try Different Templates

Try the other templates:
- **Promotional Newsletter:** `templates/newsletter-promotional.html` with `data/subscribers-promotional.csv`
- **Event Invitation:** `templates/newsletter-event.html` with `data/subscribers-event.csv`

### Option 2: Customize Your Template

1. Open a template in a text editor
2. Modify the content, colors, and layout
3. Test with your own data
4. See [Template Guide](docs/TEMPLATE-GUIDE.md) for customization tips

### Option 3: Send to Real Recipients

When ready to send to real recipients:

1. **Prepare Your List:**
   - Create a CSV with real subscriber data
   - Ensure all recipients have opted in
   - Verify email addresses are correct

2. **Test First:**
   - Always send a test to yourself first
   - Check all links and content
   - Verify personalization works

3. **Send in Batches:**
   - For lists over 100, send in smaller batches
   - Monitor for bounces and issues
   - Stay within your email provider's limits

4. **Monitor Results:**
   - Check bounce-back messages
   - Update list based on bounces
   - Track engagement

## Common First-Time Issues

### Mail Merge Button Missing
**Solution:** Restart Thunderbird, ensure extension is enabled in Add-ons

### Variables Not Replacing
**Solution:** Check that CSV column names exactly match template variables (case-sensitive)

### Emails Going to Spam
**Solution:** 
- Add 5-second delay between sends
- Include unsubscribe link
- Send smaller batches
- Don't use spam trigger words

### Formatting Looks Wrong
**Solution:** 
- Ensure you used "Insert → HTML" (not copy-paste into editor)
- Check that template copied completely
- Test in different email clients

## Need More Help?

- **Full Documentation:** See [docs/](docs/) folder
- **Detailed Instructions:** [Usage Guide](docs/USAGE-GUIDE.md)
- **Template Help:** [Template Guide](docs/TEMPLATE-GUIDE.md)
- **Best Practices:** [Best Practices](docs/BEST-PRACTICES.md)
- **Questions:** [FAQ](docs/FAQ.md)

## Quick Reference Card

| Task | Location |
|------|----------|
| Email templates | `templates/` folder |
| Sample data | `data/` folder |
| Full documentation | `docs/` folder |
| Installation guide | `docs/SETUP-GUIDE.md` |
| Troubleshooting | `docs/FAQ.md` |

## Tips for Success

1. **Always test first** - Send to yourself before sending to real recipients
2. **Start small** - Begin with 5-10 recipients
3. **Add delays** - Use 3-5 second delays between emails
4. **Check limits** - Know your email provider's sending limits
5. **Keep it legal** - Only email people who opted in
6. **Monitor bounces** - Remove invalid email addresses promptly
7. **Provide value** - Make every email worth opening

---

**Ready to become an email marketing pro?** Check out the [Best Practices Guide](docs/BEST-PRACTICES.md) for advanced tips!

**Having issues?** Check the [FAQ](docs/FAQ.md) for solutions to common problems.
