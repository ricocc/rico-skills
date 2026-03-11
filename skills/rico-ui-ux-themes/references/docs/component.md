# Component Optimization Guide

> For general optimization workflow, see SKILL.md. This guide focuses on component design system thinking.

---

## First Principles of Components

**The mark of a great component: Users don't notice its existence.**

Good components:
- **Work Silently** — No learning required from users
- **Consistent Behavior** — Same actions produce same results
- **Clear States** — Users always know current state

> "Components should be invisible. If users notice the component, we've failed."
> — From Apple Human Interface Guidelines

---

## Professional Component Decision Framework

### Anti-Patterns (Based on Impeccable)

**DON'T use placeholder text as labels**—placeholders disappear on input, leaving users without context.

**DON'T remove focus indicators** without providing alternatives—it's an accessibility violation.

**DON'T make every button primary**—hierarchy matters. Use ghost buttons, text links, and secondary styles.

### 1. States are Complete

**Every component must consider all possible states (8 states):**

| State | Description | Design Focus |
|-------|-------------|--------------|
| **Default** | Initial state | Clearly identifiable |
| **Hover** | Mouse over | Subtle "interactive here" cue |
| **Focus** | Keyboard focus | Visible but not obtrusive (use `:focus-visible`) |
| **Active** | Pressed | Confirm action |
| **Disabled** | Unavailable | Clearly non-interactive |
| **Loading** | In progress | Show progress |
| **Error** | Problem | Clear problem explanation |
| **Success** | Completed | Confirmation feedback |

**Apple Approach**: Every Apple component has 10+ state combination tests.

### 2. Interaction Consistency

**Same interaction patterns, same component behavior.**

| Pattern | Apple | Airbnb |
|---------|-------|--------|
| Click | scale(0.97) + color | Ripple effect |
| Long Press | 3D Touch / Haptic | Preview |
| Swipe | Quick actions | Delete/Favorite |
| Drag | Lift effect | Reorder |

**Anti-pattern**: In the same app, some buttons are clickable, some aren't, with no visual distinction.

### 3. Feedback is Instant

**100ms Rule**:

- Click → Visual feedback < 100ms
- Action → Result confirmation < 300ms
- Loading → State display < 100ms

---

## Apple Component System

### Button Specifications

```
┌─────────────────────────────────────┐
│ Apple Button System                 │
├─────────────────────────────────────┤
│ Size:                               │
│ - Small:  31pt height               │
│ - Medium: 34pt (default)            │
│ - Large:  38pt                      │
├─────────────────────────────────────┤
│ Corner Radius:                      │
│ - Small:  6pt                       │
│ - Large:  8pt                       │
├─────────────────────────────────────┤
│ Typography:                         │
│ - SF Pro, 15pt, Semibold           │
├─────────────────────────────────────┤
│ States:                             │
│ - Default: opacity 1.0              │
│ - Hover:   subtle highlight         │
│ - Press:   scale(0.97) + darken     │
│ - Focus:   2pt ring                 │
│ - Disabled: opacity 0.4             │
└─────────────────────────────────────┘
```

### Input Field Specifications

```
┌─────────────────────────────────────┐
│ Apple Text Field                    │
├─────────────────────────────────────┤
│ Height: 44pt (touch target)         │
│ Padding: 12pt horizontal            │
│ Corner Radius: 8pt                  │
│ Border: 1pt, #E5E5EA                │
├─────────────────────────────────────┤
│ States:                             │
│ - Default: placeholder visible      │
│ - Focus: blue ring (2pt)            │
│ - Filled: placeholder hidden        │
│ - Error: red border + message       │
│ - Disabled: gray background         │
└─────────────────────────────────────┘
```

---

## IBM Carbon Component System

### Component Principles

- **Content is king**: Components always serve content
- **Accessibility first**: All components pass WCAG AAA
- **Lightweight**: Minimum code, maximum flexibility

### Button Variants

| Variant | Usage | Visual |
|---------|-------|--------|
| Primary | Main action | Solid blue |
| Secondary | Secondary action | Outlined |
| Ghost | Tertiary option | Transparent background |
| Danger | Dangerous action | Solid red |

---

## Focus Management

### Focus Visibility (Based on Impeccable)

**Never use `outline: none` without providing an alternative.** It's an accessibility violation.

Use `:focus-visible` to show focus only for keyboard users:

```css
/* Hide focus ring for mouse/touch */
button:focus {
  outline: none;
}

/* Show focus ring for keyboard */
button:focus-visible {
  outline: 2px solid var(--color-accent);
  outline-offset: 2px;
}
```

**Focus ring design principles**:
- High contrast (3:1 minimum against adjacent colors)
- 2-3px thick
- Offset from element (not inside it)
- Consistent across all interactive elements
```

### Focus Order

```html
<!-- Logical order -->
<nav>
  <a href="#">Skip to content</a>
  <button>Search</button>
  <button>Menu</button>
</nav>
```

---

## Component API Design

### Semantic Props

```jsx
// ❌ Bad
<Button primary large onClick={fn} />

// ✅ Good - Semantic
<Button variant="primary" size="lg" onPress={fn} />
```

### Controlled/Uncontrolled

```jsx
// Controlled component
<Input value={value} onChange={setValue} />

// Uncontrolled component
<Input defaultValue="initial value" ref={inputRef} />
```

---

## Output Format

### CSS Variables

```css
:root {
  /* Buttons */
  --btn-height-sm: 32px;
  --btn-height-md: 40px;
  --btn-height-lg: 48px;
  --btn-radius: 8px;
  --btn-font-weight: 600;

  /* Inputs */
  --input-height: 44px;
  --input-radius: 8px;
  --input-border: 1px solid #E5E5EA;
  --input-focus-ring: 2px solid #007AFF;

  /* Focus */
  --focus-ring: 2px;
  --focus-ring-offset: 2px;
}
```

### React Component

```jsx
const Button = ({
  variant = 'primary',  // primary | secondary | ghost
  size = 'md',         // sm | md | lg
  loading = false,
  disabled = false,
  children,
  ...props
}) => {
  return (
    <button
      className={`btn btn-${variant} btn-${size}`}
      disabled={disabled || loading}
      {...props}
    >
      {loading && <Spinner />}
      {children}
    </button>
  );
};
```

---

## Checklist (Designer Perspective)

- [ ] All states designed?
- [ ] Focus state keyboard accessible?
- [ ] Disabled state clearly non-interactive?
- [ ] Loading state has feedback?
- [ ] Error state has explanation?
- [ ] Interactions consistent (same behavior for same operations)?
- [ ] Component "works silently"?

---

## Professional Terminology

| Term | Definition |
|------|------------|
| **Variant** | Style variation |
| **State** | Current condition |
| **Disabled** | Unavailable state |
| **Loading** | In progress state |
| **Focus Ring** | Visual focus indicator |
| **Touch Target** | Touchable area size |
| **Hit Area** | Clickable region |
| **Prop** | Component property |
| **Controlled** | Parent-controlled component |
| **Uncontrolled** | Self-managed component |
