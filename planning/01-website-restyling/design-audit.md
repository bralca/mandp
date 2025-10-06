# Design System Audit: Medical & Psychology Website

## Color Palette Analysis

### Primary Colors (from css/main.css & css/styles.css)

**Brand Colors:**
- Primary Blue: `#3399FF` (buttons, links, accents)
- Primary Purple: `#9c27b0` (styles.css - links)

**Text Colors:**
- Dark Text: `#25383B` (main.css - headings, body)
- Dark Text Alt: `#333` (main.css)
- Medium Gray: `#777` (main.css - secondary text)
- Light Gray: `#999` (main.css - muted text)
- Light Text: `#d3d3d3` (styles.css - body on dark bg)
- Very Light: `#eee` (styles.css)
- Black: `#111` (styles.css)
- White: `#fff`

**Background Colors:**
- Dark Background: `#282828` (styles.css - body)
- Dark Alt 1: `#222` (styles.css - sections)
- Dark Alt 2: `#2d2d2d` (styles.css - footer)
- Dark Alt 3: `#1d1d1d` (styles.css - modal)
- Dark Alt 4: `#36333d` (styles.css - form controls)
- Light Background: `#fff`
- Light Gray BG: `rgba(144, 144, 144, 0.075)` (main.css)
- Medium Gray BG: `#ccc` (styles.css)
- Light Button BG: `#f2f2f2` (styles.css)

**Button/Interactive States:**
- Button Hover 1: `#2f474b` (main.css)
- Button Hover 2: `#1b292b` (main.css)
- Button Hover 3: `#63c1ae` (main.css - teal)
- Button Hover 4: `#45ad97` (main.css - teal dark)

**Borders:**
- Border Light: `rgba(144, 144, 144, 0.25)`
- Border White: `#fff`
- Border Light Gray: `#ededed`
- Border Primary: `#3399FF`

**CEJRI Specific (from banners):**
- Banner Blue: `#2a95be`
- Button Blue: `#00c3ff`
- Button Hover: `#47b2ff`

### Conflicts Identified:
- Two different link colors: `#3399FF` (main.css) vs `#9c27b0` (styles.css)
- Inconsistent dark backgrounds: multiple shades (#282828, #222, #2d2d2d, #1d1d1d)
- No unified color system between the two frameworks

---

## Typography Analysis

### Font Families

**From css/styles.css:**
- Body/Headings: `'Questrial', 'Helvetica Neue', Arial, sans-serif`
- Cursive: `'Dancing Script', cursive` (for decorative headings)

**From css/main.css:**
- Body: `'Raleway', sans-serif`
- Headings: `'Raleway', sans-serif` (400, 500, 700 weights)

**Google Fonts Imports:**
- styles.css line 8: `@import url(https://fonts.googleapis.com/css?family=Questrial);` ✅ HTTPS
- styles.css line 9: `@import url(http://fonts.googleapis.com/css?family=Dancing+Script:700);` ❌ HTTP
- main.css line 3: `@import url("https://fonts.googleapis.com/css?family=Raleway:400,500,700");` ✅ HTTPS

### Font Sizes (from styles.css)
- Paragraph: `17px` (line-height: 1.7)
- Icon Large: `50px` (mobile: `1rem`, tablet: `80px`)
- Header H1: `2rem` (mobile) / `5rem` (tablet+)
- Header P: `1.3rem` (mobile) / `18px` (tablet+)
- Form Control: `14px`
- Button XL: `1rem`

### Font Weights
- Normal: 400
- Medium: 500
- Bold: 600, 700

### Conflicts Identified:
- Two different font systems: Questrial (styles.css) vs Raleway (main.css)
- Dancing Script HTTP import needs HTTPS
- No consistent font sizing system

---

## Spacing Analysis

### Padding Values (common patterns)
- Small: `5px`, `6px 12px`
- Medium: `15px`, `15px 30px`
- Large: `50px 0`, `50px 15px`
- XL: `70px 0`, `100px 0`

### Margin Values (common patterns)
- Small: `15px`, `20px`
- Medium: `0 auto 20px`
- Large: `50px auto 0`

### Section Padding
- Default section: `70px 0` (styles.css)
- Large section: `100px 0` (styles.css - tablet+)
- Aside: `50px 0`
- Footer: `15px`

### Conflicts Identified:
- No consistent spacing scale
- Mixed use of px and viewport units
- Inconsistent section padding between frameworks

---

## Responsive Breakpoints

### From css/main.css:
- Max-width: 1680px
- Max-width: 1280px
- Max-width: 980px
- Max-width: 736px
- Max-width: 480px

### From css/styles.css:
- Max-width: 480px
- Min-width: 768px
- Min-width: 992px

### Conflicts Identified:
- Different breakpoint systems between frameworks
- Need unified mobile-first breakpoints

---

## Recommendations for CSS Variables

### Proposed Color Variables:
```css
--color-primary: #3399FF;
--color-primary-hover: #2a95be;
--color-accent: #00c3ff;

--color-text-dark: #25383B;
--color-text-medium: #777;
--color-text-light: #999;
--color-text-white: #fff;

--color-bg-light: #fff;
--color-bg-dark: #282828;
--color-bg-gray: rgba(144, 144, 144, 0.075);

--color-border-light: rgba(144, 144, 144, 0.25);
--color-border-primary: #3399FF;
```

### Proposed Typography Variables:
```css
--font-primary: 'Raleway', -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, sans-serif;
--font-heading: 'Raleway', -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, sans-serif;
--font-decorative: 'Dancing Script', cursive;

--font-size-base: 17px;
--font-size-small: 14px;
--font-size-large: 20px;
--font-size-h1: 2.5rem;
--font-size-h2: 2rem;
--font-size-h3: 1.5rem;

--font-weight-normal: 400;
--font-weight-medium: 500;
--font-weight-bold: 700;

--line-height-base: 1.7;
--line-height-tight: 1.2;
```

### Proposed Spacing Variables:
```css
--spacing-xs: 5px;
--spacing-sm: 15px;
--spacing-md: 30px;
--spacing-lg: 50px;
--spacing-xl: 70px;
--spacing-2xl: 100px;
```

### Proposed Breakpoints:
```css
--breakpoint-mobile: 480px;
--breakpoint-tablet: 768px;
--breakpoint-desktop: 1024px;
--breakpoint-wide: 1280px;
```

---

**Audit Date:** 2025-10-06
**Status:** Ready for CSS Variable Implementation
