# Thunderbird Mail Merge Setup Guide

## Prerequisites

Before you begin, ensure you have:
- Mozilla Thunderbird email client installed
- Mail Merge extension for Thunderbird
- Your email account configured in Thunderbird
- Basic understanding of HTML and email marketing

## Step 1: Install Thunderbird

1. Download Thunderbird from [Mozilla's official website](https://www.thunderbird.net/)
2. Install Thunderbird following the installation wizard
3. Launch Thunderbird and configure your email account

### Email Account Configuration
- Click on "Set up an account" in Thunderbird
- Select "Email" and enter your details:
  - Your name
  - Email address
  - Password
- Thunderbird will auto-configure settings for most popular providers
- Complete the setup process

## Step 2: Install Mail Merge Extension

### Method 1: From Thunderbird Add-ons Manager
1. Open Thunderbird
2. Click on the menu (≡) in the top-right corner
3. Select "Add-ons and Themes"
4. Search for "Mail Merge"
5. Click "Add to Thunderbird" on the Mail Merge extension
6. Restart Thunderbird if prompted

### Method 2: Manual Installation
1. Download the Mail Merge XPI file from [Thunderbird Add-ons](https://addons.thunderbird.net/)
2. In Thunderbird, go to Tools → Add-ons
3. Click the gear icon and select "Install Add-on From File"
4. Navigate to the downloaded XPI file and select it
5. Restart Thunderbird

## Step 3: Verify Installation

After installation:
1. Open Thunderbird
2. Click "Write" to compose a new message
3. Look for "Mail Merge" button in the toolbar
4. If you see it, the extension is successfully installed

## Step 4: Configure SMTP Settings

For sending bulk emails, ensure your SMTP settings are properly configured:

1. Go to Account Settings (Edit → Account Settings or Tools → Account Settings)
2. Select "Outgoing Server (SMTP)" in the left sidebar
3. Verify your SMTP server settings:
   - Server Name: Your email provider's SMTP server
   - Port: Usually 587 (TLS) or 465 (SSL)
   - Connection security: STARTTLS or SSL/TLS
   - Authentication method: Normal password
   - Username: Your email address

### Important SMTP Considerations
- **Sending Limits**: Check your email provider's sending limits
- **Gmail**: 500 emails/day for regular accounts, 2000/day for Google Workspace
- **Outlook/Microsoft 365**: 300 emails/day for regular accounts
- **Custom SMTP**: Check with your provider for limits

## Step 5: Test Configuration

Before sending to your full list:
1. Create a test CSV with 2-3 email addresses (your own email addresses)
2. Use one of the provided templates
3. Perform a test mail merge
4. Verify all emails are received correctly
5. Check formatting, links, and personalization

## Troubleshooting

### Mail Merge Button Not Visible
- Ensure the extension is enabled in Add-ons manager
- Try restarting Thunderbird
- Check if you're in a new message window (not reading pane)

### Emails Not Sending
- Verify SMTP settings are correct
- Check internet connection
- Ensure you haven't exceeded sending limits
- Check if your account requires an app-specific password

### Formatting Issues
- Ensure HTML template is valid
- Test email rendering in multiple email clients
- Use inline CSS instead of external stylesheets
- Avoid JavaScript (most email clients block it)

### Merge Fields Not Working
- Verify CSV column headers match template variables exactly
- Ensure CSV file uses UTF-8 encoding
- Check for extra spaces in column headers
- Make sure template variables are enclosed in {{}}

## Security Best Practices

1. **Never include sensitive data** in CSV files that aren't encrypted
2. **Use BCC for privacy**: Configure Mail Merge to use BCC when appropriate
3. **Keep software updated**: Regularly update Thunderbird and extensions
4. **Secure your CSV files**: Store them in encrypted folders
5. **Test with small batches**: Always test before sending to full list
6. **Include unsubscribe links**: Comply with email marketing regulations

## Next Steps

Once setup is complete, proceed to:
- [Usage Guide](USAGE-GUIDE.md) - Learn how to create and send newsletters
- [Template Guide](TEMPLATE-GUIDE.md) - Customize email templates
- [Best Practices](BEST-PRACTICES.md) - Email marketing tips and guidelines
