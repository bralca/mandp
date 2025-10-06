# Medical & Psychology Design System Documentation
## Modern Healthcare Design Language - 2025

---

## 🎨 Overview

This document defines the complete design system for the Medical & Psychology website restyling project. It establishes a modern, professional, and accessible visual language that balances healthcare credibility with contemporary web design trends.

**Design Philosophy:**
- Clean, modern aesthetics with organic shapes
- Professional yet approachable
- Healthcare-focused color palette (blues, teals, greens)
- Emphasis on readability and accessibility
- Smooth, meaningful animations
- Mobile-first responsive design

---

## 🎯 Color System

### Primary Palette (Warm Healthcare)

```css
/* Primary Colors */
--color-primary: #2563eb;        /* Blue 600 - Main brand color */
--color-primary-light: #3b82f6;  /* Blue 500 - Lighter variant */
--color-primary-dark: #1e40af;   /* Blue 700 - Darker variant */

/* Secondary Colors */
--color-secondary: #059669;       /* Green 600 - Healthcare/growth */
--color-secondary-light: #10b981; /* Green 500 */
--color-secondary-dark: #047857;  /* Green 700 */

/* Accent Colors */
--color-accent: #f59e0b;          /* Amber 500 - Warmth/energy */
--color-accent-light: #fbbf24;    /* Amber 400 */
--color-accent-dark: #d97706;     /* Amber 600 */
```

### Neutral Colors

```css
/* Text Colors */
--color-text-primary: #1e293b;    /* Slate 800 - Main text */
--color-text-secondary: #475569;  /* Slate 600 - Secondary text */
--color-text-tertiary: #94a3b8;   /* Slate 400 - Muted text */

/* Background Colors */
--color-bg-primary: #ffffff;      /* White - Main background */
--color-bg-secondary: #f8fafc;    /* Slate 50 - Alt background */
--color-bg-tertiary: #f1f5f9;     /* Slate 100 - Sections */

/* Border Colors */
--color-border-light: #e2e8f0;    /* Slate 200 */
--color-border-medium: #cbd5e1;   /* Slate 300 */
--color-border-dark: #94a3b8;     /* Slate 400 */
```

### Gradient Palette

**Primary Blue Gradient (CEJRI Section):**
```css
background: linear-gradient(135deg,
  #06b6d4 0%,     /* Cyan */
  #0891b2 15%,    /* Teal */
  #3b82f6 35%,    /* Light blue */
  #2563eb 50%,    /* Medium blue */
  #1d4ed8 65%,    /* Primary blue */
  #1e40af 80%,    /* Dark blue */
  #0c4a6e 100%);  /* Navy blue-teal */
background-size: 300% 300%;
animation: gradientShift 16s ease infinite;
```

**Accent Gradient (Buttons, CTAs):**
```css
background: linear-gradient(135deg,
  var(--color-primary) 0%,
  var(--color-primary-dark) 100%);
```

**Multi-color Gradient (Decorative Elements):**
```css
background: linear-gradient(135deg,
  rgba(37, 99, 235, 0.4) 0%,    /* Blue */
  rgba(5, 150, 105, 0.4) 50%,   /* Green */
  rgba(251, 146, 60, 0.4) 100%); /* Orange */
```

---

## 📐 Spacing System

### Base Unit: 0.25rem (4px)

```css
--space-1: 0.25rem;   /* 4px */
--space-2: 0.5rem;    /* 8px */
--space-3: 0.75rem;   /* 12px */
--space-4: 1rem;      /* 16px */
--space-5: 1.25rem;   /* 20px */
--space-6: 1.5rem;    /* 24px */
--space-8: 2rem;      /* 32px */
--space-10: 2.5rem;   /* 40px */
--space-12: 3rem;     /* 48px */
--space-16: 4rem;     /* 64px */
--space-20: 5rem;     /* 80px */
--space-24: 6rem;     /* 96px */
```

**Usage Guidelines:**
- Section padding: `--space-20` to `--space-24`
- Card padding: `--space-6` to `--space-8`
- Element gaps: `--space-4` to `--space-6`
- Small gaps: `--space-2` to `--space-3`

---

## 🔤 Typography System

### Font Families

```css
--font-primary: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto,
                "Helvetica Neue", Arial, sans-serif;
--font-display: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto,
                "Helvetica Neue", Arial, sans-serif;
```

### Font Sizes (Responsive with clamp)

```css
--text-xs: 0.75rem;      /* 12px */
--text-sm: 0.875rem;     /* 14px */
--text-base: 1rem;       /* 16px */
--text-lg: 1.125rem;     /* 18px */
--text-xl: 1.25rem;      /* 20px */
--text-2xl: 1.5rem;      /* 24px */
--text-3xl: 1.875rem;    /* 30px */
--text-4xl: 2.25rem;     /* 36px */
--text-5xl: 3rem;        /* 48px */
--text-6xl: 3.75rem;     /* 60px */
```

### Font Weights

```css
--font-weight-normal: 400;
--font-weight-medium: 500;
--font-weight-semibold: 600;
--font-weight-bold: 700;
--font-weight-extrabold: 800;
```

### Line Heights

```css
--line-height-tight: 1.25;
--line-height-normal: 1.5;
--line-height-relaxed: 1.75;
--line-height-loose: 2;
```

### Letter Spacing

```css
--letter-spacing-tight: -0.025em;
--letter-spacing-normal: 0;
--letter-spacing-wide: 0.025em;
```

### Typography Usage Examples

**Hero Titles:**
```css
font-size: clamp(2rem, 6vw, 3.5rem);
font-weight: var(--font-weight-bold);
line-height: var(--line-height-tight);
letter-spacing: var(--letter-spacing-tight);
```

**Section Titles:**
```css
font-size: var(--text-5xl);
color: var(--color-primary);
margin-bottom: var(--space-8);
```

**Body Text:**
```css
font-size: var(--text-lg);
line-height: var(--line-height-relaxed);
color: var(--color-text-secondary);
```

---

## 🎭 Border Radius System

```css
--radius-sm: 0.25rem;     /* 4px - Small elements */
--radius-md: 0.375rem;    /* 6px - Default */
--radius-lg: 0.5rem;      /* 8px - Buttons */
--radius-xl: 0.75rem;     /* 12px - Cards */
--radius-2xl: 1rem;       /* 16px - Large cards */
--radius-3xl: 1.5rem;     /* 24px - Sections */
--radius-full: 9999px;    /* Full rounded */
```

**Organic Blob Shapes (Images):**
```css
/* First variant */
border-radius: 30% 70% 70% 30% / 30% 30% 70% 70%;

/* Second variant (alternate) */
border-radius: 70% 30% 30% 70% / 60% 40% 60% 40%;
```

---

## 🌟 Shadow System

### Standard Shadows

```css
--shadow-sm: 0 1px 2px 0 rgb(0 0 0 / 0.05);
--shadow-md: 0 4px 6px -1px rgb(0 0 0 / 0.1),
             0 2px 4px -2px rgb(0 0 0 / 0.1);
--shadow-lg: 0 10px 15px -3px rgb(0 0 0 / 0.1),
             0 4px 6px -4px rgb(0 0 0 / 0.1);
--shadow-xl: 0 20px 25px -5px rgb(0 0 0 / 0.1),
             0 8px 10px -6px rgb(0 0 0 / 0.1);
--shadow-2xl: 0 25px 50px -12px rgb(0 0 0 / 0.25);
```

### Drop Shadows (for organic shapes)

```css
/* Default state */
filter: drop-shadow(0 20px 60px rgba(0, 0, 0, 0.25));

/* Hover state */
filter: drop-shadow(0 30px 80px rgba(0, 0, 0, 0.35));
```

### Layered Shadows (Premium elements)

```css
box-shadow:
  0 20px 60px -15px rgba(0, 0, 0, 0.3),
  0 0 0 1px rgba(255, 255, 255, 0.1),
  inset 0 1px 0 0 rgba(255, 255, 255, 0.2);
```

---

## ⚡ Animation System

### Timing Functions

```css
--transition-base: 0.3s ease-in-out;
--transition-fast: 0.15s ease-in-out;
--transition-slow: 0.5s ease-in-out;
```

### Custom Easing

```css
cubic-bezier(0.4, 0, 0.2, 1)  /* Smooth, professional */
```

### Keyframe Animations

**Gradient Shift (Background animations):**
```css
@keyframes gradientShift {
  0%, 100% {
    background-position: 0% 50%;
  }
  50% {
    background-position: 100% 50%;
  }
}
/* Usage: animation: gradientShift 16s ease infinite; */
```

**Float Dynamic (Hero blobs):**
```css
@keyframes floatDynamic {
  0%, 100% {
    transform: translate(0, 0) scale(1);
  }
  25% {
    transform: translate(50px, -40px) scale(1.1);
  }
  50% {
    transform: translate(-30px, 50px) scale(0.9);
  }
  75% {
    transform: translate(40px, 30px) scale(1.05);
  }
}
/* Usage: animation: floatDynamic 20s ease-in-out infinite; */
```

**Pulse (Attention elements):**
```css
@keyframes pulse {
  0%, 100% {
    transform: scale(1);
    box-shadow: 0 20px 25px -5px rgb(0 0 0 / 0.1);
  }
  50% {
    transform: scale(1.05);
    box-shadow: 0 25px 30px -5px rgb(0 0 0 / 0.15);
  }
}
/* Usage: animation: pulse 3s ease-in-out infinite; */
```

**Card Float (Glassmorphism cards):**
```css
@keyframes cardFloat {
  0%, 100% {
    transform: translateY(0px);
  }
  50% {
    transform: translateY(-10px);
  }
}
/* Usage: animation: cardFloat 6s ease-in-out infinite; */
```

---

## 🧩 Component Patterns

### 1. Hero Section

**Structure:**
```html
<header id="first">
  <div class="hero-bg-accent-1"></div>
  <div class="hero-bg-accent-2"></div>
  <div class="hero-bg-grid"></div>
  <div class="header-content">
    <div class="slider-inner">
      <h1>Main Title</h1>
      <h4 class="subtitles">Subtitle</h4>
      <hr>
      <a href="#main" class="btn btn-primary btn-xl">CTA</a>
    </div>
  </div>
  <img src="bg.jpg" class="bg" alt="Background">
</header>
```

**Key Styles:**
- Multiple layered background blobs with animations
- Large, centered text with gradient underlining
- Semi-transparent background image overlay
- Floating animated elements
- Responsive typography using clamp()

### 2. Glassmorphism Cards (CEJRI Section)

**Structure:**
```html
<section id="banner">
  <div class="banner-content">
    <h1 class="title">Title</h1>
    <p>Description</p>
    <ul class="actions">
      <li><a href="#" class="button big special">CTA →</a></li>
    </ul>
  </div>
</section>
```

**Key Styles:**
```css
.banner-content {
  background: rgba(255, 255, 255, 0.15);
  backdrop-filter: blur(20px) saturate(180%);
  -webkit-backdrop-filter: blur(20px) saturate(180%);
  border-radius: var(--radius-3xl);
  border: 1px solid rgba(255, 255, 255, 0.3);
  box-shadow:
    0 8px 32px 0 rgba(31, 38, 135, 0.37),
    inset 0 1px 0 0 rgba(255, 255, 255, 0.5);
  animation: cardFloat 6s ease-in-out infinite;
}
```

**Background:**
- Animated gradient with cyan → blue → navy range
- Floating orbs with blur effects
- 300% background size for visible movement
- 16s animation duration

### 3. Content Sections with Organic Images

**Structure:**
```html
<section id="main" class="wrapper">
  <div class="container">
    <h1 class="title">Section Title</h1>

    <div class="content-section">
      <div class="content-text">
        <h4>Subsection</h4>
        <p>Content...</p>
      </div>
      <a href="#" class="image-detail">
        <img src="image.png" alt="Description" />
      </a>
    </div>
  </div>
</section>
```

**Key Features:**
- CSS Grid layout: 2 columns on desktop, stacked on mobile
- Automatic alternating layout using `nth-of-type`
- Organic blob shapes using asymmetric border-radius
- Gradient glow effect on hover
- 4:3 aspect ratio images
- Vertically centered alignment

**Image Blob Styles:**
```css
/* First variant */
border-radius: 30% 70% 70% 30% / 30% 30% 70% 70%;

/* Second variant (even sections) */
border-radius: 70% 30% 30% 70% / 60% 40% 60% 40%;

/* Hover effects */
transform: translateY(-8px);
filter: drop-shadow(0 30px 80px rgba(0, 0, 0, 0.35));
```

### 4. Floating Top Banner

**Structure:**
```html
<div class="top-bar" id="topBanner">
  <div class="top-bar-content">
    <div class="top-bar-message">
      <div class="top-bar-icon">📚</div>
      <div class="top-bar-text">
        <h1>Message</h1>
      </div>
    </div>
    <div class="top-bar-actions">
      <button class="btn-banner">CTA →</button>
      <button class="top-bar-close">✕</button>
    </div>
  </div>
</div>
```

**Key Features:**
- Glassmorphism effect with backdrop-filter
- Margin on desktop, full-width on mobile
- Hides on scroll, reappears after 1s of no scroll
- Session-based dismissal using sessionStorage
- Smooth slide-up animation on close

### 5. Buttons

**Primary Button:**
```css
.btn-primary {
  background: linear-gradient(135deg,
    var(--color-primary) 0%,
    var(--color-primary-dark) 100%);
  color: var(--color-white);
  padding: var(--space-5) var(--space-10);
  border-radius: var(--radius-full);
  box-shadow: var(--shadow-md);
  transition: all var(--transition-base);
}

.btn-primary:hover {
  transform: translateY(-2px);
  box-shadow: var(--shadow-lg);
}
```

**Glassmorphism Button (on gradient backgrounds):**
```css
.button.big.special {
  background: rgba(255, 255, 255, 0.95);
  color: var(--color-primary);
  border-radius: var(--radius-full);
  box-shadow: 0 10px 30px rgba(0, 0, 0, 0.2);
  border: 2px solid rgba(255, 255, 255, 0.5);
}

.button.big.special:hover {
  transform: translateY(-4px) scale(1.05);
  box-shadow: 0 15px 40px rgba(255, 255, 255, 0.4);
}
```

---

## 📱 Responsive Design Guidelines

### Breakpoints

```css
/* Mobile First Approach */
@media (min-width: 640px)  { /* sm */ }
@media (min-width: 768px)  { /* md */ }
@media (min-width: 1024px) { /* lg */ }
@media (min-width: 1280px) { /* xl */ }
```

### Layout Patterns

**Mobile (< 768px):**
- Single column layout
- Full-width banners
- Stacked content sections
- Reduced spacing
- Smaller typography

**Tablet (768px - 1024px):**
- 2-column grid for content sections
- Moderate spacing
- Medium typography

**Desktop (> 1024px):**
- Full grid layouts
- Maximum spacing
- Large typography
- Enhanced animations
- Floating elements

### Responsive Typography

Always use `clamp()` for smooth responsive scaling:

```css
font-size: clamp(min-size, preferred-size, max-size);

/* Example */
h1 {
  font-size: clamp(2rem, 6vw, 3.5rem);
}
```

---

## 🎨 Design Patterns Summary

### Visual Hierarchy

1. **Primary attention**: Glassmorphism cards, hero sections
2. **Secondary attention**: Organic image shapes
3. **Tertiary attention**: Body content, supporting text

### Animation Principles

1. **Purpose**: Every animation should have meaning
2. **Duration**:
   - Fast interactions: 0.15s - 0.3s
   - Attention elements: 3s - 6s
   - Ambient backgrounds: 15s - 25s
3. **Easing**: Use cubic-bezier for professional feel
4. **Performance**: Prefer `transform` and `opacity` changes

### Accessibility

1. **Color contrast**: Minimum 4.5:1 for body text
2. **Focus states**: Always visible
3. **Motion**: Respect `prefers-reduced-motion`
4. **Touch targets**: Minimum 44x44px
5. **Alt text**: Required for all images

---

## 🔧 Implementation Checklist

When applying this design system to a new page:

- [ ] Include `modern-design-system.css`
- [ ] Use CSS custom properties for all colors
- [ ] Apply organic blob shapes to images
- [ ] Implement alternating grid layouts
- [ ] Add glassmorphism effects to featured sections
- [ ] Use gradient backgrounds for hero/banner sections
- [ ] Apply proper spacing using spacing scale
- [ ] Use clamp() for responsive typography
- [ ] Add hover animations to interactive elements
- [ ] Implement proper shadow hierarchy
- [ ] Test on mobile, tablet, desktop
- [ ] Verify color contrast ratios
- [ ] Add proper alt text to images

---

## 🎯 Key Differentiators

What makes this design system unique:

1. **Organic Shapes**: Asymmetric blob shapes instead of standard rectangles
2. **Glassmorphism**: Modern frosted glass effects for depth
3. **Dynamic Gradients**: Animated multi-color gradients
4. **Healthcare Colors**: Professional blue/teal/green palette
5. **Smooth Animations**: Cubic-bezier easing for premium feel
6. **Layered Depth**: Multiple shadow layers and blur effects

---

## 📚 Resources

**CSS File:** `/css/modern-design-system.css`
**HTML Example:** `/index-modern.html`
**Color Palette:** Option B (Warm Healthcare)
**Browser Support:** Modern browsers (Chrome, Firefox, Safari, Edge)

---

**Version:** 1.0
**Last Updated:** 2025-01-06
**Author:** Medical & Psychology Design Team
