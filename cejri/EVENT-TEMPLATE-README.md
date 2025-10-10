# CEJRI Event Template - Usage Guide

## Overview
This is a modern, reusable event page template designed specifically for CEJRI events (courses, conferences, workshops, etc.). It follows the CEJRI Design System and provides a consistent, professional look across all event pages.

---

## Files

### Core Files
- **`corso-bobath.html`** - Example implementation (current Bobath course)
- **`css/event-template.css`** - Reusable event page styles
- **`css/cejri-modern.css`** - CEJRI design system (shared with main site)

### Backup
- **`corso-bobath-old.html`** - Original version (before modernization)

---

## How to Create a New Event Page

### Step 1: Copy the Template
```bash
cp corso-bobath.html your-event-name.html
```

### Step 2: Update Meta Information
Replace the following in the `<head>` section:

```html
<!-- Update Title -->
<title>Your Event Name | Centro Jonico Riabilitativo | Bianco (RC)</title>

<!-- Update Description -->
<meta name="description" content="Your event description here..." />

<!-- Update Schema.org & Open Graph -->
<meta itemprop="name" content="Your Event Name - Ce.J.Ri">
<meta itemprop="description" content="Your event description...">
<meta property="og:title" content="Your Event Name - Ce.J.Ri" />
<meta property="og:description" content="Your event description..." />
<meta property="og:url" content="http://www.medicalandpsychology.com/cejri/your-event-name.html" />
```

### Step 3: Update Hero Section

```html
<section class="event-hero">
    <div class="event-hero-background"></div>
    <div class="event-hero-content">
        <!-- Update Badge -->
        <div class="event-badge">
            <i class="fa fa-graduation-cap"></i> <!-- Change icon if needed -->
            <span>Event Category</span> <!-- e.g., "Formazione Professionale", "Convegno", etc. -->
        </div>

        <!-- Update Title -->
        <h1 class="event-title">YOUR EVENT NAME</h1>

        <!-- Update Subtitle -->
        <p class="event-subtitle">Event subtitle or tagline</p>

        <!-- Update Organizer -->
        <p class="event-organizer">Organizer information</p>

        <!-- Update Meta Items -->
        <div class="event-hero-meta">
            <div class="meta-item">
                <i class="fa fa-calendar"></i>
                <div>
                    <strong>Date</strong>
                    <span>Event dates</span>
                </div>
            </div>
            <div class="meta-item">
                <i class="fa fa-map-marker"></i>
                <div>
                    <strong>Sede</strong>
                    <span>Event location</span>
                </div>
            </div>
            <div class="meta-item">
                <i class="fa fa-certificate"></i> <!-- Change icon as needed -->
                <div>
                    <strong>Key Info</strong>
                    <span>Important detail</span>
                </div>
            </div>
        </div>
    </div>
</section>
```

### Step 4: Update Content Sections

The template includes several pre-built section types. Use what you need and remove what you don't:

#### Speaker/Relatori Section
```html
<div class="event-section">
    <div class="section-icon">
        <i class="fa fa-user-md"></i>
    </div>
    <h2 class="section-title">RELATORI</h2>
    <div class="content-card">
        <ul class="speakers-list">
            <li>
                <i class="fa fa-user-md"></i>
                <span>Speaker Name</span>
            </li>
        </ul>
    </div>
</div>
```

#### Dates Section
```html
<div class="event-section">
    <div class="section-icon">
        <i class="fa fa-calendar"></i>
    </div>
    <h2 class="section-title">DATE</h2>
    <div class="content-card">
        <p class="info-text">Description text...</p>
        <div class="dates-grid">
            <div class="date-card">
                <div class="date-icon">
                    <i class="fa fa-calendar-o"></i>
                </div>
                <div class="date-info">
                    <strong>Date Label</strong>
                    <span>Date details</span>
                </div>
            </div>
        </div>
    </div>
</div>
```

#### Pricing Section
```html
<div class="event-section">
    <div class="section-icon">
        <i class="fa fa-euro"></i>
    </div>
    <h2 class="section-title">PRICING</h2>
    <div class="content-card pricing-card">
        <div class="price-main">
            <span class="price-amount">€ 1.200</span>
            <span class="price-label">complessivi</span>
        </div>
        <div class="payment-options">
            <p class="info-text">Payment details...</p>
            <ul class="payment-list">
                <li><span class="rate-number">Option 1:</span> details</li>
            </ul>
        </div>
    </div>
</div>
```

#### Contact Section
```html
<div class="event-section">
    <div class="section-icon">
        <i class="fa fa-phone"></i>
    </div>
    <h2 class="section-title">CONTATTI</h2>
    <div class="content-card contact-card">
        <div class="contact-name">
            <strong>Contact Person Name</strong>
        </div>
        <div class="contact-details">
            <div class="contact-item">
                <i class="fa fa-phone"></i>
                <span>Tel. xxx</span>
            </div>
        </div>
    </div>
</div>
```

#### Downloads Section
```html
<div class="event-section downloads-section">
    <div class="section-icon">
        <i class="fa fa-download"></i>
    </div>
    <h2 class="section-title">DOCUMENTI</h2>
    <div class="downloads-grid">
        <a href="your-link" target="_blank" class="download-card">
            <div class="download-icon">
                <i class="fa fa-file-pdf-o"></i>
            </div>
            <div class="download-info">
                <strong>Document Title</strong>
                <span>Document description</span>
            </div>
            <i class="fa fa-arrow-right"></i>
        </a>
    </div>
</div>
```

### Step 5: Update CTA Section
```html
<div class="event-cta">
    <h3>Interested in this event?</h3>
    <p>Call to action description</p>
    <a href="your-registration-link" target="_blank" class="cta-button">
        <i class="fa fa-envelope"></i>
        <span>Register Now</span>
    </a>
</div>
```

---

## Available Section Icons

Use Font Awesome icons (already included). Common ones:

- `fa-graduation-cap` - Education/courses
- `fa-calendar` - Dates
- `fa-map-marker` - Location
- `fa-user-md` - Speakers/doctors
- `fa-certificate` - Credentials/certifications
- `fa-users` - Participants
- `fa-euro` - Pricing
- `fa-phone` - Contact
- `fa-envelope` - Email
- `fa-download` - Downloads
- `fa-pencil-square-o` - Registration
- `fa-building` - Venue

[Full Font Awesome 4.7 icon list](https://fontawesome.com/v4/icons/)

---

## Design System Guidelines

### Colors
The template automatically uses CEJRI brand colors from `cejri-modern.css`:
- **Primary Blue**: `#2563eb`
- **Secondary Green**: `#059669`
- **Accent Orange**: `#f59e0b`

### Typography
All typography follows the CEJRI design system with responsive sizing.

### Spacing
Uses the standard spacing scale (`--space-2` through `--space-24`).

### Cards & Borders
- Border radius: Consistent rounded corners
- Shadows: Subtle elevation with hover effects
- Borders: Light blue tint for premium feel

---

## Best Practices

### Content
1. **Keep content concise** - Users scan, don't read everything
2. **Use bullet points** - Better readability than paragraphs
3. **Highlight key information** - Use bold for important details
4. **Include visual hierarchy** - Use section icons and titles effectively

### Structure
1. **Hero first** - Most important info at the top
2. **Progressive disclosure** - Details in order of importance
3. **Clear CTA** - Make registration/contact obvious
4. **Downloads at end** - After user has context

### Mobile
- Template is fully responsive
- Test on mobile devices
- Ensure all interactive elements are tap-friendly

### Accessibility
- All icons have semantic meaning
- Alt text on images
- Proper heading hierarchy
- Color contrast meets WCAG standards

---

## Customization

### Adding New Section Types

If you need a section type not in the template:

1. Follow the existing structure:
```html
<div class="event-section">
    <div class="section-icon">
        <i class="fa fa-your-icon"></i>
    </div>
    <h2 class="section-title">SECTION TITLE</h2>
    <div class="content-card">
        <!-- Your content here -->
    </div>
</div>
```

2. Use existing CSS classes when possible
3. If you need custom styles, add them to a separate CSS file (don't modify `event-template.css`)

### Custom Colors (Per Event)

If an event needs unique colors, add inline styles:

```html
<style>
    .event-hero {
        background: your-custom-gradient;
    }
    .section-title {
        color: your-custom-color;
        border-bottom-color: your-custom-color;
    }
</style>
```

---

## Maintenance

### When Updating the Design System
If you update `cejri-modern.css`, all event pages automatically inherit those changes.

### When Fixing Bugs
Fix in `event-template.css` - all event pages benefit.

### When Changing Content
Edit individual event HTML files only.

---

## Examples

### Current Implementation
- **Corso Bobath Base** (`corso-bobath.html`) - Professional course with all features

### Suggested Future Events
- Medical conferences
- Workshops and seminars
- Open days/recruitment events
- Continuing education courses
- Community health events

---

## Support

For questions or issues with the template:
1. Check this README
2. Review the CEJRI Design System docs at `/planning/01-website-restyling/`
3. Reference the Corso Bobath implementation

---

## Changelog

### Version 1.0 (January 2025)
- Initial template creation
- Based on CEJRI Modern Design System
- Implemented for Corso Bobath Base
- Full responsive design
- Reusable component library
