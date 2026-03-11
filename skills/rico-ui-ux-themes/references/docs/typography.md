# Typography Optimization Guide

> For general optimization workflow, see SKILL.md. This guide focuses on typography design decisions.

---

## First Principles of Typography

**Typography is the skeletal system of interface.**

Good typography helps users:
- **Understand instantly** — Get key information within 1 second
- **Read fluently** — No need to "learn" to read the interface
- **Feel professionalism** — Font choice conveys brand character

> Apple: Typography is about establishing a clear hierarchy that guides the user through content.
>
> "Excellent typography is invisible—users don't notice it, but feel its presence."

---

## Professional Typography Decision Framework

### 1. Hierarchy is Meaning

**The question is not "how big", but "how important".**

| Level | Visual Weight | Apple Approach | Airbnb Approach |
|-------|---------------|----------------|-----------------|
| **Display** | Heaviest | 34-40pt | 32-40px |
| **Title** | Heavy | 28pt | 24-28px |
| **Headline** | Medium-heavy | 22pt | 20-22px |
| **Body** | Normal | 17pt | 16px |
| **Caption** | Light | 13pt | 12-13px |

**Core Principles**:
- Maximum 5 hierarchy levels
- Adjacent levels differ by at least 20%
- Step back and ask: Do we really need this level?

### 2. Leading is Breathing

**Professional Formula**: Line height = Font size × 1.2 ~ 1.8

| Content Type | Ratio | Use Case |
|--------------|-------|----------|
| Headlines | 1.1-1.3 | Apple style |
| Body text | 1.5-1.6 | Regular reading |
| Long form | 1.7-1.8 | Blogs, documentation |
| UI labels | 1.2-1.4 | Buttons, forms |

**Apple SF Pro Approach**:
- 17pt body uses 22pt line height (1.29)
- 22pt headline uses 28pt line height (1.27)
- Maintain visual consistency, not mathematical consistency

### 3. Weight is Emphasis

**If weight can solve it, don't use color.**

| Weight | Value | Apple Usage |
|--------|-------|-------------|
| Regular | 400 | Body text, labels |
| Medium | 500 | Headlines, buttons |
| Semibold | 600 | Emphasized headlines |
| Bold | 700 | Rarely used |

**Anti-pattern**: All bold = no bold.

---

## Top Company Typography Systems

### Apple SF Pro

```
SF Pro Text: -0.01 letter-spacing
SF Pro Display: -0.02 letter-spacing
```

| Style | Font Size | Line Height | Weight | Letter Spacing |
|-------|-----------|-------------|--------|----------------|
| Large Title | 34pt | 41pt | Bold | -0.37 |
| Title 1 | 28pt | 34pt | Bold | -0.36 |
| Title 2 | 22pt | 28pt | Bold | -0.35 |
| Title 3 | 20pt | 25pt | Semibold | -0.2 |
| Headline | 17pt | 22pt | Semibold | -0.41 |
| Body | 17pt | 22pt | Regular | -0.41 |
| Callout | 16pt | 21pt | Regular | -0.32 |
| Subhead | 15pt | 20pt | Regular | -0.24 |
| Footnote | 13pt | 18pt | Regular | -0.08 |
| Caption 1 | 12pt | 16pt | Regular | 0 |
| Caption 2 | 11pt | 13pt | Regular | 0.07 |

### IBM Plex

IBM's in-house font, serving industrial style:

```css
/* IBM Plex Typography System */
--font-family-sans: 'IBM Plex Sans', system-ui;
--font-family-mono: 'IBM Plex Mono', monospace;

/* Characteristics: */
--letter-spacing-tightest: -0.02em;
--letter-spacing-tight: -0.01em;
--letter-spacing-normal: 0;
--letter-spacing-wide: 0.01em;
--letter-spacing-widest: 0.02em;
```

### Airbnb Cereal

Airbnb's in-house font, serving warm and friendly style:

```css
/* Characteristics: Rounded x-height */
/* Precisely calculated number spacing */
font-feature-settings: 'tnum' on, 'lnum' on;
```

---

## Font Selection Decisions

### Anti-Patterns (Based on Impeccable)

**DON'T use overused fonts**—Inter, Roboto, Arial, Open Sans, system defaults unless appropriate for the context. These fonts are everywhere, making your design feel generic and "AI-generated."

**Better alternatives**:
- Instead of Inter → **Instrument Sans**, **Plus Jakarta Sans**, **Outfit**
- Instead of Roboto → **Onest**, **Figtree**, **Urbanist**
- Instead of Open Sans → **Source Sans 3**, **Nunito Sans**, **DM Sans**
- For editorial/premium feel → **Fraunces**, **Newsreader**, **Lora**

**When system fonts are appropriate**: Native apps, developer tools, performance-critical applications where font loading time matters.

### When to Use Which Font

| Scenario | Recommended | Avoid |
|----------|-------------|-------|
| Enterprise/SaaS | IBM Plex, Source Sans | Decorative fonts |
| Consumer/Social | DM Sans, Circular | System defaults |
| Media/Content | Merriweather, Lora | Bold geometric |
| Developer | JetBrains, Fira Code | Handwriting fonts |

### Font Pairing Principles

**One Principle**: Contrast, not matching

```
Display Font (Headlines)  +  Body Font (Body)
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
Geometric Sans            Humanist Sans
(e.g., Futura)            (e.g., Proxima Nova)

Serif Headlines           Sans Body
(e.g., Playfair)          (e.g., Inter)

Bold Heavy Headlines      Light Fine Body
(e.g., Brandon)           (e.g., Lato)
```

**Common Mistake**: Pairing two similar fonts (Inter + Roboto = pointless repetition)

---

## Vertical Rhythm

### Professional Grid System

**Every spacing should be a multiple of the base unit.**

```
Base unit = Line height

If line height = 20px
Spacing = 20px, 40px, 60px...
```

### Apple Approach

```css
/* 20px baseline grid */
--space-1: 4px;   /* 4/20 = 0.2 */
--space-2: 8px;   /* 8/20 = 0.4 */
--space-3: 12px;  /* 12/20 = 0.6 */
--space-4: 16px;  /* 16/20 = 0.8 */
--space-5: 20px;  /* 20/20 = 1.0 */
--space-6: 24px;  /* 24/20 = 1.2 */
```

### Checkpoints

- [ ] Headline to body spacing is a multiple of line height
- [ ] Paragraph spacing is a multiple of line height
- [ ] Component spacing coordinates with text line height
- [ ] Baseline grid alignment (optional, Apple doesn't enforce)

---

## Responsive Typography

### Fluid Typography

```css
/* Use clamp for smooth scaling */
--font-size-body: clamp(14px, 0.875rem + 0.5vw, 18px);
--font-size-heading: clamp(24px, 1.5rem + 1vw, 48px);
```

### Breakpoint Strategy

| Device | Base Font Size | Max Line Width |
|--------|----------------|----------------|
| Mobile | 14-16px | 45ch |
| Tablet | 16px | 55ch |
| Desktop | 16-17px | 65ch |

**Apple Approach**: iPhone and iPad use the same font size system, Mac has slight adjustments.

---

## Output Format

### CSS Variables

```css
:root {
  /* Font sizes */
  --font-size-xs: 12px;
  --font-size-sm: 14px;
  --font-size-base: 16px;
  --font-size-lg: 18px;
  --font-size-xl: 20px;
  --font-size-2xl: 24px;
  --font-size-3xl: 30px;
  --font-size-4xl: 36px;

  /* Line heights */
  --line-height-tight: 1.25;
  --line-height-normal: 1.5;
  --line-height-relaxed: 1.75;

  /* Font weights */
  --font-weight-regular: 400;
  --font-weight-medium: 500;
  --font-weight-semibold: 600;

  /* Letter spacing */
  --letter-spacing-tight: -0.02em;
  --letter-spacing-normal: 0;
  --letter-spacing-wide: 0.02em;
}
```

---

## Checklist (Designer Perspective)

- [ ] Can users identify the page theme within 1 second?
- [ ] Is hierarchy using the "step back" principle? (Can we remove a level?)
- [ ] Is body text 16px? (Mobile)
- [ ] Does line height match font size? (1.2-1.8x)
- [ ] Maximum 2 font families?
- [ ] Is vertical rhythm aligned?

---

## Professional Terminology

| Term | Definition |
|------|------------|
| **Leading** | Line height |
| **Kerning** | Letter spacing adjustment |
| **Tracking** | Character spacing |
| **x-height** | Lowercase letter height |
| **Cap height** | Uppercase letter height |
| **Baseline** | Baseline |
| **Measure** | Line length (character count) |
| **Fluid Type** | Fluid typography |
| **Type Scale** | Font size ratio |
