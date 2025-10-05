# Product Requirements Document: Medical & Psychology Website Restyling

## 1. Overview & Vision

This project aims to modernize the Medical & Psychology institute website, originally developed in 2015, transforming it into a contemporary, professional web presence while maintaining its simple HTML structure. The restyling will consolidate inconsistent CSS frameworks, implement modern layout techniques, optimize performance, and improve the brand hierarchy between Medical & Psychology (parent company) and CEJRI (Centro Jonico Riabilitativo - the well-known rehabilitation center). The modernization will enhance user experience, improve conversion potential, and establish a cohesive visual identity without introducing complex frameworks or technologies.

## 2. Problem Statement

The current website suffers from several critical issues:
- **Technical Debt**: Built with outdated technologies (Bootstrap 3, jQuery plugins from 2015, legacy IE8/9 polyfills)
- **Inconsistent Design**: Mixes two different CSS frameworks (TEMPLATED Retrospect and BootstrapZero Landing Zero) creating visual inconsistency
- **Performance Issues**: Large unoptimized images (16.4MB home.jpg), heavy JavaScript libraries, HTTP font imports
- **Poor Information Architecture**: CEJRI content isolated in separate folder despite being the primary brand customers recognize
- **Legacy Code Bloat**: Unnecessary polyfills, outdated animation libraries, deprecated responsive techniques
- **Security Concerns**: Mixed HTTP/HTTPS content, outdated dependencies

## 3. Target Users

### Primary User Personas

**Persona 1: Prospective Patients & Families**
- Age: 30-65 years old
- Needs: Information about rehabilitation services, trustworthy medical institute, easy contact methods
- Pain Points: Current site feels dated, unclear relationship between Medical & Psychology and CEJRI
- Goals: Find quality rehabilitation services, understand offerings, contact for appointments

**Persona 2: Healthcare Referral Professionals**
- Age: 28-55 years old
- Needs: Professional presentation, clear service descriptions, credentials and certifications
- Pain Points: Outdated website reduces perceived credibility
- Goals: Refer patients to reputable facilities, verify service quality

**Persona 3: Mobile Users**
- Device: Smartphones and tablets
- Needs: Fast loading times, responsive design, easy navigation
- Pain Points: Heavy page loads, outdated mobile experience
- Goals: Quick access to information on-the-go

## 4. Core Requirements

### 4.1 Functional Requirements

**Design System Consolidation**
- Consolidate TEMPLATED Retrospect and BootstrapZero Landing Zero into single cohesive design system
- Implement CSS custom properties (variables) for colors, spacing, typography, and theming
- Create consistent component library across all 5 HTML pages

**Modern Layout Architecture**
- Replace Bootstrap 3 float-based grid with CSS Grid and Flexbox
- Maintain current visual structure and layout hierarchy
- Ensure responsive design across all breakpoints (mobile, tablet, desktop)

**Typography & Fonts**
- Retain current fonts: Dancing Script, Questrial, Raleway
- Update all Google Fonts imports from HTTP to HTTPS
- Implement system font fallbacks for performance

**Brand Integration**
- Restructure site to highlight CEJRI as primary brand while showing Medical & Psychology as parent organization
- Integrate CEJRI content into main site structure (remove separate folder isolation)
- Create clear brand hierarchy in navigation and content sections

**Interactive Elements**
- Remove jQuery plugins: wow.js, prettyPhoto, isotope, owl carousel
- Replace with minimal modern CSS animations and vanilla JavaScript
- Keep interactions simple and purposeful

**Footer & Integrations**
- Maintain existing footer links: Iubenda privacy, Whistleblowing portal, Google Drive documentation
- Modernize footer styling while preserving functionality
- Keep existing Google Analytics setup (UA-89376496-1)

### 4.2 Non-Functional Requirements

**Performance Requirements**
- Remove all legacy browser support (IE8/9 polyfills: html5shiv.js, respond.min.js)
- Optimize images: implement WebP/AVIF formats with fallbacks
- Implement responsive image srcsets for different screen sizes
- Add lazy loading for images to improve initial render time
- Reduce JavaScript payload by removing Bootstrap 3, jQuery, and outdated plugins
- Focus on practical optimizations without specific load time targets

**Code Quality Requirements**
- Maintain simple HTML structure (no complex frameworks)
- Use semantic HTML5 elements
- Ensure clean, maintainable CSS with modern best practices
- Implement vanilla JavaScript where needed (minimal dependencies)

**Security Requirements**
- All external resources loaded via HTTPS
- No mixed content warnings
- Maintain existing privacy and compliance integrations

**Compatibility Requirements**
- Modern browsers only (Chrome, Firefox, Safari, Edge - latest 2 versions)
- Fully responsive across mobile, tablet, desktop
- Progressive enhancement approach

## 5. User Stories & Acceptance Criteria

### Epic 1: Design System Modernization

**As a** website visitor
**I want** a visually consistent and modern website experience
**So that** I trust the medical institute's professionalism and credibility

**Acceptance Criteria:**
- [ ] All pages use single unified CSS design system with CSS custom properties
- [ ] Color palette, spacing, and typography are consistent across all 5 HTML pages
- [ ] No visual remnants of conflicting TEMPLATED/BootstrapZero frameworks
- [ ] Design feels modern and professional (2024 standards)
- [ ] All fonts loaded via HTTPS with proper fallbacks

### Epic 2: Modern Layout Implementation

**As a** website visitor on any device
**I want** a responsive layout that adapts beautifully to my screen size
**So that** I can easily access information regardless of device

**Acceptance Criteria:**
- [ ] All layouts use CSS Grid and/or Flexbox (no Bootstrap 3 float-based grid)
- [ ] Visual structure maintained from original design
- [ ] Responsive breakpoints work smoothly on mobile, tablet, desktop
- [ ] No horizontal scrolling on any device size
- [ ] All 5 HTML pages (index.html, santeufemia.html, maintenance.html, portage.html, other-projects.html) follow consistent layout patterns

### Epic 3: Brand Hierarchy & Information Architecture

**As a** prospective patient
**I want** to clearly understand that CEJRI is the rehabilitation center managed by Medical & Psychology
**So that** I can easily find the services I need and trust the organization

**Acceptance Criteria:**
- [ ] CEJRI prominently featured on main site with clear relationship to parent company
- [ ] CEJRI content integrated into main site structure (not isolated in separate folder)
- [ ] Navigation clearly shows Medical & Psychology as parent organization
- [ ] Conversion goals maintained (patient contact/information requests)
- [ ] Call-to-action hierarchy redesigned to reflect brand integration

### Epic 4: Performance Optimization

**As a** mobile user with limited bandwidth
**I want** fast page load times
**So that** I can quickly access information without frustration

**Acceptance Criteria:**
- [ ] All legacy IE8/9 polyfills removed (html5shiv.js, respond.min.js)
- [ ] jQuery, Bootstrap 3, and outdated plugins removed
- [ ] Large images optimized (16.4MB home.jpg, 1.7MB background-main.png reduced significantly)
- [ ] WebP/AVIF formats implemented with appropriate fallbacks
- [ ] Responsive image srcsets implemented for all major images
- [ ] Lazy loading implemented for below-the-fold images
- [ ] Modern CSS animations replace WOW.js scroll animations
- [ ] Overall page weight reduced by at least 70%

### Epic 5: Simplified Interactions

**As a** website visitor
**I want** smooth, simple animations and interactions
**So that** the site feels modern without being overwhelming

**Acceptance Criteria:**
- [ ] All jQuery animation plugins removed (wow.js, prettyPhoto, isotope, owl carousel)
- [ ] Modern CSS animations implemented for key interactions
- [ ] Vanilla JavaScript used for any required interactive features
- [ ] Animations are subtle and purposeful (not excessive)
- [ ] No JavaScript errors in browser console
- [ ] Interactions work smoothly across all supported browsers

### Epic 6: Footer & Third-Party Integrations

**As a** website administrator
**I want** all existing integrations maintained with modern styling
**So that** we remain compliant and functional while looking current

**Acceptance Criteria:**
- [ ] Iubenda privacy policy link maintained and styled
- [ ] Whistleblowing portal link maintained and styled
- [ ] Google Drive documentation link maintained and styled
- [ ] Google Analytics (UA-89376496-1) continues tracking properly
- [ ] Footer styling modernized to match new design system
- [ ] All footer links accessible and working

## 6. Technical Considerations

### Technology Stack
- **HTML**: Semantic HTML5, maintain simple structure
- **CSS**: Modern CSS3 with Grid, Flexbox, Custom Properties, no preprocessors required
- **JavaScript**: Vanilla JS (ES6+), minimal dependencies
- **Images**: WebP/AVIF with JPG/PNG fallbacks, lazy loading
- **Fonts**: Google Fonts (HTTPS), system font fallbacks

### Architecture Approach
- Static site structure maintained (no build tools required for core functionality)
- Optional: Simple image optimization script (if easy to implement)
- Progressive enhancement strategy
- Mobile-first CSS approach

### Integration Points
**Files to Modernize:**
- index.html - Main landing page structure
- santeufemia.html - Detail page
- maintenance.html - Detail page
- portage.html - Detail page
- other-projects.html - Detail page
- css/main.css - Consolidate and modernize
- css/styles.css - Consolidate and modernize
- js/main.js - Rewrite with vanilla JavaScript

**Files to Remove:**
- js/jquery.min.js
- js/bootstrap.min.js
- js/wow.js
- js/jquery.easing.min.js
- js/ie/html5shiv.js
- js/ie/respond.min.js
- css/bootstrap.min.css (Bootstrap 3)

**CEJRI Integration:**
- Evaluate cejri/ subdirectory content
- Integrate key CEJRI content into main site navigation
- Maintain visual consistency between parent and CEJRI sections

### Browser Support
- Chrome (latest 2 versions)
- Firefox (latest 2 versions)
- Safari (latest 2 versions)
- Edge (latest 2 versions)
- Mobile browsers (iOS Safari, Chrome Mobile)

## 7. Success Metrics

### Performance Metrics
- **Page Weight Reduction**: Target 70%+ reduction in total page size
- **Image Optimization**: home.jpg reduced from 16.4MB to <500KB
- **JavaScript Payload**: Reduced by 80%+ (removal of jQuery, Bootstrap, plugins)
- **First Contentful Paint**: Improved by at least 50%
- **Lighthouse Score**: Achieve 90+ in Performance category

### User Experience Metrics
- **Mobile Usability**: Google Mobile-Friendly Test passes with no issues
- **Accessibility**: Maintain or improve accessibility scores
- **Cross-browser Compatibility**: Zero visual bugs across supported browsers
- **Page Load Success**: All resources load via HTTPS with no mixed content warnings

### Business Metrics
- **Bounce Rate**: Maintain or improve current bounce rate
- **Time on Site**: Increase by highlighting better content structure
- **Conversion Rate**: Maintain or improve patient contact inquiries
- **Brand Perception**: CEJRI brand recognition improved through better integration

### Quality Metrics
- **Code Consistency**: Single design system across all pages
- **Maintainability**: Reduced codebase complexity (fewer dependencies)
- **Standards Compliance**: Valid HTML5, modern CSS, ES6+ JavaScript
- **Visual Consistency**: Design system applied uniformly across all 5 pages

---

**Document Version:** 1.0
**Last Updated:** 2025-10-05
**Status:** Ready for Development
