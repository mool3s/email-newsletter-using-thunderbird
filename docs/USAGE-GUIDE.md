# Mail Merge Usage Guide

This guide walks you through the process of sending personalized email newsletters using Thunderbird and the Mail Merge extension.

## Overview

The mail merge process consists of:
1. Preparing your recipient data (CSV file)
2. Creating or customizing an HTML email template
3. Composing the email in Thunderbird
4. Running the mail merge
5. Monitoring and verifying delivery

## Step-by-Step Instructions

### Step 1: Prepare Your CSV File

Your CSV file should contain recipient information with column headers matching the variables in your template.

**Example CSV Structure:**
```csv
Email,FirstName,LastName,Company,City
john@example.com,John,Doe,TechCorp,San Francisco
jane@example.com,Jane,Smith,InnovateLab,New York
```

**Important CSV Guidelines:**
- First row MUST contain column headers
- Column headers are case-sensitive
- Use comma (,) as the delimiter
- Enclose fields with commas or special characters in quotes
- Save file as UTF-8 encoding
- Email column is mandatory

**Sample CSV Files Included:**
- `data/subscribers-basic.csv` - Basic newsletter data
- `data/subscribers-promotional.csv` - Promotional email data
- `data/subscribers-event.csv` - Event invitation data

### Step 2: Choose or Customize a Template

Select from the provided templates or create your own:

**Available Templates:**
- `templates/newsletter-basic.html` - General newsletter
- `templates/newsletter-promotional.html` - Sales and promotions
- `templates/newsletter-event.html` - Event invitations

**Template Variables:**
Variables in templates are marked with double curly braces: `{{VariableName}}`

Common variables:
- `{{Email}}` - Recipient's email address
- `{{FirstName}}` - Recipient's first name
- `{{LastName}}` - Recipient's last name
- `{{Company}}` - Company name
- `{{City}}` - City name

### Step 3: Compose Email in Thunderbird

1. **Open Thunderbird** and click "Write" to create a new message

2. **Insert Template:**
   - Click "Insert" in the menu
   - Select "HTML..." or use the Insert menu
   - Paste your HTML template content
   - Or use "Insert File" to load the HTML template

3. **Configure Basic Email Settings:**
   - **From:** Select your sending email account
   - **Subject:** Create a subject line (can include merge fields like "Hello {{FirstName}}")
   - **Body:** Your HTML template should now be visible

### Step 4: Start Mail Merge

1. **Click "Mail Merge" button** in the toolbar
   - If you don't see it, go to View → Toolbars and ensure it's enabled

2. **Configure Mail Merge Settings:**

   **Source Tab:**
   - Select "Comma Separated (.csv)"
   - Click "Browse" and select your CSV file
   - Preview the data to ensure it loaded correctly

   **Delivery Tab:**
   - Choose "Send Later" for better control (recommended)
   - Or choose "Send Now" for immediate sending
   - Set delay between emails (recommended: 2-5 seconds)
   - This helps avoid spam filters and stay within sending limits

   **Advanced Options:**
   - **Subject Line:** You can use variables here too (e.g., "Hello {{FirstName}}")
   - **Test Mode:** Check this to send only to yourself first
   - **Include Attachments:** Add any files to include

3. **Review Settings:**
   - Double-check your CSV file is correct
   - Verify template variables match CSV columns
   - Review subject line

4. **Click "OK"** to start the mail merge process

### Step 5: Monitor Sending Process

**If you selected "Send Now":**
- Thunderbird will send emails immediately
- Watch the status bar for progress
- Check Sent folder to verify

**If you selected "Send Later":**
- Emails are queued in the Outbox
- Click "Send Unsent Messages" when ready
- Or wait for Thunderbird's scheduled send time
- Monitor progress in the Activity Manager (Tools → Activity Manager)

### Step 6: Verify Delivery

1. **Check Sent Folder:**
   - Verify emails appear in your Sent folder
   - Each email should show individual recipient

2. **Test Email Receipt:**
   - Send test emails to yourself first
   - Check different email clients (Gmail, Outlook, etc.)
   - Verify formatting and personalization

3. **Monitor Bounces:**
   - Watch for bounce-back messages
   - Update your CSV to remove invalid addresses
   - Keep track of delivery failures

## Advanced Features

### Using Conditional Content

While Mail Merge doesn't support conditional logic directly, you can:
- Create separate CSV files for different segments
- Use different templates for different audiences
- Pre-process your CSV with scripts to add custom content

### Attachments

To include attachments in your mail merge:
1. Attach files to your compose window before starting mail merge
2. All recipients will receive the same attachments
3. Be mindful of total email size

### HTML Email Best Practices

- **Keep it simple:** Use table-based layouts for better compatibility
- **Inline CSS:** Use inline styles instead of external stylesheets
- **Test thoroughly:** Preview in multiple email clients
- **Alt text:** Always include alt text for images
- **Plain text version:** Consider including a plain text alternative

### Subject Line Personalization

Make your subject lines more engaging:
- `Hello {{FirstName}}, Check out our new products!`
- `{{FirstName}}, exclusive offer for {{City}} residents`
- `Your invitation to {{EventName}}`

## Common Workflows

### Workflow 1: Monthly Newsletter
1. Update subscribers-basic.csv with current subscriber list
2. Open newsletter-basic.html template
3. Update content for current month
4. Send test to yourself
5. Run mail merge to full list

### Workflow 2: Promotional Campaign
1. Prepare subscribers-promotional.csv with promo codes
2. Customize newsletter-promotional.html
3. Test with small segment
4. Schedule sending during optimal hours
5. Monitor response rates

### Workflow 3: Event Invitations
1. Create event-specific CSV with RSVP details
2. Customize newsletter-event.html with event details
3. Send to segmented list
4. Track RSVPs
5. Send reminder emails to non-responders

## Tips for Success

1. **Always test first** with your own email addresses
2. **Send in batches** if you have a large list (500+ recipients)
3. **Respect time zones** when scheduling sends
4. **Monitor open rates** to optimize send times
5. **Keep lists clean** by removing bounced emails
6. **Include unsubscribe link** to comply with regulations
7. **Track engagement** to improve future campaigns
8. **A/B test** subject lines and content with small segments

## Troubleshooting

### Variables Not Replacing
- Check CSV column headers match template exactly
- Ensure variable syntax is {{VariableName}}
- Verify CSV file encoding is UTF-8

### Emails Going to Spam
- Add delay between sends (3-5 seconds)
- Ensure SPF/DKIM records are configured
- Avoid spam trigger words
- Include plain text version
- Keep clean sender reputation

### Formatting Issues
- Use inline CSS instead of CSS in &lt;style&gt; tags
- Test in multiple email clients
- Avoid advanced CSS features
- Use HTML tables for layout

### Slow Sending
- Reduce email size (optimize images)
- Increase delay between sends
- Send in smaller batches
- Check internet connection speed

## Next Steps

- Review [Template Guide](TEMPLATE-GUIDE.md) to create custom templates
- Read [Best Practices](BEST-PRACTICES.md) for email marketing tips
- Check [FAQ](FAQ.md) for common questions
