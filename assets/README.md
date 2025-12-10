# Assets Directory

This directory contains resources for email newsletter templates.

## Directory Structure

```
assets/
├── images/     # Image files for email templates
├── css/        # CSS files (for reference, use inline CSS in templates)
└── README.md   # This file
```

## Images Directory

Store images that will be used in your email templates. 

### Best Practices for Email Images

**File Formats:**
- **JPEG** - Photos and complex images
- **PNG** - Logos, graphics with transparency
- **GIF** - Simple animations (use sparingly)

**Optimization:**
- Compress images to reduce file size
- Maximum width: 600px (standard email width)
- Use web-safe formats
- Optimize for fast loading

**Hosting:**
- Images must be hosted online (not local files)
- Use absolute URLs in templates: `https://example.com/image.jpg`
- Consider using:
  - Your website server
  - Image hosting services (Imgur, Cloudinary)
  - CDN services
  - Your email hosting provider

**Alt Text:**
Always include descriptive alt text:
```html
<img src="https://example.com/logo.png" 
     alt="Company Logo" 
     width="200" 
     height="100">
```

### Image Naming Conventions

Use clear, descriptive names:
- ✅ `company-logo.png`
- ✅ `header-banner-2025.jpg`
- ✅ `product-feature-icon.png`
- ❌ `img1.jpg`
- ❌ `untitled.png`

### Image Sizes

**Recommended Dimensions:**
- Header images: 600px width
- Logo: 200-300px width
- Product images: 300-400px width
- Icons: 32-64px
- Social media icons: 24-32px

**File Size:**
- Keep individual images under 100KB
- Total email size: under 1MB including all images

## CSS Directory

While email templates should use inline CSS, this directory can store:
- Reference stylesheets
- Design system documentation
- CSS snippets for copying into templates

### Using CSS in Email Templates

**DO:**
- Use inline styles: `<p style="color: #333;">`
- Use web-safe fonts
- Use full hex color codes: `#3498db`
- Use tables for layout

**DON'T:**
- Don't use external stylesheets
- Don't use complex CSS features
- Don't rely on JavaScript
- Don't use advanced selectors

## Usage Example

### In Your HTML Template:

```html
<!-- Hosted image -->
<img src="https://yourwebsite.com/assets/images/logo.png" 
     alt="Company Logo" 
     width="200" 
     height="80"
     style="display: block; margin: 0 auto;">

<!-- With styling -->
<div style="text-align: center; padding: 20px;">
    <img src="https://cdn.example.com/newsletter-header.jpg"
         alt="Newsletter Header"
         width="600"
         style="max-width: 100%; height: auto;">
</div>
```

## Image Checklist

Before using images in email templates:

- [ ] Image is compressed and optimized
- [ ] Image has appropriate dimensions
- [ ] Image is hosted online (not local)
- [ ] URL is absolute (https://)
- [ ] Alt text is included
- [ ] Image loads correctly
- [ ] Image is relevant to content
- [ ] Image enhances the message

## Free Image Resources

If you need images for your newsletters:

**Stock Photos:**
- Unsplash (https://unsplash.com)
- Pexels (https://pexels.com)
- Pixabay (https://pixabay.com)

**Icons:**
- Font Awesome (https://fontawesome.com)
- Flaticon (https://flaticon.com)
- Icons8 (https://icons8.com)

**Image Editing:**
- Canva (https://canva.com)
- Photopea (https://photopea.com)
- GIMP (https://gimp.org)

**Image Optimization:**
- TinyPNG (https://tinypng.com)
- ImageOptim (https://imageoptim.com)
- Squoosh (https://squoosh.app)

## Notes

- This directory structure is for organizational purposes
- Actual images used in emails must be hosted online
- Update image URLs in templates to point to your hosted images
- Keep backup copies of all images used in campaigns
- Test image loading across different email clients
- Monitor image hosting service uptime and reliability

## Questions?

See the main [Template Guide](../docs/TEMPLATE-GUIDE.md) for more information on using images in email templates.
