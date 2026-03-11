# Linear Style

Efficient, Precise, Minimal, Technical, Professional

---

## Design Philosophy

### Brand Philosophy

**"Efficiency First"**

Linear's design philosophy is designed for extreme efficiency. Every pixel is carefully calculated, every interaction pursues the fastest response. Design conveys professional, efficient, and technical qualities through minimalist black and white palette and ultra-compact layout.

### Design Philosophy

1. **Extreme Compactness - Information Density First**
   - Screen space is precious
   - Display more information in limited space
   - Reduce scrolling, improve efficiency

2. **Minimal Black and White - Remove Distractions**
   - Black and white primarily, no extra colors
   - Let content be the hero
   - Reduce visual noise

3. **Precise and Efficient - Every Millisecond Counts**
   - Fast response (100-150ms)
   - Keyboard operation priority
   - Distraction-free workflow

4. **Technical Aesthetics - Professional Quality**
   - Non-standard font weights (510, 590)
   - Pixel-perfect design
   - For technical users

### Core Keywords

- Efficient
- Precise
- Minimal
- Technical
- Professional

---

## Overview

Linear style originates from linear.app—efficient, precise, compact. Suitable for SaaS platforms, project management tools, and data dashboards.

---

## Color System

### Brand Color

```css
--color-primary: #000000;        /* Black */
--color-primary-hover: #1A1A1A;
--color-secondary: #FFFFFF;
```

#### Usage Guidelines

**When to Use:**

- Primary buttons (black background, white text)
- Key operations
- Titles and important text
- Borders and dividers

**Avoid Using:**

- Large area black backgrounds (too heavy)
- Decorative elements
- Non-critical information

**Why Black and White?**
- Extreme minimalism: No color distraction
- High contrast: Best readability
- Timeless: Classic palette
- Technical feel: Black and white = code, terminal

### Background Colors

```css
/* Light mode */
--color-bg: #FFFFFF;
--color-bg-subtle: #F5F5F5;
--color-bg-hover: #F0F0F0;

/* Dark mode - Pure black */
--color-bg-dark: #000000;
--color-bg-subtle-dark: #0A0A0A;
--color-bg-hover-dark: #111111;
```

### Text Colors

```css
/* Light mode - Black primarily */
--color-text: #000000;
--color-text-secondary: #525252;
--color-text-tertiary: #737373;
--color-text-disabled: #A3A3A3;

/* Dark mode - White */
--color-text-dark: #FFFFFF;
--color-text-secondary-dark: #A3A3A3;
--color-text-tertiary-dark: #737373;
```

### Border Colors

```css
--color-border: #E5E5E5;
--color-border-subtle: #F0F0F0;

/* Dark mode */
--color-border-dark: #262626;
--color-border-subtle-dark: #171717;
```

### Accent Colors

```css
--color-accent: #000000;        /* Black accent */
--color-accent-purple: #8B5CF6;
--color-accent-red: #EF4444;
--color-accent-green: #22C55E;
--color-accent-yellow: #EAB308;
--color-accent-blue: #3B82F6;
```

#### Functional Color Guidelines

- Success: Green #22C55E
- Warning: Yellow #EAB308
- Error: Red #EF4444
- Info: Blue #3B82F6
- Special: Purple #8B5CF6 (Linear purple)

**Restrained Use:** Functional colors only for status indicators, not decoration

---

## Interaction Philosophy

### Animation Principles

**Every Millisecond Counts**

#### State Response

- Focus: Border thickening + shadow
- Hover: Slight background change (#F0F0F0)
- Click: Immediate feedback

#### Transition Duration

- Ultra fast: 50ms (dropdown menus)
- Fast: 100ms (button hover)
- Normal: 150ms (panel expand)

**Why So Fast?**
- SaaS tools need efficiency
- Reduces waiting feeling
- Improves workflow efficiency

#### Animations to Avoid

- All animations (> 200ms)
- Rotation, bounce, zoom
- Complex transitions
- Shadow gradients

### Feedback Mechanisms

**Instant, Precise**

- Button click: Background immediately turns black
- Input focus: 1px black border
- Operation success: Top notification (2s auto-dismiss)
- Operation failure: Red border + inline error text

---

## Layout Principles

### Spacing Strategy

**Extreme Compactness**

**Non-Standard Spacing System:**

- Minimum: 4px, 6px (not 8px)
- Small spacing: 8px, 12px
- Medium spacing: 16px, 20px
- Large spacing: 24px, 32px

**Why 6px?**
- More compact than 8px
- More breathing room than 4px
- Linear's unique rhythm

### Information Density First

**Ultra-Small Font Sizes:**

- Body: 13px (not 16px)
- Small labels: 11px, 12px
- Compact line height: 1.4-1.5

**Non-Standard Font Weights:**

- Medium: 510 (not 500)
- Semibold: 590 (not 600)
- Precise control of visual weight

**Why So Small?**
- Screen space is limited
- Technical users are used to dense information
- Reduce scrolling, improve efficiency

### Content Max Width

- Main content area: 1200px
- Sidebar: 240px (narrower than standard 280px)
- Data tables: Full width

---

## Component Design Decisions

### Buttons

#### Why 28px Height?

- Smaller than Claude's 32px
- Much smaller than Airbnb's 48px
- Extreme compactness, saves space

#### Why 4px Border Radius?

- Smaller than all other styles
- Nearly square corners, more professional
- Strong technical feel

#### Why Black and White Buttons?

- Primary button: Black background, white text
- Secondary button: White background, black border
- Extreme minimalism, no distraction

### Tables/Lists

#### Why So Compact?

- Row height: 32px (not 44px)
- Cell spacing: 4px
- Font size: 13px

**Why?**
- Display more data per screen
- Reduce scrolling
- Improve browsing efficiency

### Inputs

#### Why 28px Height?

- Consistent with buttons
- Visual unity
- Saves vertical space

#### Why Black Border on Focus?

- 1px black border
- Clear state feedback
- Doesn't change layout (avoids jumping)

---

## Application Scenarios

### Scenario 1: Project Management Tools

**Core Applications:**

- Black primary button ("Create Issue")
- Compact list view
- Pure black and white palette
- Minimalist icons

**Adjustments:**

- Maintain compact layout
- Use keyboard shortcuts
- Drag and drop sorting

### Scenario 2: Data Dashboards

**Core Applications:**

- High-density data display
- Thin line charts (1px line width)
- Black and white chart colors
- Compact cards

**Adjustments:**

- Use purple to accent key data
- Chart animation 100ms
- Avoid flashy effects

### Scenario 3: SaaS Platforms

**Core Applications:**

- Side navigation 240px
- Black brand bar
- Compact forms
- Keyboard operation priority

**Adjustments:**

- Add search function
- Use command palette (Cmd+K)
- Shortcut hints

### Scenario 4: Code Collaboration Tools

**Core Applications:**

- Monospace font (13px)
- Black and white syntax highlighting
- Compact diff view
- Line numbers (11px)

**Adjustments:**

- Code folding
- Quick navigation
- Keyboard navigation

### Scenario 5: Mobile Adaptation

**Key Adjustments:**

- Buttons: 28px → 44px (touch target)
- Spacing: 4px → 8px (avoid mis-taps)
- Sidebar: 240px → Full screen drawer

**Keep Unchanged:**

- Black and white palette
- Compact layout
- Fast response

---

## Common Mistakes

### Common Errors

#### Error 1: Using Colors

- Wrong: Blue primary buttons, colorful icons
- Correct: Black and white primarily, purple accents
- Reason: Loses minimal aesthetic, increases visual noise

#### Error 2: Font Size Too Large

- Wrong: 16px, 18px body text
- Correct: 13px, 14px body text
- Reason: Loses compact feel, cannot display information efficiently

#### Error 3: Too Much Whitespace

- Wrong: 24px, 32px spacing
- Correct: 6px, 8px, 12px
- Reason: Wastes screen space, reduces information density

#### Error 4: Border Radius Too Large

- Wrong: 8px, 12px border-radius
- Correct: 3px, 4px, 6px
- Reason: Loses technical feel, appears unprofessional

#### Error 5: Animations Too Slow

- Wrong: 200ms, 300ms transitions
- Correct: 50ms, 100ms, 150ms
- Reason: Affects efficiency, users feel sluggish

#### Error 6: Using Standard Font Weights

- Wrong: 500, 600 font weights
- Correct: 510, 590 font weights
- Reason: Loses Linear's unique visual quality

### Negative Checklist

- Don't use colors, use black and white
- Don't use large font sizes (> 14px), use small (11-13px)
- Don't use large spacing (> 16px), use compact (4-12px)
- Don't use large border-radius (> 6px), use small (3-6px)
- Don't use slow animations (> 150ms), use fast response (50-150ms)
- Don't use standard font weights (500/600), use non-standard (510/590)
- Don't over-decorate, stay minimal

---

## Typography Scale

**Compact Style - Smaller than Standard**

```css
--font-size-xs: 11px;       /* Very small labels */
--font-size-sm: 12px;       /* Small labels, auxiliary */
--font-size-base: 13px;     /* Body - Note: not 16px */
--font-size-lg: 14px;        /* Emphasized body */
--font-size-xl: 15px;       /* Small headings */
--font-size-2xl: 16px;      /* Card titles */
--font-size-3xl: 20px;      /* Section titles */
--font-size-4xl: 32px;      /* Page titles */
--font-size-5xl: 48px;      /* Hero */
```

### Font Weights

```css
--font-weight-normal: 400;
--font-weight-medium: 510;    /* Non-standard 500 */
--font-weight-semibold: 590;  /* Non-standard 600 */
```

### Letter Spacing

```css
--letter-spacing-tightest: -0.02em;   /* Large headings */
--letter-spacing-tight: -0.01em;     /* Headings */
--letter-spacing-normal: -0.005em;   /* Default */
```

---

## Spacing System

**Compact Spacing**

```css
--space-1: 4px;
--space-2: 6px;    /* Non-standard 8px */
--space-3: 8px;
--space-4: 12px;
--space-5: 16px;
--space-6: 20px;
--space-8: 24px;
--space-10: 32px;
--space-12: 40px;
```

---

## Border Radius System

**Small Border Radius**

```css
--radius-sm: 3px;
--radius-md: 4px;
--radius-lg: 6px;
--radius-xl: 8px;
--radius-2xl: 10px;
--radius-full: 9999px;
```

---

## Component Specifications

### Buttons

**Compact Size**

```css
.btn {
  /* Compact size */
  height: 28px;           /* Small */
  padding: 0 10px;
  font-size: 12px;
  font-weight: 510;

  /* Or standard */
  height: 32px;
  padding: 0 12px;
  font-size: 13px;

  border-radius: 6px;
  transition: all 0.1s ease-out;
}

.btn-primary {
  background: #000000;
  color: white;
}

.btn-secondary {
  background: transparent;
  border: 1px solid #E5E5E5;
}

.btn-ghost {
  background: transparent;
  color: #525252;
}

.btn-ghost:hover {
  background: #F5F5F5;
}
```

### Inputs

```css
.input {
  height: 32px;           /* Compact */
  padding: 0 10px;
  font-size: 13px;
  border: 1px solid #E5E5E5;
  border-radius: 6px;
  background: transparent;
}

.input:focus {
  outline: none;
  border-color: #000000;
}
```

### Cards

```css
.card {
  background: white;
  border: 1px solid #E5E5E5;
  border-radius: 8px;
  padding: 12px;          /* Compact padding */
}
```

### List Items

```css
.list-item {
  padding: 8px 12px;
  font-size: 13px;
  border-bottom: 1px solid #F0F0F0;
}

.list-item:hover {
  background: #F5F5F5;
}
```

---

## Animations

**Fast Response**

```css
--duration-fastest: 50ms;
--duration-fast: 100ms;
--duration-normal: 150ms;
--duration-slow: 200ms;

/* Decisive easing */
--ease-out-expo: cubic-bezier(0.16, 1, 0.3, 1);
--ease-out-quart: cubic-bezier(0.25, 1, 0.5, 1);
```

---

## Best For

- Project management tools
- SaaS platforms
- Data dashboards
- Efficiency tools
- Developer tools
- Real-time collaboration apps
