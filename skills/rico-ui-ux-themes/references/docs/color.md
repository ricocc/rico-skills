# Color Optimization Guide

> For general optimization workflow, see SKILL.md. This guide focuses on color design decisions.

---

## First Principles of Color

**Color is not decoration, it's information.**

At Apple and Airbnb, color has three levels:

| Level | Purpose | Apple Example | Airbnb Example |
|-------|---------|---------------|----------------|
| **Brand Color** | Identity | iOS Blue | Airbnb Coral Red |
| **Functional Color** | Status Communication | Green = Success | Red = Warning |
| **Neutral Color** | Content Carrier | System Gray | Stone Gray |

**Core Question**: What information is this color conveying?

---

## Professional Color Decision Framework

### 1. Emotion First

**Ask first: What should the user feel?**

| Emotion | Hue Choice | Examples |
|---------|------------|----------|
| **Trust** | Blue, Cyan | Apple Pay, IBM |
| **Vitality** | Orange, Coral | Airbnb, Instagram |
| **Luxury** | Black, Gold | Apple Pro |
| **Warmth** | Warm Yellow, Peach | Notion, Warm Themes |
| **Professional** | Deep Blue, Charcoal | Enterprise SaaS |

**Anti-pattern**: Finance apps using orange (too playful), social apps using dark gray (too serious).

### 2. The Real Meaning of 60-30-10

**Not about area, but visual weight.**

- **60% Whitespace** — Let content breathe
- **30% Neutral Color** — Carry and connect
- **10% Accent Color** — Guide attention

**Common Mistake**: Using brand color for 30%, causing visual fatigue.

### 3. Contrast is Hierarchy

**Users should read by color importance.**

| Level | Contrast | Usage |
|-------|----------|-------|
| Primary Text | 7:1 (AAA) | Headlines, important content |
| Body Text | 4.5:1 (AA) | Main reading content |
| Secondary | 3:1 | Supporting info, labels |
| Disabled | 1.5:1 | Non-primary states |

**Apple Approach**: iOS text contrast strictly follows WCAG AAA, remaining clear even in bright environments.

---

## Color System Design

### Apple Color Philosophy

- **Semantic First**: Use semantic colors (label, secondaryLabel) rather than specific values
- **Dynamic Colors**: Light/dark mode auto-adapt, no need to maintain two sets
- **Blur Effects**: Use blur + tint rather than hard color blocks to distinguish layers

### Airbnb Color Philosophy

- **Photo First**: Brand color yields to content (property photos)
- **Clear Functions**: Success green, warning yellow, error red, action blue
- **Neutral Modern**: Background uses warm gray (Stone) rather than cool gray

### IBM Color Philosophy

- **Industrial Precision**: Every color has a precise purpose, no "random" colors
- **Carbon System**: 11-level grayscale, each level has a code (Gray 10-100)
- **Accessibility First**: All colors pass AAA contrast

---

## Dark Mode Design

### Core Principles

**Dark mode is not "inversion", it's "reconstruction".**

| Light Mode | Dark Mode |
|------------|-----------|
| Shadow indicates depth | Brightness indicates depth |
| Dark text | Light text (reduce font weight) |
| Saturated accent colors | Reduce saturation |
| Pure white background | Dark gray background (#000 is harsh) |

### IBM Carbon Dark Scheme

```css
/* IBM Carbon Dark Mode */
--cds-background: #161616;      /* Level 16 gray, not pure black */
--cds-background-hover: #1F1F1F;
--cds-layer-01: #262626;       /* Elevated layer */
--cds-layer-02: #393939;       /* Floating layer */
--cds-text-primary: #f4f4f4;    /* 90% white */
--cds-text-secondary: #c6c6c6;  /* 70% white */
```

### Apple iOS Dark Scheme

```css
/* Apple Semantic Colors */
--systemBackground: oklch(1 0 0);
--secondarySystemBackground: oklch(0.97 0 0);
--tertiarySystemBackground: oklch(0.94 0 0);
--systemGray: oklch(0.55 0 0);
```

---

## OKLCH Deep Dive

### Why Professional Designers Choose OKLCH

HSL Problem: At 50% lightness, yellow appears much brighter than blue.

OKLCH Advantages:
- **Perceptually Uniform**: Lightness changes are visually consistent
- **Chroma Adaptive**: Extreme lightness automatically reduces saturation
- **CSS Native**: Browser direct support

### Professional Color Adjustment Techniques

```css
/* Extract primary color */
--color-brand: oklch(60% 0.15 250);  /* Blue */

/* Light variant - increase lightness, maintain hue */
--color-brand-light: oklch(90% 0.05 250);

/* Dark variant - decrease lightness, slightly adjust hue */
--color-brand-dark: oklch(40% 0.2 250);

/* Technique: Closer to white/black, lower chroma */
--color-brand-subtle: oklch(95% 0.02 250);
```

---

## Output Format

### Design Tokens

```css
:root {
  /* Brand Colors */
  --color-brand: oklch(60% 0.15 250);
  --color-brand-hover: oklch(50% 0.18 250);

  /* Functional Colors */
  --color-success: oklch(62% 0.15 150);
  --color-warning: oklch(70% 0.15 75);
  --color-error: oklch(58% 0.18 25);

  /* Neutral Colors - with tint */
  --color-bg: oklch(98% 0.01 250);
  --color-bg-elevated: oklch(95% 0.02 250);
  --color-text: oklch(20% 0.01 250);
  --color-text-secondary: oklch(50% 0.01 250);
}
```

### Tailwind Extension

```javascript
// tailwind.config.js
theme: {
  extend: {
    colors: {
      brand: {
        DEFAULT: 'oklch(60% 0.15 250)',
        hover: 'oklch(50% 0.18 250)',
      }
    }
  }
}
```

---

## Color Anti-Patterns (Based on Impeccable)

**DON'T use gray text on colored backgrounds**—it looks washed out and "dead." Use a darker shade of the background color instead.

**DON'T use pure black (#000) or pure white (#fff)**—they don't exist in nature. Always tint. Use oklch(12-18%) for dark backgrounds.

**DON'T use the "AI color palette"**—cyan-on-dark, purple-to-blue gradients, neon accents on dark backgrounds are telltale signs of AI-generated design.

**DON'T overuse brand colors**—accent works because it's rare. Following 60-30-10 rule: 60% neutrals, 30% secondary, 10% accent.

---

## Checklist (Designer Perspective)

- [ ] Does the color convey the right emotion?
- [ ] Is the accent color "scarce"? (Not exceeding 10%)
- [ ] Does contrast guide visual hierarchy?
- [ ] Is dark mode redesigned rather than inverted?
- [ ] Do neutral colors have subtle brand tint?
- [ ] Are functional colors globally universal? (Red = error, Green = success)

---

## Professional Terminology

| Term | Definition | Application |
|------|------------|-------------|
| **Chroma** | Color purity/saturation | Adjusting color vibrancy |
| **Luminance** | Perceived lightness | Contrast calculation |
| **Tint** | Mix with white | Create light variants |
| **Shade** | Mix with black | Create dark variants |
| **Tone** | Mix with gray | Create mid-tones |
| **Semantic Color** | Meaningful color names | label, background |
| **Token** | Design token | Reusable design values |
