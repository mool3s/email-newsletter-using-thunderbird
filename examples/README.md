# Examples

This directory contains complete examples of email newsletter campaigns showing how to use the templates and data files together.

## Available Examples

### 1. Basic Monthly Newsletter

**Use Case:** Send a monthly update to all subscribers

**Files:**
- Template: `../templates/newsletter-basic.html`
- Data: `../data/subscribers-basic.csv`

**Merge Fields Used:**
- `{{Email}}` - Recipient email
- `{{FirstName}}` - First name
- `{{LastName}}` - Last name
- `{{Company}}` - Company name
- `{{City}}` - City name
- `{{State}}` - State
- `{{ZIP}}` - Postal code
- `{{Address}}` - Street address
- `{{WebsiteURL}}` - Website link

**Sample Subject Lines:**
- "{{FirstName}}, here's your monthly update"
- "Monthly Newsletter from {{Company}}"
- "News and updates for {{City}} subscribers"

**Best Used For:**
- Regular monthly/weekly updates
- Company news
- Product announcements
- General communications

---

### 2. Promotional Campaign

**Use Case:** Send special offers with discount codes

**Files:**
- Template: `../templates/newsletter-promotional.html`
- Data: `../data/subscribers-promotional.csv`

**Merge Fields Used:**
- All basic fields plus:
- `{{PromoCode}}` - Unique promo code
- `{{Discount}}` - Discount percentage
- `{{ExpiryDate}}` - Offer expiration
- `{{Phone}}` - Contact phone

**Sample Subject Lines:**
- "{{FirstName}}, exclusive {{Discount}}% off just for you!"
- "Special offer for {{City}} - Save {{Discount}}%"
- "Your exclusive promo code: {{PromoCode}}"

**Best Used For:**
- Sales campaigns
- Special promotions
- Seasonal offers
- Product launches
- Flash sales

**Tips:**
- Create urgency with expiration dates
- Personalize offers by location
- Track promo code usage
- A/B test different discount levels

---

### 3. Event Invitation

**Use Case:** Invite subscribers to an event with RSVP

**Files:**
- Template: `../templates/newsletter-event.html`
- Data: `../data/subscribers-event.csv`

**Merge Fields Used:**
- All basic fields plus:
- `{{EventName}}` - Event title
- `{{EventDate}}` - Event date
- `{{EventTime}}` - Event time
- `{{VenueName}}` - Venue name
- `{{VenueAddress}}` - Venue address
- `{{RSVPDeadline}}` - RSVP deadline
- `{{RSVPURL}}` - RSVP link
- `{{ConfirmationCode}}` - Unique confirmation code

**Sample Subject Lines:**
- "You're invited: {{EventName}}"
- "{{FirstName}}, join us for {{EventName}}"
- "Event invitation for {{City}} - {{EventDate}}"

**Best Used For:**
- Conference invitations
- Webinar announcements
- Meetup notifications
- Workshop registrations
- Corporate events

**Tips:**
- Send 2-3 weeks in advance
- Send reminder 1 week before
- Send final reminder 1 day before
- Include calendar invite option
- Make RSVP process easy

---

## Example Workflows

### Workflow 1: First-Time Setup Test

**Goal:** Test your setup with your own emails

1. Copy `data/subscribers-basic.csv`
2. Replace with your own email addresses (2-3)
3. Update names and details
4. Use `newsletter-basic.html` template
5. Send with "Send Later" option
6. Verify receipt and formatting

### Workflow 2: Segmented Campaign

**Goal:** Send different content to different groups

**Segment 1: New Customers**
- Create `data/new-customers.csv`
- Use welcome content
- Focus on getting started

**Segment 2: Regular Customers**
- Create `data/regular-customers.csv`
- Use promotional content
- Focus on loyalty rewards

**Segment 3: Inactive Customers**
- Create `data/inactive-customers.csv`
- Use re-engagement content
- Focus on winning them back

### Workflow 3: Event Campaign Series

**Email 1: Initial Invitation**
- Send 3 weeks before event
- Use `newsletter-event.html`
- Include full event details

**Email 2: Reminder**
- Send 1 week before
- Shorter version
- Emphasize RSVP deadline

**Email 3: Final Reminder**
- Send 1 day before
- Include logistics
- Provide contact information

**Email 4: Follow-up**
- Send after event
- Thank attendees
- Share resources/photos

---

## Creating Your Own Examples

### Step 1: Define Your Goal
What do you want to achieve?
- Build awareness?
- Drive sales?
- Increase engagement?
- Invite to event?

### Step 2: Choose or Create Template
- Start with existing template
- Customize for your brand
- Add/remove sections as needed

### Step 3: Prepare Your Data
Create CSV with required fields:
```csv
Email,FirstName,LastName,...
recipient@example.com,John,Doe,...
```

### Step 4: Test Thoroughly
- Send to yourself first
- Check all links
- Verify personalization
- Test on mobile
- Check different email clients

### Step 5: Send to Small Group
- Start with 10-50 recipients
- Monitor results
- Adjust based on feedback

### Step 6: Scale Up
- Send to larger segments
- Track metrics
- Continuously improve

---

## Advanced Examples

### Multi-Step Drip Campaign

**Day 1: Welcome Email**
- Thank subscriber
- Set expectations
- Provide initial value

**Day 3: Educational Content**
- Share useful tips
- Link to resources
- Build trust

**Day 7: Product/Service Introduction**
- Introduce offering
- Highlight benefits
- Soft call-to-action

**Day 14: Social Proof**
- Share testimonials
- Show case studies
- Build credibility

**Day 21: Special Offer**
- Provide discount
- Create urgency
- Strong call-to-action

### A/B Testing Example

**Test Subject Lines:**

**Version A:** "{{FirstName}}, new products just for you"
- Send to 50% of list

**Version B:** "Exclusive offer for {{City}} residents"
- Send to other 50%

**Track:** Which has higher open rate?

---

## Tips for Each Template Type

### Basic Newsletter Tips
- Keep content focused
- Use clear headings
- Include one main CTA
- Make it scannable
- Provide value in every email

### Promotional Email Tips
- Create urgency
- Use attention-grabbing design
- Make discount prominent
- Clear CTA button
- Show what they're saving

### Event Invitation Tips
- Include all essential details upfront
- Make RSVP easy
- Provide calendar invite
- Include map/directions link
- Set clear RSVP deadline

---

## Measuring Success

### Key Metrics to Track

**Open Rate:**
- % who opened email
- Track by subject line
- Optimize based on results

**Click Rate:**
- % who clicked links
- Track which links get clicks
- Optimize CTAs

**Conversion Rate:**
- % who completed desired action
- Use UTM parameters
- Track ROI

**Bounce Rate:**
- % of undelivered emails
- Remove hard bounces immediately
- Monitor soft bounces

**Unsubscribe Rate:**
- % who unsubscribed
- Should be <0.5%
- Indicates content relevance

---

## Need Help?

- **Getting Started:** See [QUICKSTART.md](../QUICKSTART.md)
- **Template Customization:** See [Template Guide](../docs/TEMPLATE-GUIDE.md)
- **Best Practices:** See [Best Practices](../docs/BEST-PRACTICES.md)
- **Common Issues:** See [FAQ](../docs/FAQ.md)

---

## Contributing Examples

Have a great example to share?

1. Create your template and data files
2. Document the use case
3. Include sample subject lines
4. Add tips and best practices
5. Submit a pull request

See [CONTRIBUTING.md](../CONTRIBUTING.md) for guidelines.
