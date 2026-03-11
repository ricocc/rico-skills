# Claude Style

Rational, Restrained, Warm, Unique

---

## Design Philosophy

### Brand Philosophy

**"AI with Warmth"**

Claude's design philosophy is injecting warmth into rational restraint. Not a cold technical tool, but an intelligent and empathetic assistant. Design conveys professionalism without losing approachability through warm ocher orange and warm white tones.

### Design Philosophy

1. **Restrained Minimalism - Function First**
   - Keep only core information and interactions
   - Remove redundant decoration, follow "less is more"
   - Visual elements serve function, don't steal the show

2. **Secure & Transparent - Auditable**
   - Interface clearly shows permissions, operation boundaries
   - Let users perceive security and controllability
   - Don't hide risks, don't blur operation logic

3. **Developer Friendly - Professional Quality**
   - Target technical audience, emphasize code feel
   - Strong logic, high professionalism
   - Calm and rational visual style, not flashy

4. **Warm & Unique - Differentiated**
   - Warm white tone distinguishes from cold development tools
   - Ocher orange brand color, unique and recognizable
   - Stand out among similar products

### Core Keywords

- Rational
- Restrained
- Warm
- Professional
- Trustworthy

---

## Overview

Claude style originates from Claude Code official VS Code theme—unique warm white tone + ocher orange accent. Suitable for developer tools, AI products.

---

## Color System

### Brand Color

```css
/* Claude Ocher Orange - Brand Primary Color */
--color-primary: #C15F3C;
--color-primary-hover: #A14A2F;
--color-primary-muted: #C15F3C80;
```

#### Usage Guidelines

**When to Use:**

- Status bar background (brand identity)
- Primary buttons (CTA)
- Selected states, active states
- Links and key interactive elements
- Code highlight keywords

**Avoid Using:**

- Large area backgrounds (ocher orange has high saturation)
- Non-critical action buttons
- Decorative elements

**Usage Principle:** Not exceeding 8% of page area

**Why Ocher Orange?**
- Warmth: Distinguishes from cold blue development tools
- Uniqueness: Stands out among similar products
- Professionalism: Ocher orange is warm yet steady
- Recognizability: Distinctive brand color, memorable

### Background Colors

```css
/* Light mode - Warm White */
--color-bg: #FAFAF9;        /* Main background */
--color-bg-editor: #FAF9F4;  /* Editor background */
--color-bg-secondary: #F5F4ED; /* Sidebar */
--color-bg-tertiary: #F0EFED; /* Secondary background */
--color-bg-elevated: #FDFCFB; /* Floating layer */

/* Dark mode */
--color-bg-dark: #171615;
--color-bg-secondary-dark: #1F1E1D;
--color-bg-tertiary-dark: #2A2928;
```

### Text Colors

```css
/* Light mode */
--color-text: #2C2C2C;       /* Primary text */
--color-text-secondary: #525252;
--color-text-tertiary: #A19A94;
--color-text-disabled: #706F6E;

/* Dark mode */
--color-text-dark: #FAF9F4;
--color-text-secondary-dark: #A7A8A7;
--color-text-tertiary-dark: #706F6E;
```

### Border Colors

```css
/* Light mode */
--color-border: #E8E6E3;
--color-border-hover: #D4D4D4;

/* Dark mode */
--color-border-dark: #47494B;
--color-border-subtle-dark: #2A2928;
```

#### Why Light Borders?

- Restrained design: Borders don't distract, content is primary
- Clear hierarchy: Distinguish areas through subtle borders
- Avoid clutter: Dark borders make interface appear harsh

### Accent Colors

```css
/* Claude Signature Accents */
--color-accent: #C15F3C;       /* Ocher - Primary accent */
--color-accent-gold: #EEC554;    /* Gold - Highlight/Special */
--color-accent-blue: #0366D6;
--color-accent-green: #28A745;
--color-accent-red: #D73A49;
--color-accent-pink: #EA4AAA;
--color-accent-cyan: #39C5CF;
```

#### Functional Color Guidelines

- Success: Green #28A745
- Warning: Gold #EEC554 (softer)
- Error: Red #D73A49 (low saturation)
- Info: Blue #0366D6

**Avoid High Saturation:** All functional colors use low saturation, maintaining restrained professionalism

---

## Interaction Philosophy

### Animation Principles

**Fast, Precise, Non-Intrusive**

Developer tools need fast response, animations cannot affect efficiency.

#### State Feedback

- Focus: Border highlight + glow (ocher orange)
- Hover: Slight background change
- Click: Slight scale (scale 0.98)

#### Transition Duration

- Fast: 100ms (button hover)
- Normal: 150ms (panel expand)
- Slow: 200ms (page transition)

**Why So Fast?**
- Developer tools need efficiency
- Reduce waiting feeling
- Avoid sluggishness

#### Animations to Avoid

- Rotating spinners (use solid progress bar instead)
- Bounce effects
- Complex 3D effects
- Long animations (> 300ms)

### Feedback Mechanisms

**Instant, Clear**

- Button click: Immediate background change
- Input focus: Immediate border highlight
- Operation success: Toast notification (1.5s auto-dismiss)
- Operation failure: Red border + error text

---

## Layout Principles

### Spacing Strategy

**4px Grid System**

- All spacing is multiples of 4
- Compact but not crowded
- Suitable for high information density scenarios

**Common Spacing:**

- Small spacing: 4px, 8px (related elements)
- Medium spacing: 12px, 16px (inside components)
- Large spacing: 24px, 32px (between modules)

### Compact Layout

**Information Density First**

Developer tools need to display lots of information, layout is relatively compact:

- Button height: 32px (smaller than standard 44px)
- Spacing: 12-16px (smaller than standard 24px)
- Font size: 13-14px (smaller than standard 16px)

**Why So Compact?**
- Screen space is precious
- Developers are used to dense information
- Improve work efficiency

### Content Max Width

- Editor area: Unlimited (full width)
- Sidebar: 280-320px
- Terminal panel: Height 200px (adjustable)

---

## Component Design Decisions

### Buttons

#### Why 32px Height?

- Compact layout requirement
- Mouse operation primary (no need for 44px touch target)
- Consistent with code editor style

#### Why 6px Border Radius?

- Smaller than Airbnb's 8px (more professional)
- Larger than pure square corners (more friendly)
- Fits the restrained aesthetic of developer tools

#### Why Ocher Orange Primary Button?

- Brand identity
- Stands out in gray background
- Warmth distinguishes from cold development tools

### Inputs

#### Why 32px Height?

- Consistent with button height
- Visual coordination and unity

#### Why Ocher Orange Focus Glow?

- Clear state feedback
- Brand color reinforcement
- Doesn't change border thickness (avoids layout jumping)

### Cards

#### Why 8px Border Radius?

- More rounded than buttons (6px)
- Creates container feel
- Restrained design, doesn't dominate

#### Why Light Borders?

- Doesn't compete with content
- Clear hierarchy
- Maintains simplicity

### Status Bar

#### Why Ocher Orange Background?

- Brand identity
- Distinguishes from regular editors
- Warmth, not cold

---

## Application Scenarios

### Scenario 1: Developer Tools (IDE/Editor)

**Core Applications:**

- Ocher orange status bar
- Warm white editor background
- Compact toolbar
- Syntax highlighting (ocher orange keywords)

**Adjustments:**

- Maintain compact layout
- Emphasize code readability
- Use dark mode (#171615 background)

### Scenario 2: AI Product Interface

**Core Applications:**

- Ocher orange primary button ("Generate", "Execute")
- Warm white background
- Gold highlight (AI response section)
- Restrained animations

**Adjustments:**

- Increase whitespace (more generous than developer tools)
- Emphasize conversational feel
- Use avatars and identity indicators

### Scenario 3: Technical Documentation

**Core Applications:**

- Warm white background (#FAFAF9)
- Ocher orange links
- Clear hierarchy structure
- Code block warm gray background (#FDFCFB)

**Adjustments:**

- Increase line height (1.6-1.8)
- Increase content max width (65ch)
- Optimize reading experience

### Scenario 4: API Documentation

**Core Applications:**

- Code blocks use monospace font
- Ocher orange identifies methods and parameters
- Clear request/response examples
- Side navigation (280px)

**Adjustments:**

- Strengthen code display
- Use code copy button
- Highlight key information

### Scenario 5: Terminal CLI

**Key Adjustments:**

- Dark background (#171615)
- Green/ocher orange prompt
- Monospace font
- Minimized decoration

**Keep Unchanged:**

- Ocher orange brand elements
- Restrained aesthetic
- Fast response

---

## Common Mistakes

### Common Errors

#### Error 1: Overusing Ocher Orange

- Wrong: All buttons, all icons use ocher orange
- Correct: Sparingly applied, not exceeding 8% of page area
- Reason: Loses restrained aesthetic, appears cluttered

#### Error 2: Using Cool White Tones

- Wrong: #FFFFFF pure white background
- Correct: #FAFAF9 warm white background
- Reason: Loses warmth, cannot convey "warm rationality"

#### Error 3: Border Radius Too Large

- Wrong: 12px, 16px border-radius
- Correct: 4-8px border-radius
- Reason: Loses professionalism, appears insufficiently rational

#### Error 4: Animations Too Slow

- Wrong: 300ms, 500ms slow transitions
- Correct: 100-150ms fast response
- Reason: Affects work efficiency, developers don't need flashy animations

#### Error 5: Too Much Whitespace

- Wrong: Lots of whitespace, like marketing pages
- Correct: Compact layout, high information density
- Reason: Screen space is precious, developers need to see more information

#### Error 6: Font Size Too Large

- Wrong: 16px, 18px body text
- Correct: 13-14px body text
- Reason: Loses compact feel, doesn't fit developer tool positioning

### Negative Checklist

- Don't use pure white (#FFFFFF), use warm white (#FAFAF9)
- Don't use large border-radius (> 8px), use small (4-8px)
- Don't use slow animations (> 200ms), use fast response (100-150ms)
- Don't over-decorate, maintain restraint
- Don't use high saturation colors, use low saturation professional colors
- Don't use rotating spinners, use progress bars or solid indicators
- Don't hide risks, maintain transparent and auditable

---

## Typography Scale

```css
--font-size-xs: 11px;
--font-size-sm: 13px;
--font-size-base: 14px;
--font-size-lg: 16px;
--font-size-xl: 18px;
--font-size-2xl: 20px;
--font-size-3xl: 24px;
--font-size-4xl: 30px;
```

### Font Weights

```css
--font-weight-normal: 400;
--font-weight-medium: 500;
--font-weight-semibold: 600;
```

---

## Spacing System

```css
--space-1: 4px;
--space-2: 8px;
--space-3: 12px;
--space-4: 16px;
--space-5: 20px;
--space-6: 24px;
--space-8: 32px;
--space-10: 40px;
--space-12: 48px;
```

---

## Border Radius System

```css
--radius-sm: 4px;
--radius-md: 6px;
--radius-lg: 8px;
--radius-xl: 10px;
--radius-2xl: 12px;
--radius-full: 9999px;
```

---

## Shadows

```css
--shadow-sm: 0 1px 2px rgb(0 0 0 / 0.05);
--shadow-md: 0 4px 6px -1px rgb(0 0 0 / 0.1);
--shadow-lg: 0 10px 15px -3px rgb(0 0 0 / 0.1);
```

---

## Component Specifications

### Buttons

```css
.btn {
  height: 32px;
  padding: 0 12px;
  font-size: 13px;
  font-weight: 500;
  border-radius: 6px;
  transition: all 0.15s ease-out;
}

.btn-primary {
  background: #C15F3C;
  color: white;
}

.btn-primary:hover {
  background: #A14A2F;
}

.btn-secondary {
  background: transparent;
  border: 1px solid #E8E6E3;
  color: #2C2C2C;
}

.btn-ghost {
  background: transparent;
  color: #525252;
}

.btn-ghost:hover {
  background: #F5F4ED;
}
```

### Inputs

```css
.input {
  height: 32px;
  padding: 0 10px;
  font-size: 13px;
  border: 1px solid #E8E6E3;
  border-radius: 6px;
  background: white;
}

.input:focus {
  outline: none;
  border-color: #C15F3C;
  box-shadow: 0 0 0 2px rgba(193, 95, 60, 0.2);
}
```

### Cards

```css
.card {
  background: white;
  border: 1px solid #E8E6E3;
  border-radius: 8px;
  padding: 16px;
}
```

### Status Bar

```css
.status-bar {
  background: #C15F3C;
  color: white;
}

.activity-bar {
  background: #F0EFED;
  border-right: 1px solid #E8E6E3;
}

.side-bar {
  background: #F5F4ED;
  border-right: 1px solid #E8E6E3;
}
```

### Panels & Terminal

```css
.panel {
  background: #F8F7F6;
  border-top: 1px solid #E8E6E3;
}

.terminal {
  background: #FDFCFB;
  color: #2C2C2C;
}
```

---

## Animations

```css
--duration-fast: 100ms;
--duration-normal: 150ms;
--duration-slow: 200ms;

--ease-out: cubic-bezier(0.16, 1, 0.3, 1);
```

---

## Best For

- Developer tools
- AI products
- Code editors
- Technical documentation
- IDE themes
