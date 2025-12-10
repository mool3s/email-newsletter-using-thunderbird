# HTML Email Template Guide

This guide explains how to create and customize HTML email templates for use with Thunderbird Mail Merge.

## Template Structure

### Basic Template Anatomy

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Email Title</title>
    <style>
        /* Inline styles preferred */
    </style>
</head>
<body>
    <div class="container">
        <!-- Email content -->
    </div>
</body>
</html>
```

## Merge Variables

### Syntax
Variables use double curly braces: `{{VariableName}}`

### Common Variables
- `{{Email}}` - Recipient's email
- `{{FirstName}}` - First name
- `{{LastName}}` - Last name
- `{{Company}}` - Company name
- `{{City}}` - City
- `{{State}}` - State/Province
- `{{ZIP}}` - Postal code
- `{{Phone}}` - Phone number
- `{{WebsiteURL}}` - Website URL

### Custom Variables
You can create any custom variable:
1. Add a column to your CSV file
2. Use the column header name in your template
3. Example: CSV has `FavoriteColor` → Template uses `{{FavoriteColor}}`

### Using Variables in Different Contexts

**In HTML Content:**
```html
<p>Hello {{FirstName}},</p>
<p>Welcome to {{City}}!</p>
```

**In Links:**
```html
<a href="{{WebsiteURL}}">Visit our website</a>
<a href="mailto:{{Email}}">Contact {{FirstName}}</a>
```

**In Attributes:**
```html
<img src="https://example.com/city/{{City}}.jpg" alt="{{City}}">
```

**In Subject Lines:**
```
Subject: Hello {{FirstName}}, special offer for {{City}}!
```

## Email HTML Best Practices

### 1. Use Table-Based Layouts

Many email clients don't support modern CSS layouts:

```html
<table width="600" border="0" cellpadding="0" cellspacing="0">
    <tr>
        <td>
            <!-- Content here -->
        </td>
    </tr>
</table>
```

### 2. Inline CSS

Always use inline styles for maximum compatibility:

```html
<!-- Good -->
<p style="color: #333; font-size: 16px;">Text</p>

<!-- Avoid (may not work in all clients) -->
<style>
    p { color: #333; }
</style>
<p>Text</p>
```

### 3. Fixed Width

Set a fixed width (typically 600px) for better control:

```html
<div style="max-width: 600px; margin: 0 auto;">
    <!-- Content -->
</div>
```

### 4. Safe Web Fonts

Stick to web-safe fonts:
- Arial, Helvetica, sans-serif
- Georgia, Times New Roman, serif
- Courier New, monospace
- Verdana, sans-serif

### 5. Color Codes

Use full hex codes:
```html
<!-- Good -->
<div style="background-color: #3498db;">

<!-- Avoid -->
<div style="background-color: #39d;">
```

### 6. Images

**Hosting:**
- Host images on a reliable server (not local files)
- Use absolute URLs
- Consider using a CDN

**Optimization:**
- Compress images to reduce email size
- Use appropriate formats (JPEG for photos, PNG for graphics)
- Maximum width: 600px

**Alt Text:**
```html
<img src="https://example.com/logo.png" 
     alt="Company Logo" 
     width="200" 
     height="100" 
     style="display: block;">
```

## Template Components

### Header Section

```html
<div style="background-color: #2c3e50; color: #ffffff; padding: 30px; text-align: center;">
    <h1 style="margin: 0; font-size: 28px;">{{Company}}</h1>
    <p style="margin: 10px 0 0 0;">Newsletter Title</p>
</div>
```

### Content Section

```html
<div style="padding: 30px 20px; background-color: #ffffff;">
    <p style="font-size: 18px; margin-bottom: 20px;">
        Dear {{FirstName}} {{LastName}},
    </p>
    <p style="line-height: 1.6; color: #333;">
        Your content here...
    </p>
</div>
```

### Button/CTA

```html
<table width="100%" border="0" cellpadding="0" cellspacing="0">
    <tr>
        <td align="center" style="padding: 20px 0;">
            <a href="{{WebsiteURL}}" 
               style="display: inline-block; padding: 15px 40px; background-color: #3498db; 
                      color: #ffffff; text-decoration: none; border-radius: 5px; 
                      font-weight: bold;">
                Click Here
            </a>
        </td>
    </tr>
</table>
```

### Footer Section

```html
<div style="background-color: #ecf0f1; padding: 20px; text-align: center; 
            font-size: 12px; color: #7f8c8d;">
    <p style="margin: 5px 0;">{{Company}}</p>
    <p style="margin: 5px 0;">{{Address}}, {{City}}, {{State}} {{ZIP}}</p>
    <p style="margin: 5px 0;">
        <a href="mailto:{{Email}}" style="color: #3498db; text-decoration: none;">
            Contact Us
        </a> | 
        <a href="#" style="color: #3498db; text-decoration: none;">
            Unsubscribe
        </a>
    </p>
</div>
```

## Responsive Design

### Media Queries

Email client support varies, but you can include basic responsive styles:

```html
<style>
    @media only screen and (max-width: 600px) {
        .container {
            width: 100% !important;
        }
        .mobile-padding {
            padding: 10px !important;
        }
    }
</style>
```

### Mobile-Friendly Tips
- Use larger font sizes (minimum 14px)
- Make buttons touch-friendly (minimum 44px height)
- Use single-column layouts
- Increase padding for mobile

## Testing Templates

### Pre-Send Checklist
- [ ] All variables match CSV columns exactly
- [ ] Links are working and use absolute URLs
- [ ] Images are hosted and loading correctly
- [ ] Alt text provided for all images
- [ ] Responsive design tested
- [ ] Content is clear and error-free
- [ ] Unsubscribe link included
- [ ] Contact information present

### Testing Tools
1. **Email on Acid** - Tests across multiple clients
2. **Litmus** - Preview in various email clients
3. **Mail Tester** - Check spam score
4. **HTML Validator** - Validate HTML syntax

### Manual Testing
Send test emails to:
- Gmail (web and mobile app)
- Outlook (desktop and web)
- Apple Mail (desktop and iOS)
- Yahoo Mail
- Your own email client

## Common Patterns

### Two-Column Layout

```html
<table width="100%" border="0" cellpadding="0" cellspacing="0">
    <tr>
        <td width="50%" style="padding: 10px; vertical-align: top;">
            <!-- Left column -->
        </td>
        <td width="50%" style="padding: 10px; vertical-align: top;">
            <!-- Right column -->
        </td>
    </tr>
</table>
```

### Image + Text Block

```html
<table width="100%" border="0" cellpadding="0" cellspacing="0">
    <tr>
        <td width="150" style="padding: 10px;">
            <img src="image.jpg" alt="Description" width="130" style="display: block;">
        </td>
        <td style="padding: 10px; vertical-align: top;">
            <h3 style="margin: 0 0 10px 0;">Heading</h3>
            <p style="margin: 0; line-height: 1.6;">Description text...</p>
        </td>
    </tr>
</table>
```

### Social Media Links

```html
<table border="0" cellpadding="0" cellspacing="0" style="margin: 20px auto;">
    <tr>
        <td style="padding: 0 10px;">
            <a href="https://facebook.com/yourpage">
                <img src="facebook-icon.png" alt="Facebook" width="32" height="32">
            </a>
        </td>
        <td style="padding: 0 10px;">
            <a href="https://twitter.com/yourhandle">
                <img src="twitter-icon.png" alt="Twitter" width="32" height="32">
            </a>
        </td>
    </tr>
</table>
```

## Avoiding Spam Filters

### Content Best Practices
- Avoid excessive use of capital letters
- Don't use spam trigger words excessively (FREE, URGENT, ACT NOW)
- Balance text and images (not image-only emails)
- Include plain text version
- Use proper HTML structure

### Technical Best Practices
- Valid HTML structure
- Include alt text for images
- Proper sender authentication (SPF, DKIM, DMARC)
- Include physical mailing address
- Include unsubscribe link

## Customization Examples

### Adding a Promo Code Section

```html
<div style="background-color: #fff3cd; border: 2px dashed #ffc107; 
            border-radius: 8px; padding: 20px; margin: 20px 0; text-align: center;">
    <p style="margin: 0; font-size: 16px;">Use promo code:</p>
    <p style="margin: 10px 0; font-size: 24px; font-weight: bold; 
              color: #e74c3c; letter-spacing: 2px;">
        {{PromoCode}}
    </p>
    <p style="margin: 0;">Get {{Discount}}% OFF your next purchase!</p>
</div>
```

### Adding Event Details

```html
<div style="background-color: #ecf0f1; border-left: 4px solid #3498db; 
            padding: 20px; margin: 25px 0;">
    <h3 style="margin-top: 0; color: #2c3e50;">Event Details</h3>
    <p style="margin: 10px 0;"><strong>Date:</strong> {{EventDate}}</p>
    <p style="margin: 10px 0;"><strong>Time:</strong> {{EventTime}}</p>
    <p style="margin: 10px 0;"><strong>Location:</strong> {{VenueName}}, {{City}}</p>
</div>
```

## Resources

### Recommended Reading
- [HTML Email Development Best Practices](https://www.campaignmonitor.com/)
- [Can I email](https://www.caniemail.com/) - CSS support reference
- [Really Good Emails](https://reallygoodemails.com/) - Design inspiration

### Tools
- **HTML Email Editors**: Topol, BEE Free, Stripo
- **Image Optimization**: TinyPNG, ImageOptim
- **Color Tools**: Coolors, Adobe Color

## Troubleshooting

### Variables Not Replacing
- Check CSV column names match exactly (case-sensitive)
- Ensure proper {{}} syntax
- Verify no extra spaces in variable names

### Layout Breaking
- Use tables for structure, not divs
- Test in multiple email clients
- Validate HTML code
- Check for unclosed tags

### Images Not Showing
- Use absolute URLs (https://)
- Check image hosting
- Verify images are publicly accessible
- Include alt text

## Next Steps

- Review the [Usage Guide](USAGE-GUIDE.md) to learn how to send emails
- Check [Best Practices](BEST-PRACTICES.md) for email marketing tips
- Explore provided templates in the `templates/` directory
