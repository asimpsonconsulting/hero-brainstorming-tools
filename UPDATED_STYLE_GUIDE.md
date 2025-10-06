# UPDATED Style Guide - Based on Hero Brainstorming Tool Implementation

## 3. Typography

### Primary Typeface
**Font Name:** Inter
- **Where to use:** All text elements (headings, body text, UI elements, navigation)
- **Weights available:** Light (300), Regular (400), Medium (500), Semi-Bold (600), Bold (700), Extra Bold (800)
- **Web-safe alternative:** system-ui, -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, sans-serif

**Complete Font Stack:** `'Inter', system-ui, -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, sans-serif`

### Hero Section Typography Scale (3 Tested Variations)

#### **Version 1: Modern SaaS Style**
- **Hero Headline:** 56px, 700 weight, line-height: 1.1, gradient text
- **Sub-headline:** 24px, 400 weight, line-height: 1.4
- **Body Copy:** 18px, 400 weight, line-height: 1.6
- **Eyebrow:** 12px, 600 weight, uppercase, letter-spacing: 1.5px
- **CTA Button:** 18px, 600 weight

#### **Version 2: Bold & Minimal**
- **Hero Headline:** 64px, 800 weight, line-height: 1.05, solid color
- **Sub-headline:** 28px, 500 weight, line-height: 1.3
- **Body Copy:** 20px, 400 weight, line-height: 1.7
- **Eyebrow:** 14px, 700 weight, uppercase, letter-spacing: 2px
- **CTA Button:** 20px, 700 weight

#### **Version 3: Clean & Professional**
- **Hero Headline:** 48px, 700 weight, line-height: 1.15, solid color
- **Sub-headline:** 22px, 400 weight, line-height: 1.5
- **Body Copy:** 17px, 400 weight, line-height: 1.65
- **Eyebrow:** 13px, 600 weight, uppercase, letter-spacing: 1.2px
- **CTA Button:** 17px, 600 weight

### Navigation Typography
- **Main Nav Links:** 15px, 700 weight (updated from 500)
- **Nav Eyebrows:** 9px, 400 weight, uppercase, letter-spacing: -0.3px (condensed)
- **Nav CTA:** 14px, 600 weight

### Typography Guidelines
**DO:**
- **Test across light + dark themes** - readability varies significantly
- **Use gradient text for headlines** in Modern SaaS style (Version 1)
- **Maintain baseline alignment** when mixing eyebrows and main text
- **Use condensed letter-spacing** (-0.3px) for micro-text eyebrows
- **Reserve 800 weight** for high-impact headlines (Bold & Minimal style)

**DON'T:**
- Use gradient text on dark backgrounds (readability issues)
- Go below 9px for any text (even eyebrows)
- Mix different eyebrow patterns in same navigation
- Ignore line-height differences between versions

---

## 4. Color Palette

### Light Theme Colors (Parts 1 & 2)
*(Same as your existing palette)*

### **NEW: Dark Theme Colors (Part 3)**

#### **Dark Backgrounds (Customizable)**
- **Primary Dark:** #1a1a1a (recommended default)
- **Solid Black:** #000000 (high contrast)
- **Charcoal:** #2d2d2d (softer alternative)
- **Dark Blue:** #1e1e2e (branded dark)
- **Custom:** User-definable hex values

#### **Dark Theme Text Colors**
- **Primary Text:** #ffffff (white)
- **Secondary Text:** #e5e7eb (gray-200)
- **Muted Text:** #d1d5db (gray-300)
- **Eyebrow Text:** #f97316 (brand orange)
- **Nav Eyebrows:** #9ca3af (gray-400)

#### **Dark Theme Interactive Elements**
- **Glass Navigation:** rgba(0, 0, 0, 0.3) with backdrop-filter: blur(10px)
- **Glass TOC:** rgba(255, 255, 255, 0.1) with backdrop-filter: blur(10px)
- **Borders:** rgba(255, 255, 255, 0.1) to rgba(255, 255, 255, 0.2)
- **Hover States:** rgba(255, 255, 255, 0.1)
- **Active States:** rgba(249, 115, 22, 0.2)

#### **Dark Theme Gradients (Headlines)**
- **Primary Headline:** linear-gradient(135deg, #ffffff 0%, #f97316 100%)
- **Alternative:** Use solid #ffffff for better readability
- **CTA Buttons:** Keep same gradients as light theme (still readable)

### **NEW: Glass Effect Specifications**
```css
/* Glass Navigation (Dark Theme) */
background: rgba(0, 0, 0, 0.3);
backdrop-filter: blur(10px);
border-bottom: 1px solid rgba(255, 255, 255, 0.1);

/* Glass TOC Panel */
background: rgba(255, 255, 255, 0.1);
backdrop-filter: blur(10px);
border: 1px solid rgba(255, 255, 255, 0.2);
```

### Updated Color Usage Guidelines

**DO:**
- **Test all colors on both light AND dark backgrounds**
- **Use glass effects** for overlays on dark themes
- **Maintain brand orange** (#f97316) as accent across light/dark
- **Use rgba with low opacity** for dark theme cards/panels
- **Apply backdrop-filter: blur()** for modern glass effects

**DON'T:**
- Use pure gradients for headlines on dark backgrounds
- Apply same contrast ratios from light to dark (adjust accordingly)
- Forget to test CTA button readability on various dark backgrounds
- Use solid blacks/whites without considering glass effects

### **NEW: Accessibility for Dark Themes**
- **White text on #1a1a1a:** 15.3:1 contrast ratio (AAA)
- **Orange (#f97316) on dark:** Sufficient for accent use
- **Glass effects:** Test readability case-by-case
- **Custom dark colors:** Require contrast validation

---

## **NEW: Multi-Theme Design Strategy**

### **Design System Approach:**
1. **Start with light theme** messaging (Part 2)
2. **Validate dark theme** readability (Part 3)
3. **Compare side-by-side** for optimal contrast and impact
4. **Export screenshots** for stakeholder review across themes

### **Theme-Specific Optimizations:**
- **Light theme:** Full gradient usage, subtle shadows
- **Dark theme:** Glass effects, reduced gradients, higher contrast
- **Navigation:** Consistent structure, theme-appropriate styling
- **TOC elements:** Floating on light, glass panels on dark

This updated style guide reflects your **actual implemented design system** from the Hero Brainstorming tools! 🎯
