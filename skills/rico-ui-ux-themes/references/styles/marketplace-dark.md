# Marketplace Dark Style

Developer Marketplace, Dark Theme, Code Aesthetics, Efficient Browsing

---

## Design Philosophy

### Brand Philosophy

**"Code & Discover"**

Marketplace Dark design philosophy creates a code aesthetics style for developer marketplaces and technical resource platforms. Through dark backgrounds and code-style design, it conveys technical professionalism and efficient browsing experience.

### Design Philosophy

1. **Code Aesthetics - Developer Friendly**
   - Dark theme (developer preference)
   - Code-style typography
   - Monospace font elements
   - Command-line style prompts

2. **Efficient Browsing - Information Density**
   - Compact layout
   - Clear information hierarchy
   - Quick filtering and search
   - Large resource display

3. **Technical Professional - Quality First**
   - Restrained decoration
   - High contrast design
   - Professional color scheme
   - Technology-oriented

4. **Open Ecosystem - Community Driven**
   - GitHub integration
   - Open source spirit
   - Community contributions
   - Quality metrics

### Core Keywords

- Technical
- Efficient
- Dark
- Developer
- Marketplace

---

## Overview

Marketplace Dark style is designed for developer marketplaces, technical resource platforms, and open source project showcases. Dark theme, code aesthetics, suitable for scenarios that need to display large amounts of technical resources and tools.

---

## Color System

### Brand Color

```css
/* Marketplace Dark Tech Blue - Brand Primary Color */
--color-primary: #3B82F6;
--color-primary-hover: #2563EB;
--color-primary-light: #60A5FA;
--color-primary-lighter: #1E3A8A;
```

#### Usage Guidelines

**When to Use:**

- CTA buttons (Install, Clone)
- Links and clickable elements
- Tags and categories
- Code highlight keywords
- GitHub integration elements

**Avoid Using:**

- Large area backgrounds (too harsh)
- Decorative elements
- Non-critical operations

**Usage Principle:** About 5-8% of page area

**Why Tech Blue?**
- Developer friendly: Blue represents technology and rationality
- GitHub style: Echoes GitHub blue
- Visual effect: Clear on dark background
- Industry characteristic: Common color for developer tools

### Background Colors

```css
/* Dark theme (default) */
--color-bg: #0D1117;           /* Main background - Deep blue-black */
--color-bg-secondary: #161B22; /* Secondary background */
--color-bg-tertiary: #21262D;   /* Auxiliary background */
--color-bg-elevated: #1C2128;   /* Floating layer */
--color-bg-card: #161B22;       /* Card background */

/* Light mode (optional) */
--color-bg-light: #FFFFFF;
--color-bg-secondary-light: #F6F8FA;
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
```

### Border Colors

```css
/* Dark mode */
--color-border: #30363D;
--color-border-light: #21262D;
--color-border-focus: #3B82F6;

/* Light mode */
--color-border-light-mode: #D0D7DE;
--color-border-subtle-light: #EAEAEF;
```

### Accent Colors

```css
/* Marketplace Dark Functional Colors */
--color-accent-green: #22C55E;   /* Green - Success/Active */
--color-accent-yellow: #EAB308;  /* Yellow - Warning/Pending */
--color-accent-red: #EF4444;     /* Red - Error/Deprecated */
--color-accent-purple: #8B5CF6;  /* Purple - Premium/Featured */
--color-accent-orange: #F97316;  /* Orange - Trending/Hot */
```

#### Functional Color Guidelines

- Success/Active: Green #22C55E
- Warning/Pending: Yellow #EAB308
- Error/Deprecated: Red #EF4444
- Premium/Featured: Purple #8B5CF6
- Trending/Hot: Orange #F97316

---

## Interaction Philosophy

### Animation Principles

**Fast, Smooth, Efficient**

Developer marketplaces need efficient browsing experience, animations should be fast and smooth.

#### State Feedback

- Focus: Border highlight (blue) + glow
- Hover: Slight background change (#161B22)
- Click: Slight scale (scale 0.98)

#### Transition Duration

- Fast: 100ms (button hover)
- Normal: 150ms (panel expand)
- Slow: 200ms (page transition)

**Why So Fast?**
- Developers need efficient browsing
- Fast response improves experience
- Maintains smoothness

#### Animations to Avoid

- Rotating spinners (use linear indicators)
- Bounce effects (unprofessional)
- Complex 3D effects (too flashy)
- Long animations (> 200ms)

### Feedback Mechanisms

**Instant, Clear, Professional**

- Button click: Immediate background change
- Card hover: Immediately show action buttons
- Operation success: Green prompt (1.5s auto-dismiss)
- Operation failure: Red prompt + error explanation
- Loading state: Skeleton screen or linear indicator

---

## Layout Principles

### Spacing Strategy

**4px Grid System**

- All spacing is multiples of 4
- Compact layout, high information density
- Suitable for developer tool standards

**Common Spacing:**

- Small spacing: 4px, 8px (related elements)
- Medium spacing: 12px, 16px (inside components)
- Large spacing: 24px, 32px (between modules)

### Compact Layout

**Information Density First**

Developer marketplaces need to display lots of resources:

- Button height: 32-36px (compact)
- Spacing: 8-12px (dense)
- Font size: 13-14px (body)
- Line height: 1.4-1.5 (compact)

**Why So Compact?**
- Screen space is precious
- Developers are used to dense information
- Improves browsing efficiency

### Content Max Width

- Resource list: Unlimited (full width)
- Content area: 1400px
- Sidebar: 280px
- Mobile: 100% (full width)

---

## Component Design Decisions

### Resource Cards

#### Why Compact Cards?

- High information density
- Quick browsing
- Efficient display

#### Why Code-Style Design?

- Developer friendly
- Strong technical feel
- Consistent with GitHub style

#### Why Show Action Buttons on Hover?

- Doesn't disturb static state
- Available when needed
- Keeps interface clean

### Search and Filter

#### Why Fixed at Top?

- Always available
- Quick access
- Matches user habits

#### Why Code-Style Prompts?

- Strong technical feel
- Developer friendly
- Visual recognition

### Quality Metrics

#### Why Show Stars and Downloads?

- Quality signals
- Quick judgment
- Community trust

#### Why Icon Display?

- Saves space
- Quick recognition
- Visual clarity

### Tags and Categories

#### Why Small Tag Design?

- Quick categorization
- Doesn't take space
- Visual rhythm

#### Why Colorful Tags?

- Quick distinction
- Enhanced recognition
- Improved efficiency

---

## Application Scenarios

### Scenario 1: Developer Marketplace

**Core Applications:**

- Dark theme
- Code-style design
- Resource card display
- Search and filter

**Adjustments:**

- Maintain compact layout
- Strengthen search function
- Optimize resource display

### Scenario 2: Open Source Project Directory

**Core Applications:**

- GitHub integration
- Project cards
- Quality metrics
- Categories and tags

**Adjustments:**

- Strengthen GitHub integration
- Optimize project info
- Add contributor display

### Scenario 3: Technical Resource Platform

**Core Applications:**

- Resource categories
- Filter and sort
- Favorite and share
- Ratings and reviews

**Adjustments:**

- Add user features
- Strengthen community interaction
- Optimize discovery mechanism

### Scenario 4: Plugin Marketplace

**Core Applications:**

- Plugin display
- Installation guide
- Version history
- Compatibility info

**Adjustments:**

- Strengthen installation flow
- Optimize version display
- Add compatibility notes

### Scenario 5: API Documentation Center

**Core Applications:**

- API list
- Code examples
- Parameter descriptions
- Request/Response

**Adjustments:**

- Strengthen code display
- Optimize example code
- Add testing features

---

## Common Mistakes

### Common Errors

#### Error 1: Overusing Blue

- Wrong: All buttons, all icons use blue
- Correct: Restrained accents, not exceeding 8% of page area
- Reason: Loses professionalism, appears cluttered

#### Error 2: Information Density Too Low

- Wrong: Too much whitespace, too large font sizes
- Correct: Compact layout, maintain information density
- Reason: Loses developer tool character

#### Error 3: Border Radius Too Large

- Wrong: 12px, 16px large border-radius
- Correct: 4-6px small border-radius
- Reason: Loses technical feel

#### Error 4: Animations Too Slow

- Wrong: 300ms, 500ms slow transitions
- Correct: 100-150ms fast response
- Reason: Affects browsing efficiency

#### Error 5: Ignoring Dark Mode

- Wrong: Light mode primarily
- Correct: Dark mode primarily
- Reason: Developers prefer dark

#### Error 6: Inconsistent Code Style

- Wrong: Mixing multiple code styles
- Correct: Unified code style (GitHub style)
- Reason: Loses professionalism

### Negative Checklist

- Don't overuse blue, restrained accents (<= 8%)
- Don't lower information density, maintain compact layout
- Don't use large border-radius (> 6px), use small (4-6px)
- Don't use slow animations (> 200ms), use fast (100-150ms)
- Don't ignore dark mode, prioritize dark
- Don't mix code styles, maintain consistency
- Don't ignore quality metrics, show stars and downloads

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
/* Code-style font */
--font-family: 'Inter', -apple-system, BlinkMacSystemFont, sans-serif;
--font-family-mono: 'JetBrains Mono', 'SF Mono', 'Fira Code', Consolas, monospace;
--font-family-code: 'Fira Code', 'JetBrains Mono', monospace;
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
```

---

## Border Radius System

```css
--radius-sm: 4px;
--radius-md: 6px;
--radius-lg: 8px;
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
  font-family: 'Inter', sans-serif;
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

.btn-secondary:hover {
  background: #30363D;
}

.btn-ghost {
  background: transparent;
  color: #3B82F6;
  border: none;
}

.btn-ghost:hover {
  background: #161B22;
}
```

### Resource Cards

```css
.resource-card {
  background: #161B22;
  border: 1px solid #30363D;
  border-radius: 6px;
  padding: 16px;
  transition: all 0.2s ease-out;
}

.resource-card:hover {
  border-color: #3B82F6;
  box-shadow: 0 0 0 1px #3B82F6;
}

.resource-header {
  display: flex;
  align-items: center;
  gap: 12px;
  margin-bottom: 12px;
}

.resource-icon {
  width: 40px;
  height: 40px;
  border-radius: 6px;
  background: #21262D;
}

.resource-title {
  font-size: 16px;
  font-weight: 600;
  color: #E6EDF3;
  margin-bottom: 4px;
}

.resource-meta {
  font-size: 12px;
  color: #8B949E;
  font-family: 'Fira Code', monospace;
}

.resource-description {
  font-size: 13px;
  color: #8B949E;
  line-height: 1.5;
  margin-bottom: 12px;
}

.resource-stats {
  display: flex;
  gap: 16px;
  font-size: 12px;
  color: #6E7681;
}

.resource-stat {
  display: flex;
  align-items: center;
  gap: 4px;
}
```

### Code Blocks

```css
.code-block {
  background: #0D1117;
  border: 1px solid #30363D;
  border-radius: 6px;
  padding: 12px;
  font-family: 'Fira Code', monospace;
  font-size: 13px;
  line-height: 1.5;
  overflow-x: auto;
}

/* Syntax highlighting (example) */
.syntax-keyword { color: #FF7B72; }
.syntax-string { color: #A5D6FF; }
.syntax-comment { color: #8B949E; }
.syntax-function { color: #D2A8FF; }
.syntax-number { color: #79C0FF; }
.syntax-variable { color: #FFA657; }
```

### Search Box

```css
.search-box {
  position: relative;
  width: 100%;
  max-width: 400px;
}

.search-input {
  width: 100%;
  height: 36px;
  padding: 0 12px 0 40px;
  font-size: 13px;
  font-family: 'Inter', sans-serif;
  border: 1px solid #30363D;
  border-radius: 6px;
  background: #0D1117;
  color: #E6EDF3;
  transition: all 0.15s ease-out;
}

.search-input:focus {
  outline: none;
  border-color: #3B82F6;
  box-shadow: 0 0 0 2px rgba(59, 130, 246, 0.3);
}

.search-icon {
  position: absolute;
  left: 12px;
  top: 50%;
  transform: translateY(-50%);
  color: #6E7681;
  pointer-events: none;
}

.search-placeholder {
  color: #6E7681;
  font-family: 'Fira Code', monospace;
  font-size: 12px;
}
```

### Tags

```css
.tag {
  display: inline-block;
  padding: 2px 8px;
  font-size: 11px;
  font-weight: 500;
  border-radius: 12px;
  font-family: 'Inter', sans-serif;
  transition: all 0.15s ease-out;
}

.tag-default {
  background: #21262D;
  color: #8B949E;
}

.tag-primary {
  background: #1E3A8A;
  color: #60A5FA;
}

.tag-success {
  background: #162D1E;
  color: #22C55E;
}

.tag-warning {
  background: #2D2510;
  color: #EAB308;
}

.tag-error {
  background: #2D1212;
  color: #EF4444;
}
```

### Command Prompt

```css
.command-prompt {
  background: #0D1117;
  border: 1px solid #30363D;
  border-left: 3px solid #3B82F6;
  border-radius: 6px;
  padding: 12px;
  font-family: 'Fira Code', monospace;
  font-size: 12px;
  line-height: 1.6;
}

.command-prefix {
  color: #3B82F6;
  font-weight: 600;
}

.command-content {
  color: #E6EDF3;
}

.command-comment {
  color: #8B949E;
  font-style: italic;
}
```

### Quality Metrics

```css
.quality-metrics {
  display: flex;
  gap: 12px;
  font-size: 12px;
  color: #6E7681;
}

.metric {
  display: flex;
  align-items: center;
  gap: 4px;
}

.metric-icon {
  width: 14px;
  height: 14px;
}

.metric-value {
  font-weight: 600;
  color: #8B949E;
}

.metric-high {
  color: #22C55E;
}

.metric-medium {
  color: #EAB308;
}

.metric-low {
  color: #6E7681;
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

- Developer marketplaces
- Open source project directories
- Technical resource platforms
- Plugin marketplaces
- API documentation centers
- Tool resource sites
- Developer communities
- Technical blog aggregators
