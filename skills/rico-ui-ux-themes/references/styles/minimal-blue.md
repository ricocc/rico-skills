# Minimal Blue Style

Minimal, Efficient, Professional, Performance-First, Collaborative

---

## Design Philosophy

### Brand Philosophy

**"Speed & Collaboration"**

Minimal Blue design philosophy creates a minimal style for high-performance code editors and developer tools. Through dark backgrounds and high-contrast accent colors, it conveys professional, efficient, and modern technical product qualities.

### Design Philosophy

1. **Minimalism First - Performance Priority**
   - Remove all unnecessary decoration
   - Every pixel serves a function
   - Fast response, zero lag feeling

2. **High Contrast - Clear & Readable**
   - Dark background reduces eye strain
   - Bright accent colors clearly identify syntax and status
   - Restrained syntax highlighting, not flashy

3. **Collaboration Friendly - Real-Time Multiplayer**
   - Clear cursor and selection states
   - Elegant multi-user collaboration visual feedback
   - Clear code diff comparison

4. **Modern Professional - Contemporary**
   - Contemporary design language
   - Light/dark mode support
   - Elegant transition animations

### Core Keywords

- Fast
- Minimal
- Professional
- Collaborative
- Modern

---

## Overview

Minimal Blue style is designed for code editors, developer tools, and AI programming assistants. Dark background as primary, paired with blue/purple accent colors, high contrast ensures visual comfort during extended programming sessions.

---

## Color System

### Brand Color

```css
/* Minimal Blue Blue-Purple - Brand Primary Color */
--color-primary: #3B82F6;
--color-primary-hover: #2563EB;
--color-primary-light: #60A5FA;
--color-primary-lighter: #DBEAFE;
```

#### Usage Guidelines

**When to Use:**

- Primary buttons (download, install)
- Links and clickable elements
- Cursor and selection states
- Key syntax highlighting
- Collaborator cursor colors

**Avoid Using:**

- Large area backgrounds (too harsh)
- Decorative elements
- Non-critical operations

**Usage Principle:** About 5-8% of page area

**Why Blue-Purple?**
- Psychology: Blue represents professionalism, technology, trust
- Visual effect: Clearly distinguishable on dark background
- Industry characteristic: Common color for developer tools
- Modern feel: Matches contemporary editor aesthetics

### Background Colors

```css
/* Dark mode (default) */
--color-bg: #0D1117;           /* Main background - Deep blue-black */
--color-bg-secondary: #161B22; /* Secondary background */
--color-bg-tertiary: #21262D;   /* Auxiliary background */
--color-bg-elevated: #1C2128;   /* Floating layer */

/* Light mode */
--color-bg-light: #FFFFFF;
--color-bg-secondary-light: #F6F8FA;
--color-bg-tertiary-light: #EAEAEF;
```

### Text Colors

```css
/* Dark mode */
--color-text: #E6EDF3;           /* Primary text */
--color-text-secondary: #8B949E; /* Secondary text */
--color-text-tertiary: #6E7681;  /* Auxiliary text */
--color-text-disabled: #484F58;

/* Light mode */
--color-text-light: #24292F;
--color-text-secondary-light: #57606A;
--color-text-tertiary-light: #8B949E;
```

### Border Colors

```css
/* Dark mode */
--color-border: #30363D;
--color-border-light: #21262D;
--color-border-focus: #3B82F6; /* Blue on focus */

/* Light mode */
--color-border-light: #D0D7DE;
--color-border-subtle-light: #EAEAEF;
```

### Accent Colors

```css
/* Minimal Blue Signature Accents */
--color-accent-blue: #3B82F6;    /* Blue - Primary accent */
--color-accent-purple: #8B5CF6;  /* Purple - AI/Collaboration */
--color-accent-green: #22C55E;   /* Green - Success */
--color-accent-red: #EF4444;     /* Red - Error */
--color-accent-yellow: #EAB308;  /* Yellow - Warning */
--color-accent-orange: #F97316;  /* Orange - Modification */
```

#### Functional Color Guidelines

- Success: Green #22C55E
- Warning: Yellow #EAB308
- Error: Red #EF4444
- Info: Blue #3B82F6
- Collaboration: Purple #8B5CF6 (multi-user cursors)

---

## Interaction Philosophy

### Animation Principles

**Fast, Fluid, Non-Intrusive**

Code editors need zero-lag response, animations cannot affect programming efficiency.

#### State Feedback

- Focus: Border highlight (blue) + slight glow
- Hover: Slight background change (#161B22)
- Click: Immediate response, no scaling

#### Transition Duration

- Fast: 100ms (button hover)
- Normal: 150ms (panel expand)
- Slow: 200ms (page transition)

**Why So Fast?**
- Editors need zero lag feeling
- Reduce visual distraction
- Maintain fluid experience

#### Animations to Avoid

- Any animation that blocks input
- Bounce effects
- Complex 3D effects
- Long animations (> 200ms)

### Feedback Mechanisms

**Instant, Clear, Non-Intrusive**

- Button click: Immediate background change
- Input focus: Immediate border highlight
- Operation success: Blue toast (2s auto-dismiss)
- Operation failure: Red prompt + error explanation
- Loading state: Minimal spinner or progress bar

---

## Layout Principles

### Spacing Strategy

**4px Grid System**

- All spacing is multiples of 4
- Compact layout, high information density
- Suitable for code editing scenarios

**Common Spacing:**

- Small spacing: 4px, 8px (related elements)
- Medium spacing: 12px, 16px (inside components)
- Large spacing: 24px, 32px (between modules)

### Compact Layout

**Information Density First**

Developer tools need to display lots of information, layout is relatively compact:

- Button height: 32-36px (compact)
- Spacing: 8-12px (dense)
- Font size: 13-14px (body text)
- Line height: 1.4-1.5 (code lines)

**Why So Compact?**
- Screen space is precious
- Developers are used to dense information
- Maximize code visible area

### Content Max Width

- Editor area: Unlimited (full width)
- Sidebar: 280px
- Terminal panel: Height 200px (adjustable)

---

## Component Design Decisions

### Buttons

#### Why 32-36px Height?

- Compact layout requirement
- Mouse operation primary
- Consistent with editor style

#### Why 6px Border Radius?

- Smaller than consumer products (8px)
- More professional, restrained
- Matches developer tool aesthetics

#### Why Blue Primary Button?

- Brand identity
- Clear on dark background
- Professional feel

### Inputs

#### Why 32-36px Height?

- Consistent with button height
- Visual coordination and unity

#### Why Blue Focus Glow?

- Clear state feedback
- Brand color reinforcement
- Doesn't change border thickness (avoids layout jumping)

### Code Editor

#### Why Dark Background?

- Reduces eye strain
- Improves contrast
- Developer preference
- Comfortable for extended programming

#### Why Restrained Syntax Highlighting?

- Avoids rainbow color distraction
- Highlights key information
- Maintains professional feel
- Reduces cognitive load

### Diff Comparison

#### Why Highlight Modified Lines?

- Clearly identify changes
- Code review friendly
- Collaboration essential
- Version control visualization

---

## Typography Scale

```css
--font-size-xs: 11px;
--font-size-sm: 13px;
--font-size-base: 14px;
--font-size-md: 16px;
--font-size-lg: 18px;
--font-size-xl: 20px;
--font-size-2xl: 24px;
```

### Font Weights

```css
--font-weight-normal: 400;
--font-weight-medium: 500;
--font-weight-semibold: 600;
```

### Font Family

```css
/* Modern monospace font */
--font-family: 'Inter', -apple-system, BlinkMacSystemFont, sans-serif;
--font-family-mono: 'JetBrains Mono', 'SF Mono', 'Fira Code', Consolas, monospace;
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
```

---

## Border Radius System

```css
--radius-sm: 4px;
--radius-md: 6px;
--radius-lg: 8px;
--radius-xl: 12px;
```

---

## Shadows

```css
--shadow-sm: 0 1px 2px rgba(0, 0, 0, 0.3);
--shadow-md: 0 4px 6px rgba(0, 0, 0, 0.25);
--shadow-lg: 0 10px 15px rgba(0, 0, 0, 0.2);
```

---

## Component Specifications

### Buttons

```css
.btn {
  height: 34px;
  padding: 0 12px;
  font-size: 13px;
  font-weight: 500;
  border-radius: 6px;
  transition: all 0.1s ease-out;
}

.btn-primary {
  background: #3B82F6;
  color: white;
  border: none;
}

.btn-primary:hover {
  background: #2563EB;
}

.btn-secondary {
  background: #21262D;
  color: #E6EDF3;
  border: 1px solid #30363D;
}

.btn-ghost {
  background: transparent;
  color: #3B82F6;
}
```

### Inputs

```css
.input {
  height: 34px;
  padding: 0 10px;
  font-size: 13px;
  border: 1px solid #30363D;
  border-radius: 6px;
  background: #0D1117;
  color: #E6EDF3;
}

.input:focus {
  outline: none;
  border-color: #3B82F6;
  box-shadow: 0 0 0 2px rgba(59, 130, 246, 0.3);
}
```

### Code Blocks

```css
.code-block {
  background: #161B22;
  border: 1px solid #30363D;
  border-radius: 6px;
  padding: 12px;
  font-family: 'JetBrains Mono', monospace;
  font-size: 13px;
  line-height: 1.5;
}

/* Syntax highlighting (example) */
.syntax-keyword { color: #FF7B72; }
.syntax-string { color: #A5D6FF; }
.syntax-comment { color: #8B949E; }
.syntax-function { color: #D2A8FF; }
.syntax-number { color: #79C0FF; }
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

## Application Scenarios

### Scenario 1: Code Editor (IDE)

**Core Applications:**

- Dark background editor (#0D1117)
- Blue syntax highlighting (#3B82F6)
- High contrast text
- Clear line numbers and cursor

**Adjustments:**

- Maintain compact layout
- Emphasize code readability
- Restrained syntax highlighting
- Support theme switching

### Scenario 2: AI Programming Assistant

**Core Applications:**

- Purple AI suggestion highlight (#8B5CF6)
- Inline edit interface
- Fluid interaction feedback
- Multi-user collaboration cursors

**Adjustments:**

- Add purple accent (AI elements)
- Reinforce collaboration feel
- Optimize interaction flow

### Scenario 3: Developer Tools

**Core Applications:**

- Dark console
- Blue/green syntax colors
- Clear error prompts
- Efficient data display

**Adjustments:**

- Highlight data visualization
- Optimize table display
- Reinforce filtering functionality

### Scenario 4: Technical Documentation

**Core Applications:**

- Light/dark mode
- Code block dark background
- Blue links
- Clear hierarchy structure

**Adjustments:**

- Increase line height (1.6-1.8)
- Increase content max width (75ch)
- Optimize reading experience

### Scenario 5: API Documentation

**Key Adjustments:**

- Code blocks use monospace font
- Blue identifies methods and parameters
- Clear request/response examples
- Side navigation (280px)

**Keep Unchanged:**

- Blue primary elements
- Minimal aesthetics
- Fast response

---

## Common Mistakes

### Common Errors

#### Error 1: Overusing Blue

- Wrong: All buttons, all icons use blue
- Correct: Restrained accents, not exceeding 8% of page area
- Reason: Loses minimal aesthetic, appears cluttered

#### Error 2: Syntax Highlighting Too Flashy

- Wrong: Rainbow syntax highlighting, high saturation
- Correct: Restrained blue/purple/green/orange low saturation
- Reason: Interferes with reading, loses professional feel

#### Error 3: Border Radius Too Large

- Wrong: 12px, 16px border-radius
- Correct: 4-6px border-radius
- Reason: Loses professional feel, appears insufficiently rigorous

#### Error 4: Animations Too Slow

- Wrong: 300ms, 500ms slow transitions
- Correct: 100-150ms fast response
- Reason: Affects programming efficiency, developers don't need flashy animations

#### Error 5: Too Much Whitespace

- Wrong: Lots of whitespace, like marketing pages
- Correct: Compact layout, high information density
- Reason: Screen space is precious, need to see more code

#### Error 6: Font Size Too Large

- Wrong: 16px, 18px body text
- Correct: 13-14px body text
- Reason: Loses compact feel, doesn't match editor positioning

### Negative Checklist

- Don't use light background (#FFFFFF) as main editor background, use dark (#0D1117)
- Don't use large border-radius (> 6px), use small (4-6px)
- Don't use slow animations (> 200ms), use fast response (100-150ms)
- Don't over-decorate, maintain minimal
- Don't use high saturation syntax highlighting, use low saturation professional colors
- Don't use bounce effects, use fluid transitions
- Don't hide important information, maintain transparency

---

## Best For

- Code editors / IDE
- AI programming assistants
- Developer tools
- Technical documentation
- API documentation
- Version control interfaces
- Terminal / Console
- Online code playgrounds
