# Notion Style

Warm, Friendly, Human, Minimal

---

## Design Philosophy

### Brand Philosophy

**"Block-Based Thinking"**

Notion's design philosophy centers around "everything is a block." Each piece of content is an independent block that can be freely combined, dragged, and nested. Design conveys infinite possibilities and creative freedom through warm paper-like texture and soft blue.

### Design Philosophy

1. **Block-Driven - Modular Thinking**
   - Each piece of content is an independent block
   - Free combination, dragging, nesting
   - Progressive complexity

2. **Minimal Low Noise - Content is King**
   - Interface recedes, content stands out
   - Remove decorative elements
   - Paper-like texture, as natural as writing

3. **Warm and Friendly - Human Care**
   - Parchment white (#F7F6F3) instead of pure white
   - Deep brown-gray text (#37352F) instead of pure black
   - Soft shadows, not harsh

4. **User as Builder - Flexible and Malleable**
   - Highly customizable
   - Low cognitive load
   - Supports multiple workflows

### Core Keywords

- Flexible
- Minimal
- Block-Based
- Warm
- Collaborative

---

## Overview

Notion style originates from Notion official website (notion.so)—warm, friendly, modular. Suitable for collaboration tools, knowledge management, content products.

**Core Philosophy**: Block-driven, progressive complexity, minimal low noise, user as builder.

**Style Positioning**: Minimal writing style, block-based modular, lightweight customizable, cross-scenario collaboration, low cognitive load.

**Character**: Calm, inclusive, flexible, efficient, growable.

---

## Color System

### Brand Color

```css
/* Notion Blue - Used for primary buttons, links, selected states, command panel accent */
--color-primary: #2E75CC;
--color-primary-hover: #1A56DB;
--color-primary-light: #EBF5FF;
```

#### Usage Guidelines

**When to Use:**

- Add buttons (+ New)
- Links and clickable text
- Selected states, active states
- Command panel accent
- Block handles (shown on hover)

**Avoid Using:**

- Large area backgrounds
- Non-critical action buttons
- Decorative elements

**Usage Principle:** Not exceeding 5% of page area

**Why Soft Blue?**
- Trust: Blue conveys reliability
- Friendly: Not too cold
- Distinction: Clearly visible on white background
- Notion brand identity

### Background Colors

```css
/* Light mode - Parchment white */
--color-bg: #FFFFFF;           /* Page background */
--color-bg-block: #F7F6F3;     /* Block background/card - core */
--color-bg-secondary: #F5F4ED;
--color-bg-tertiary: #F0EFED;

/* Dark mode */
--color-bg-dark: #191919;
--color-bg-block-dark: #272727;
--color-bg-secondary-dark: #1F1E1D;
```

### Text Colors

```css
/* Light mode */
--color-text: #37352F;          /* Deep brown-gray - Primary text */
--color-text-secondary: #64748B; /* Slate gray */
--color-text-tertiary: #9CA3AF;
--color-text-disabled: #A1A1AA;

/* Dark mode */
--color-text-dark: #EAE9E7;
--color-text-secondary-dark: #94A3B8;
```

### Border Colors

```css
/* Light mode */
--color-border: #E9E9E7;
--color-border-hover: #D4D4D4;

/* Dark mode */
--color-border-dark: #373737;
```

#### Why Extremely Light Borders?

- Almost invisible, doesn't compete with content
- Only used to distinguish areas
- Maintains "white paper" texture

### Functional Colors (Restrained Use)

**Note**: Functional colors are only for content-level auxiliary use, not for UI decoration.

```css
/* Success */
--color-success: #059669;
--color-success-bg: #ECFDF5;

/* Warning */
--color-warning: #D97706;
--color-warning-bg: #FFFBEB;

/* Error */
--color-error: #DC2626;
--color-error-bg: #FEF2F2;

/* Info */
--color-info: #2563EB;
--color-info-bg: #EFF6FF;

/* Gray (default) */
--color-gray: #6B7280;
```

---

## Interaction Philosophy

### Animation Principles

**Natural, Smooth, Non-Intrusive**

#### Block Operations

- Hover: Show handle (left 6 dots)
- Drag: Semi-transparent shadow
- Nest: Indent 20px
- Expand/Collapse: 150ms ease-out

#### State Feedback

- Focus: Light blue background (#EBF5FF)
- Hover: Extremely light gray (#F5F4ED)
- Selected: Blue left border (2px)

#### Transition Duration

- Fast: 150ms (block expand)
- Normal: 200ms (page transition)
- Slow: 300ms (modal)

**Why So Natural?**
- Smooth as writing
- Doesn't interrupt train of thought
- Reduces cognitive load

#### Animations to Avoid

- Rotation, bounce, zoom
- Complex 3D effects
- Flashy transitions
- Shadow gradients

### Feedback Mechanisms

**Soft, Friendly**

- Block focus: Light blue background
- Drag: Preview shadow
- Operation success: Top notification (2s auto-dismiss)
- Operation failure: Red border + inline prompt

---

## Layout Principles

### Spacing Strategy

**Comfortable and Generous**

**Standard Spacing System:**

- Minimum: 4px
- Small spacing: 8px, 12px
- Medium spacing: 16px, 20px
- Large spacing: 24px, 32px
- Extra large: 48px, 64px

**Why Larger Than Linear?**
- Notion is a content tool, needs breathing room
- Whitespace makes content more readable
- Reduces visual fatigue

### Block-Based Layout

**Everything is a Block**

- Each paragraph, list, image is a block
- Blocks can be operated independently
- Blocks can be nested (indent 20px/40px/60px)
- 12px spacing between blocks

**Why Block-Driven?**
- Flexibility: Free combination
- Readability: Independent units
- Editability: Drag to reorder

### Content Max Width

- Document content: 900px (optimal reading width)
- Database: Full width
- Sidebar: 240px
- Line height: 1.6-1.8 (reading friendly)

---

## Component Design Decisions

### Block

#### Why Is Every Content a Block?

- Unified operation method
- Supports dragging and nesting
- Progressive complexity
- Reduces learning curve

#### Why Show Handle on Hover?

- Doesn't disturb reading
- Only appears when needed
- 6-dot icon: drag, delete, copy, etc.

### Buttons

#### Why 28px Height?

- Slightly larger than Linear (28px vs 28px)
- Smaller than Airbnb (48px)
- Moderate size

#### Why Soft Blue?

- Brand identity
- Friendly not cold
- Clear on white background

### Cards/Pages

#### Why Parchment White (#F7F6F3)?

- Warmth: Distinguishes from pure white
- Writing feel: As natural as paper
- Reduced contrast: Less eye strain

#### Why Extremely Light Borders?

- Almost invisible
- Only for distinction
- Doesn't compete with content

### Database

#### Why Compact Table Cells?

- High information density
- More data per screen
- Quick browsing

**But Maintains:**
- Row height: 32px (not 28px)
- Spacing: 12px (comfortable)
- Font size: 13px (readable)

---

## Application Scenarios

### Scenario 1: Knowledge Management Tool

**Core Applications:**

- Block-based editor
- Parchment white background (#F7F6F3)
- Nested page structure
- Soft blue accent

**Adjustments:**

- Support block dragging
- Support block nesting
- Keyboard shortcuts priority (Cmd+/)

### Scenario 2: Collaboration Tool

**Core Applications:**

- Real-time collaboration cursors
- Comments and discussions
- @ mentions
- Sharing and permissions

**Adjustments:**

- Show collaborator avatars
- Collaboration cursors (soft colors)
- Comment sidebar

### Scenario 3: Project Management

**Core Applications:**

- Database views (table, kanban, calendar)
- Task blocks
- Tags and properties
- Progress tracking

**Adjustments:**

- Multi-view switching
- Filter and sort
- Custom properties

### Scenario 4: Personal Notes

**Core Applications:**

- Clean note editing
- Quick capture
- Tag organization
- Full-text search

**Adjustments:**

- Minimal interface
- Quick start (Cmd+N)
- Mobile friendly

### Scenario 5: Team Documentation

**Key Adjustments:**

- Permission management
- Version history
- Publishing and sharing
- Custom domain

**Keep Unchanged:**

- Block-based editing
- Parchment background
- Soft blue

---

## Common Mistakes

### Common Errors

#### Error 1: Overusing Blue

- Wrong: All buttons, all borders use blue
- Correct: Sparingly applied, not exceeding 5% of page area
- Reason: Loses minimal aesthetic, appears cluttered

#### Error 2: Using Pure White Background

- Wrong: #FFFFFF pure white background
- Correct: #F7F6F3 parchment white
- Reason: Loses warmth, looks like ordinary document tool

#### Error 3: Block Spacing Too Large

- Wrong: 24px, 32px block spacing
- Correct: 12px, 16px
- Reason: Loses compact feel, wastes space

#### Error 4: Using Dark Text

- Wrong: #000000 pure black text
- Correct: #37352F deep brown-gray
- Reason: Contrast too high, eye strain

#### Error 5: Borders Too Dark

- Wrong: #CCCCCC, #AAAAAA dark borders
- Correct: #E9E9E7 extremely light borders
- Reason: Competes with content, loses "white paper" texture

#### Error 6: Over-Decoration

- Wrong: Gradients, shadows, too many icons
- Correct: Minimal, let content speak
- Reason: Increases cognitive load, interrupts writing

### Negative Checklist

- Don't use pure white (#FFFFFF), use parchment white (#F7F6F3)
- Don't use pure black (#000000), use deep brown-gray (#37352F)
- Don't use dark borders (> #E5E5E5), use extremely light borders (#E9E9E7)
- Don't over-decorate, maintain minimal
- Don't use high saturation colors, use soft colors
- Don't fix layout, use block-based modular
- Don't use complex animations, use natural smooth

---

## Typography System

### Font Family

```css
/* Default - General editing, collaboration */
--font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, Helvetica, Arial, sans-serif;

/* Serif - Long form, documents, books */
--font-family-serif: Georgia, Times New Roman, Times, serif;

/* Monospace - Code blocks, technical docs */
--font-family-mono: SFMono-Regular, Menlo, Consolas, monospace;
```

### Font Size Scale

**Follow "Few Levels, Strong Distinction" Principle**

```css
/* H1 - Page title */
--font-size-h1: 40px;
--line-height-h1: 1.2;

/* H2 - Section title */
--font-size-h2: 28px;
--line-height-h2: 1.3;

/* H3 - Subsection title */
--font-size-h3: 20px;
--line-height-h3: 1.4;

/* Body */
--font-size-body: 16px;
--line-height-body: 1.6;

/* Small text - Notes, timestamps */
--font-size-sm: 14px;
--line-height-sm: 1.5;

/* Code */
--font-size-code: 15px;
--line-height-code: 1.5;
```

### Font Weights

```css
--font-weight-normal: 400;
--font-weight-medium: 500;
--font-weight-semibold: 600;
```

---

## Spacing System

### Base Spacing

**4px Grid System**

```css
--space-1: 4px;
--space-2: 8px;      /* Fixed block spacing */
--space-3: 12px;     /* Text block padding */
--space-4: 16px;     /* Card padding */
--space-5: 20px;
--space-6: 24px;      /* Page padding */
--space-8: 32px;
--space-10: 40px;
--space-12: 48px;
```

### Common Sizes

```css
/* Buttons */
--btn-height-sm: 32px;
--btn-height-base: 40px;

/* Inputs */
--input-height: 40px;
--input-padding: 12px;

/* Icons */
--icon-size-sm: 16px;
--icon-size-md: 20px;
--icon-size-lg: 24px;

/* Page */
--page-padding: 24px;
--page-max-width: 1440px;

/* Sidebar */
--sidebar-width: 240px;
--sidebar-max-width: 320px;
```

---

## Border Radius System

**Globally Unified**

```css
--radius-sm: 4px;   /* Tags, badges */
--radius-md: 6px;    /* Buttons, inputs, cards, blocks, code blocks */
--radius-lg: 8px;
--radius-xl: 12px;
--radius-full: 9999px;
```

---

## Shadows

**Only for Floating and Level Distinction**

```css
--shadow-sm: 0 1px 2px rgba(0, 0, 0, 0.03);      /* Block floating */
--shadow-md: 0 2px 4px rgba(0, 0, 0, 0.05);      /* Cards */
--shadow-lg: 0 4px 12px rgba(0, 0, 0, 0.1);       /* Popups */
```

---

## Component Specifications

### Buttons

```css
/* Primary button */
.btn-primary {
  background: #2E75CC;
  color: white;
  height: 40px;
  padding: 0 20px;
  border-radius: 6px;
  font-weight: 500;
}

.btn-primary:hover {
  background: #1A56DB;
}

/* Secondary button */
.btn-secondary {
  background: transparent;
  border: 1px solid #E9E9E7;
  color: #37352F;
  height: 40px;
  padding: 0 20px;
  border-radius: 6px;
}

/* Ghost button */
.btn-ghost {
  background: transparent;
  color: #2E75CC;
  height: 32px;
  padding: 0 12px;
}

.btn-ghost:hover {
  text-decoration: underline;
}

/* Block action button */
.btn-block-action {
  width: 24px;
  height: 24px;
  border-radius: 50%;
  background: transparent;
}
```

### Inputs

```css
.input {
  height: 40px;
  padding: 0 12px;
  border: 1px solid #E9E9E7;
  border-radius: 6px;
  background: white;
  font-size: 14px;
}

.input:focus {
  outline: none;
  border-color: #2E75CC;
}

.input::placeholder {
  color: #A1A1AA;
  font-style: normal;
}

.input-error {
  border-color: #DC2626;
}

.input-error-message {
  font-size: 14px;
  color: #DC2626;
  margin-top: 4px;
}
```

### Cards

```css
.card {
  background: #F7F6F3;
  border: 1px solid #E9E9E7;
  border-radius: 6px;
  padding: 16px;
}
```

### Block Components

```css
/* Block selected state */
.block {
  padding: 12px;
}

.block-selected {
  background: #EBF5FF;
}

.block-dragging {
  opacity: 0.8;
  transform: scale(0.98);
  box-shadow: 0 2px 4px rgba(0, 0, 0, 0.05);
}

/* Quote block */
.block-quote {
  border-left: 2px solid #2E75CC;
  padding: 12px;
  background: #F3F4F6;
}

/* Code block */
.block-code {
  background: #F7F6F3;
  padding: 16px;
  border-radius: 6px;
  font-family: SFMono-Regular, Menlo, Consolas, monospace;
  font-size: 15px;
}
```

### Command Panel

```css
.command-panel {
  background: white;
  border-radius: 6px;
  box-shadow: 0 4px 12px rgba(0, 0, 0, 0.1);
  width: 400px;
}

.command-panel-item-selected {
  background: #EBF5FF;
}
```

---

## Animations

### Parameters

```css
/* Fast transitions, don't affect operations */
--duration-fast: 150ms;
--duration-normal: 200ms;
--duration-slow: 250ms;

--ease-out: ease-in-out;
```

### Allowed Animations

```css
/* Block interactions */
.block-hover {
  transition: background-color 150ms ease-in-out;
}

/* Selection */
.block-selected {
  transition: background-color 150ms ease-in-out;
}

/* Dragging */
.block-dragging {
  transition: transform 150ms ease-in-out, opacity 150ms ease-in-out;
}

/* Command panel */
.panel-popup {
  animation: fadeInUp 150ms ease-out;
}

@keyframes fadeInUp {
  from {
    opacity: 0;
    transform: translateY(4px);
  }
  to {
    opacity: 1;
    transform: translateY(0);
  }
}

/* Collapse expand */
.collapse {
  transition: height 200ms ease-in-out;
}
```

### Forbidden Animations

- Rotation, bounce, flashing, shaking
- Auto-playing animations
- Long animations (>300ms)
- Complex transitions, 3D effects

---

## Responsive

### Breakpoints

```css
--breakpoint-sm: 640px;
--breakpoint-md: 768px;
--breakpoint-lg: 1200px;
--breakpoint-xl: 1440px;
```

### Adaptation Rules

| Device | Breakpoint | Layout Rules |
|--------|-----------|--------------|
| Mobile | <768px | Single column layout, blocks cannot be dragged into columns, sidebar collapses to hamburger menu |
| Tablet | 768-1199px | Two columns optional, sidebar fixed open |
| Desktop | >=1200px | Multi-column free layout, page max width 1440px |

---

## Best For

- Collaboration tools
- Knowledge management
- Personal notes
- Educational platforms
- Content creation
- Team wikis
- Project documentation
- Database kanban
