# Task List: Medical & Psychology Website Restyling

## Overview

This task list breaks down the complete website restyling project into actionable implementation steps. Each task corresponds to requirements defined in the PRD and technical architecture outlined in the Technical Blueprint. Tasks are organized sequentially by implementation phase, designed for systematic execution while maintaining the simple HTML structure of the original site.

## Relevant Files

**HTML Pages:**
- `index.html` - Main landing page (to be modernized)
- `santeufemia.html` - Centro G. Chirico detail page (to be modernized)
- `maintenance.html` - Additional services page (to be modernized)
- `portage.html` - Portage methodology page (to be modernized)
- `other-projects.html` - Projects history page (to be modernized)

**CSS Files (New/Modernized):**
- `css/modern-design-system.css` - New unified stylesheet (to be created)
- `css/main.css` - Legacy file (to be replaced/archived)
- `css/styles.css` - Legacy file (to be replaced/archived)
- `css/bootstrap.min.css` - Bootstrap 3 (to be removed)

**JavaScript Files (New/Modernized):**
- `js/minimal-interactions.js` - New vanilla JS file (to be created)
- `js/jquery.min.js` - Legacy jQuery (to be removed)
- `js/bootstrap.min.js` - Legacy Bootstrap JS (to be removed)
- `js/wow.js` - Legacy animations (to be removed)
- `js/main.js` - Legacy custom JS (to be replaced)

**Image Assets:**
- `images/home.jpg` - Hero image (to be optimized)
- `images/bg.jpg` - Background image (to be optimized)
- `images/background-main.png` - Background (to be optimized)
- `images/banner-*.png` - Various banners (to be optimized)

**Documentation:**
- `planning/01-website-restyling/prd.md` - Product requirements
- `planning/01-website-restyling/technical_blueprint.md` - Architecture
- `planning/01-website-restyling/tasks.md` - This file

## Tasks

### 1.0 Design System Foundation

- [ ] 1.1 Audit current `css/main.css` and extract color palette values
- [ ] 1.2 Audit current `css/styles.css` and extract typography settings
- [ ] 1.3 Document all spacing values used across both CSS files
- [ ] 1.4 Create `css/modern-design-system.css` with CSS custom properties
- [ ] 1.5 Define CSS variables for colors (primary, secondary, text, background)
- [ ] 1.6 Define CSS variables for spacing (margins, padding scale)
- [ ] 1.7 Define CSS variables for typography (font families, sizes, weights)
- [ ] 1.8 Update Google Fonts import from HTTP to HTTPS in new stylesheet
- [ ] 1.9 Add system font fallbacks to font-family declarations
- [ ] 1.10 Test CSS variables work correctly in all modern browsers

### 2.0 Layout Modernization - Index Page

- [ ] 2.1 Create backup copy of original `index.html` as `index.html.backup`
- [ ] 2.2 Remove Bootstrap 3 CSS link from `index.html`
- [ ] 2.3 Link new `css/modern-design-system.css` in `index.html`
- [ ] 2.4 Convert hero section (#first) layout to CSS Grid
- [ ] 2.5 Convert about section (#main) layout to CSS Grid
- [ ] 2.6 Convert banner section (#banner) layout to Flexbox
- [ ] 2.7 Convert activities section (#one) layout to CSS Grid
- [ ] 2.8 Update footer layout with Flexbox
- [ ] 2.9 Implement mobile-first responsive breakpoints (320px, 768px, 1024px)
- [ ] 2.10 Test layout across all breakpoints on multiple devices
- [ ] 2.11 Verify visual structure matches original design intent

### 3.0 Layout Modernization - Additional Pages

- [ ] 3.1 Create backup of `santeufemia.html` as `santeufemia.html.backup`
- [ ] 3.2 Apply modern layout system to `santeufemia.html`
- [ ] 3.3 Create backup of `maintenance.html` as `maintenance.html.backup`
- [ ] 3.4 Apply modern layout system to `maintenance.html`
- [ ] 3.5 Create backup of `portage.html` as `portage.html.backup`
- [ ] 3.6 Apply modern layout system to `portage.html`
- [ ] 3.7 Create backup of `other-projects.html` as `other-projects.html.backup`
- [ ] 3.8 Apply modern layout system to `other-projects.html`
- [ ] 3.9 Test all pages for layout consistency
- [ ] 3.10 Verify responsive behavior on all pages

### 4.0 CEJRI Brand Integration

- [ ] 4.1 Analyze content structure in `cejri/` subdirectory
- [ ] 4.2 Document CEJRI content that should be integrated into main site
- [ ] 4.3 Design navigation showing Medical & Psychology → CEJRI hierarchy
- [ ] 4.4 Update header in `index.html` to show brand relationship
- [ ] 4.5 Redesign #banner section to integrate CEJRI (not external link)
- [ ] 4.6 Create visual hierarchy showing parent company relationship
- [ ] 4.7 Update internal links to reflect new structure
- [ ] 4.8 Add CEJRI content section to main site navigation
- [ ] 4.9 Test all navigation flows and link destinations
- [ ] 4.10 Verify brand messaging clarity with stakeholder review

### 5.0 JavaScript Modernization

- [ ] 5.1 Remove jQuery script tag from all HTML pages
- [ ] 5.2 Remove Bootstrap 3 JavaScript from all HTML pages
- [ ] 5.3 Remove `js/wow.js` script tag from all pages
- [ ] 5.4 Remove `js/jquery.prettyPhoto.js` from all pages
- [ ] 5.5 Remove `js/jquery.isotope.min.js` from all pages
- [ ] 5.6 Remove `js/owl.carousel.min.js` from all pages
- [ ] 5.7 Create new `js/minimal-interactions.js` file
- [ ] 5.8 Implement smooth scroll functionality in vanilla JavaScript
- [ ] 5.9 Implement Intersection Observer for lazy loading images
- [ ] 5.10 Add simple fade-in animations using CSS classes
- [ ] 5.11 Test all interactions work without jQuery
- [ ] 5.12 Verify no JavaScript console errors across all pages

### 6.0 Performance Optimization - Legacy Code Removal

- [ ] 6.1 Remove `js/ie/html5shiv.js` file and script tag
- [ ] 6.2 Remove `js/ie/respond.min.js` file and script tag
- [ ] 6.3 Remove IE conditional comments from all HTML files
- [ ] 6.4 Archive old jQuery files to `_archive/` folder
- [ ] 6.5 Archive old Bootstrap files to `_archive/` folder
- [ ] 6.6 Archive old plugin files to `_archive/` folder
- [ ] 6.7 Update HTML to remove references to archived files
- [ ] 6.8 Test site loads correctly without legacy dependencies
- [ ] 6.9 Verify JavaScript payload reduction (check browser DevTools)
- [ ] 6.10 Document removed files in project changelog

### 7.0 Image Optimization - Compression & Formats

- [ ] 7.1 Install image optimization tool (ImageMagick, Squoosh CLI, or Sharp)
- [ ] 7.2 Compress `images/home.jpg` (16.4MB) to <500KB JPEG
- [ ] 7.3 Generate WebP version of `images/home.jpg` at 300KB target
- [ ] 7.4 Generate AVIF version of `images/home.jpg` at 250KB target
- [ ] 7.5 Compress `images/background-main.png` (1.7MB) to <200KB
- [ ] 7.6 Generate WebP version of `images/background-main.png`
- [ ] 7.7 Generate AVIF version of `images/background-main.png`
- [ ] 7.8 Compress `images/bg.jpg` to optimal size
- [ ] 7.9 Compress all `images/banner-*.png` files
- [ ] 7.10 Verify image quality is acceptable after compression

### 8.0 Image Optimization - Responsive Images & Lazy Loading

- [ ] 8.1 Create 1x, 2x, 3x versions of hero image for different screens
- [ ] 8.2 Implement `<picture>` element with WebP/AVIF/JPEG sources
- [ ] 8.3 Add `srcset` attributes for responsive image loading
- [ ] 8.4 Add `loading="lazy"` attribute to below-fold images
- [ ] 8.5 Implement Intersection Observer fallback for older browsers
- [ ] 8.6 Add low-quality placeholder images for lazy-loaded content
- [ ] 8.7 Test lazy loading triggers correctly on scroll
- [ ] 8.8 Verify correct image format served based on browser support
- [ ] 8.9 Test responsive srcsets load appropriate sizes
- [ ] 8.10 Measure total page weight reduction (target 70% reduction)

### 9.0 Footer & Third-Party Integrations

- [ ] 9.1 Update footer HTML structure with modern semantic markup
- [ ] 9.2 Apply new design system styles to footer
- [ ] 9.3 Verify Iubenda privacy policy widget loads correctly
- [ ] 9.4 Test Iubenda widget displays privacy policy properly
- [ ] 9.5 Verify Whistleblowing portal link works (external)
- [ ] 9.6 Verify Google Drive documentation link works (external)
- [ ] 9.7 Test Google Analytics tracking code (UA-89376496-1)
- [ ] 9.8 Verify pageview events fire in Google Analytics real-time
- [ ] 9.9 Update copyright year with JavaScript automation
- [ ] 9.10 Test footer displays correctly on mobile devices

### 10.0 Cross-Browser & Device Testing

- [ ] 10.1 Test on Chrome (Windows) - latest version
- [ ] 10.2 Test on Chrome (macOS) - latest version
- [ ] 10.3 Test on Firefox (Windows) - latest version
- [ ] 10.4 Test on Firefox (macOS) - latest version
- [ ] 10.5 Test on Safari (macOS) - latest version
- [ ] 10.6 Test on Edge (Windows) - latest version
- [ ] 10.7 Test on iPhone (Safari iOS) - multiple screen sizes
- [ ] 10.8 Test on Android (Chrome Mobile) - multiple screen sizes
- [ ] 10.9 Test on iPad (Safari) - portrait and landscape
- [ ] 10.10 Document any browser-specific issues found

### 11.0 Performance Testing & Optimization

- [ ] 11.1 Run Google Lighthouse audit on index.html
- [ ] 11.2 Address any performance issues to achieve 90+ score
- [ ] 11.3 Run WebPageTest on 3G connection simulation
- [ ] 11.4 Optimize any resources causing slow load times
- [ ] 11.5 Minify `css/modern-design-system.css`
- [ ] 11.6 Minify `js/minimal-interactions.js`
- [ ] 11.7 Enable gzip/brotli compression on server (if not enabled)
- [ ] 11.8 Test First Contentful Paint (target <1.5s)
- [ ] 11.9 Test Time to Interactive (target <2.5s)
- [ ] 11.10 Document performance improvements vs. baseline

### 12.0 Accessibility Testing & Improvements

- [ ] 12.1 Run WAVE accessibility checker on all pages
- [ ] 12.2 Fix any errors identified by WAVE
- [ ] 12.3 Run axe DevTools automated scan
- [ ] 12.4 Address any critical accessibility issues
- [ ] 12.5 Test keyboard navigation (Tab, Enter, Esc)
- [ ] 12.6 Verify all interactive elements are keyboard accessible
- [ ] 12.7 Test with screen reader (VoiceOver or NVDA)
- [ ] 12.8 Verify all images have appropriate alt text
- [ ] 12.9 Check color contrast ratios (WCAG AA minimum)
- [ ] 12.10 Fix any contrast issues found

### 13.0 Content Verification & Link Validation

- [ ] 13.1 Verify all text content preserved from original site
- [ ] 13.2 Proofread all pages for typos or formatting issues
- [ ] 13.3 Test all internal links navigate correctly
- [ ] 13.4 Test all external links open and work properly
- [ ] 13.5 Verify all anchor links (#section) scroll to correct position
- [ ] 13.6 Check contact information is accurate and up-to-date
- [ ] 13.7 Verify legal/compliance footer text is correct
- [ ] 13.8 Test email links open default mail client
- [ ] 13.9 Verify phone numbers are clickable on mobile
- [ ] 13.10 Check all page titles and meta descriptions

### 14.0 Pre-Deployment Preparation

- [ ] 14.1 Create complete backup of current production site
- [ ] 14.2 Document backup location and restore procedure
- [ ] 14.3 Set up staging environment (if not already exists)
- [ ] 14.4 Deploy modernized site to staging server
- [ ] 14.5 Configure server MIME types for WebP/AVIF
- [ ] 14.6 Enable HTTPS on staging environment
- [ ] 14.7 Test all functionality on staging environment
- [ ] 14.8 Schedule client review of staging site
- [ ] 14.9 Incorporate client feedback and make revisions
- [ ] 14.10 Obtain final client approval for deployment

### 15.0 Production Deployment & Monitoring

- [ ] 15.1 Schedule deployment window (low traffic period)
- [ ] 15.2 Deploy modernized site to production server
- [ ] 15.3 Verify all pages load correctly on production
- [ ] 15.4 Test Google Analytics tracking on production
- [ ] 15.5 Test all third-party integrations on production
- [ ] 15.6 Check for any console errors or warnings
- [ ] 15.7 Monitor Google Analytics real-time for issues (24 hours)
- [ ] 15.8 Monitor server error logs for 404s or 500 errors
- [ ] 15.9 Verify mobile usability in Google Search Console
- [ ] 15.10 Submit updated sitemap to Google Search Console (if changed)

### 16.0 Documentation & Handoff

- [ ] 16.1 Create maintenance documentation for client
- [ ] 16.2 Document how to update HTML content
- [ ] 16.3 Document image optimization workflow for new images
- [ ] 16.4 Create CSS custom property reference guide
- [ ] 16.5 Document supported browsers policy
- [ ] 16.6 Create rollback procedure documentation
- [ ] 16.7 Document all third-party integrations and renewal dates
- [ ] 16.8 Provide technical support contact information
- [ ] 16.9 Archive old site files with proper labeling
- [ ] 16.10 Conduct final project review meeting with stakeholders

## Notes

### General Guidelines
- Create backups before modifying any existing files
- Test changes incrementally to catch issues early
- Use browser DevTools to verify CSS and JavaScript changes
- Maintain git commits for each major task completion
- Follow mobile-first approach when implementing responsive styles

### Testing Commands
- Lighthouse: Run from Chrome DevTools (F12 → Lighthouse tab)
- WAVE: Install browser extension or use https://wave.webaim.org
- Validate HTML: Use https://validator.w3.org
- Test mobile: Use Chrome DevTools device emulation (Cmd+Shift+M)

### Browser Support
- Chrome, Firefox, Safari, Edge (latest 2 versions only)
- No IE support required (legacy polyfills removed)
- Mobile: iOS Safari 13+, Chrome Mobile latest

### Image Optimization Tools
- Online: Squoosh (https://squoosh.app)
- CLI: ImageMagick, Sharp, or cwebp/avif tools
- Target: WebP quality 85, AVIF quality 80, JPEG quality 85

### Performance Targets
- Total page weight: <1MB (currently 16MB+)
- JavaScript payload: <10KB (currently 500KB+)
- First Contentful Paint: <1.5s
- Lighthouse Performance Score: 90+

### Code Standards
- Use semantic HTML5 elements (header, nav, main, section, article, footer)
- CSS: Use kebab-case for class names
- JavaScript: Use ES6+ syntax, camelCase for variables
- Indentation: 2 spaces for HTML/CSS/JS
- Comments: Document complex CSS Grid/Flexbox layouts

### Deployment Checklist
- ✅ Backup current production site
- ✅ Test on staging environment
- ✅ Client approval obtained
- ✅ Server configured for WebP/AVIF MIME types
- ✅ HTTPS enabled
- ✅ Monitoring tools ready
- ✅ Rollback plan documented

### Contact & Support
- Technical issues: Document in project issue tracker
- Client questions: Schedule review meetings as needed
- Post-launch monitoring: 48 hours active monitoring recommended
