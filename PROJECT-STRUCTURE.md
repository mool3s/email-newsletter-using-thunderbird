# Project Structure Guide

This document explains the organization of files and folders in this project.

## Directory Tree

```
Email-Newsletter-using-Thunderbird/
│
├── 📄 README.md                    # Project overview and main documentation
├── 📄 QUICKSTART.md                # 10-minute quick start guide
├── 📄 PROJECT-STRUCTURE.md         # This file - explains project organization
├── 📄 CONTRIBUTING.md              # Guidelines for contributors
├── 📄 LICENSE                      # MIT License
├── 📄 .gitignore                   # Files to exclude from git
│
├── 📁 templates/                   # Email newsletter templates
│   ├── newsletter-basic.html      # General purpose newsletter
│   ├── newsletter-promotional.html # Sales and promotions
│   └── newsletter-event.html      # Event invitations
│
├── 📁 data/                        # Sample CSV data files
│   ├── subscribers-basic.csv      # Basic subscriber data
│   ├── subscribers-promotional.csv # Promotional campaign data
│   └── subscribers-event.csv      # Event invitation data
│
├── 📁 docs/                        # Comprehensive documentation
│   ├── SETUP-GUIDE.md             # Installation and setup
│   ├── USAGE-GUIDE.md             # How to send newsletters
│   ├── TEMPLATE-GUIDE.md          # Template customization
│   ├── BEST-PRACTICES.md          # Email marketing tips
│   └── FAQ.md                     # Frequently asked questions
│
├── 📁 examples/                    # Usage examples and workflows
│   └── README.md                  # Example campaigns and use cases
│
└── 📁 assets/                      # Resources for templates
    ├── README.md                  # Assets usage guide
    ├── 📁 images/                 # Image files directory
    └── 📁 css/                    # CSS reference files
```

## File Categories

### 🚀 Getting Started Files

**Start here if you're new:**

1. **README.md** - Overview of the project, features, and quick links
2. **QUICKSTART.md** - Get up and running in 10 minutes
3. **docs/SETUP-GUIDE.md** - Detailed installation instructions

### 📧 Email Templates

**Location:** `templates/` folder

**What they are:** Ready-to-use HTML email templates with merge fields

**Templates available:**
- `newsletter-basic.html` - Clean, professional design for general newsletters
- `newsletter-promotional.html` - Eye-catching design for sales and offers
- `newsletter-event.html` - Elegant design for event invitations

**How to use:**
1. Open template in text editor
2. Customize content as needed
3. Copy HTML into Thunderbird compose window
4. Use with corresponding CSV data file

### 📊 Data Files

**Location:** `data/` folder

**What they are:** Sample CSV files with subscriber information

**Files available:**
- `subscribers-basic.csv` - For basic newsletter
- `subscribers-promotional.csv` - For promotional campaigns
- `subscribers-event.csv` - For event invitations

**How to use:**
1. Open CSV in spreadsheet program (Excel, Google Sheets)
2. Replace sample data with your real data
3. Ensure column headers match template variables
4. Save as CSV format
5. Use with Mail Merge in Thunderbird

### 📚 Documentation

**Location:** `docs/` folder

**What it contains:** Comprehensive guides for all aspects of the project

| File | Purpose | When to Read |
|------|---------|--------------|
| SETUP-GUIDE.md | Install and configure | First time setup |
| USAGE-GUIDE.md | Send newsletters | Before sending emails |
| TEMPLATE-GUIDE.md | Customize templates | When creating custom designs |
| BEST-PRACTICES.md | Email marketing tips | To improve campaigns |
| FAQ.md | Common questions | When troubleshooting |

### 💡 Examples

**Location:** `examples/` folder

**What it contains:** Real-world use cases and campaign workflows

**Includes:**
- Complete campaign examples
- Multi-step drip campaigns
- A/B testing guides
- Segmentation strategies
- Success metrics

### 🎨 Assets

**Location:** `assets/` folder

**What it contains:** Supporting files for email templates

**Subdirectories:**
- `images/` - Store images for your newsletters
- `css/` - CSS reference files (use inline CSS in templates)

**Note:** Images must be hosted online to work in emails

### 📝 Project Files

**Contributing Guidelines:** `CONTRIBUTING.md`
- How to contribute to this project
- Template submission guidelines
- Code of conduct

**License:** `LICENSE`
- MIT License terms
- Open-source usage rights

**Git Configuration:** `.gitignore`
- Files excluded from version control
- Keeps repository clean

## Typical User Journeys

### Journey 1: Complete Beginner

```
README.md (overview)
    ↓
QUICKSTART.md (10-minute guide)
    ↓
docs/SETUP-GUIDE.md (if installation needed)
    ↓
Use templates/newsletter-basic.html + data/subscribers-basic.csv
    ↓
docs/FAQ.md (if issues arise)
```

### Journey 2: Ready to Send

```
Already have Thunderbird + Mail Merge installed
    ↓
docs/USAGE-GUIDE.md (learn the process)
    ↓
Choose template from templates/
    ↓
Prepare CSV data file
    ↓
Send test emails
    ↓
Send to full list
```

### Journey 3: Customization

```
Understanding basics
    ↓
docs/TEMPLATE-GUIDE.md (learn customization)
    ↓
Modify template from templates/
    ↓
Create custom CSV data
    ↓
docs/BEST-PRACTICES.md (optimize campaign)
    ↓
examples/README.md (see real-world use cases)
```

### Journey 4: Advanced User

```
Experienced with email marketing
    ↓
Review templates/ for ideas
    ↓
docs/BEST-PRACTICES.md (learn platform-specific tips)
    ↓
examples/README.md (complex workflows)
    ↓
Create custom templates and campaigns
```

## Finding What You Need

### "I want to..."

**...send my first newsletter**
- Start: QUICKSTART.md
- Then: docs/USAGE-GUIDE.md

**...install Thunderbird and Mail Merge**
- Go to: docs/SETUP-GUIDE.md

**...customize a template**
- Start: templates/ (pick one)
- Guide: docs/TEMPLATE-GUIDE.md

**...understand merge fields**
- Read: docs/TEMPLATE-GUIDE.md (Merge Variables section)
- See: data/ files for examples

**...learn email marketing**
- Read: docs/BEST-PRACTICES.md
- Study: examples/README.md

**...fix a problem**
- Check: docs/FAQ.md
- Also: docs/USAGE-GUIDE.md (Troubleshooting section)

**...see examples of campaigns**
- Browse: examples/README.md
- Review: All three templates in templates/

**...contribute to the project**
- Read: CONTRIBUTING.md
- Review: docs/TEMPLATE-GUIDE.md for standards

## File Naming Conventions

### Templates
- Format: `newsletter-[type].html`
- Examples: `newsletter-basic.html`, `newsletter-promotional.html`
- All lowercase with hyphens

### Data Files
- Format: `subscribers-[type].csv`
- Examples: `subscribers-basic.csv`, `subscribers-event.csv`
- Match corresponding template types

### Documentation
- Format: `[NAME]-GUIDE.md` or `[TOPIC].md`
- Examples: `SETUP-GUIDE.md`, `FAQ.md`
- ALL CAPS for guides, sentence case for other docs

## Recommended Reading Order

### For First-Time Users:

1. **README.md** (5 minutes) - Get the overview
2. **QUICKSTART.md** (10 minutes) - Send first test
3. **docs/SETUP-GUIDE.md** (15 minutes) - If you need to install
4. **docs/USAGE-GUIDE.md** (20 minutes) - Learn the full process
5. **docs/FAQ.md** (as needed) - Solve problems

### For Template Customizers:

1. **docs/TEMPLATE-GUIDE.md** (30 minutes) - Learn HTML email
2. **templates/** (20 minutes) - Study existing templates
3. **docs/BEST-PRACTICES.md** (30 minutes) - Design principles
4. **examples/README.md** (20 minutes) - See use cases

### For Email Marketers:

1. **docs/BEST-PRACTICES.md** (30 minutes) - Strategy and tactics
2. **examples/README.md** (20 minutes) - Campaign workflows
3. **docs/USAGE-GUIDE.md** (15 minutes) - Platform specifics
4. **docs/TEMPLATE-GUIDE.md** (20 minutes) - Optimization tips

## Updating Your Copy

To get the latest version:

```bash
# If you cloned the repository
cd Email-Newsletter-using-Thunderbird
git pull origin main

# Or download the latest ZIP from GitHub
```

## What's Not Included

This project does NOT include:
- Email tracking/analytics tools
- Automation or scheduling
- List management software
- Image files (you need to host your own)
- Email validation services
- Subscriber management database

These are manual tools for sending personalized newsletters using free software.

## Questions About Structure?

- See: README.md for project overview
- See: docs/FAQ.md for common questions
- See: CONTRIBUTING.md to suggest improvements

## Tips for Navigating

1. **Start with README.md** - Always begin here
2. **Use QUICKSTART.md** - Fastest way to test
3. **Bookmark docs/** - Reference documentation
4. **Study templates/** - Learn by example
5. **Check examples/** - See real use cases

## Quick Reference

| I need... | Go to... |
|-----------|----------|
| Overview | README.md |
| Quick test | QUICKSTART.md |
| Installation | docs/SETUP-GUIDE.md |
| How to send | docs/USAGE-GUIDE.md |
| Customize | docs/TEMPLATE-GUIDE.md |
| Tips & tricks | docs/BEST-PRACTICES.md |
| Help | docs/FAQ.md |
| Templates | templates/ |
| Sample data | data/ |
| Examples | examples/README.md |
| Images | assets/ |
| Contribute | CONTRIBUTING.md |
