# Motion Optimization Guide

> For general optimization workflow, see SKILL.md. This guide focuses on motion design decisions.

---

## First Principles of Motion

**Motion is not decoration, it's information.**

Good motion helps users:
- **Understand** — State changes have cause and effect
- **Anticipate** — Know what results an action will produce
- **Enjoy** — Interactions have "weight" and "physical realism"

> Jony Ive: "Motion should be as natural as real-world physics. When you let go, things fall; when you push things, they move."
>
> "The best animations are invisible. They just make things feel right."

---

## Professional Motion Decision Framework

### 1. Physics-based

**The real world doesn't have bounce and elastic.**

| Real Physics | Motion Expression |
|--------------|-------------------|
| Objects have weight | Motion has duration |
| Friction | Easing curve deceleration |
| Limited elasticity | Slight overshoot acceptable |
| Energy conservation | Entrance slower than exit |

**Apple Approach**:
- Spring animations (with spring force but limited)
- No "cartoon-style" bouncing

### 2. Feedback is Confirmation

**Every action should have visual feedback.**

| Action | Feedback | Duration |
|--------|----------|----------|
| Button click | Scale down + color change | 100ms |
| Form submit | Loading + success | Instant + confirmation |
| Toggle switch | Slide + color | 200ms |
| Menu expand | Slide in + fade in | 250ms |

**Core Principle**: Users should never doubt "Did my click register?"

### 3. State is Story

**Motion helps users understand changes.**

| Scenario | Motion Narrative |
|----------|------------------|
| Expand details | "More content appearing" |
| Open modal | "Modal overlaying current view" |
| Delete item | "Item disappears, others move to fill" |
| Page transition | "Going to a new place" |

---

## Apple Motion Philosophy

### Spring Animation

```swift
// Apple Spring Animation
UIView.animate(
    withDuration: 0.5,
    delay: 0,
    usingSpringWithDamping: 0.7,  // Damping
    initialSpringVelocity: 0.5,   // Initial velocity
    options: [],
    animations: { view.transform = .identity }
)
```

**Parameter Meaning**:
- Damping: Damping (0-1), lower = more springy
- Velocity: Initial velocity

### Common Parameters

| Motion Type | Duration | Damping |
|-------------|----------|---------|
| Button feedback | 100ms | 0.8 |
| Menu expand | 250ms | 0.7 |
| Page transition | 350ms | 0.85 |
| Modal appear | 300ms | 0.75 |

---

## Professional Duration Guide

### 100/300/500 Rule

| Duration | Perception | Usage |
|----------|------------|-------|
| **50-100ms** | Instant | Button clicks, toggles |
| **150-200ms** | Fast | Hover, focus |
| **250-300ms** | Natural | Menus, expand |
| **350-400ms** | Smooth | Page transitions |
| **500ms+** | Formal | Large animations |

**Golden Rule**: If users need to "wait" for an animation, it's too slow.

---

## Easing Curves

### Physics Easing vs Curve Easing

```
Physics Easing: Spring (natural, elastic)
Curve Easing: Bezier (precise, predictable)
```

### Recommended Easings

```css
/* Fast exit, natural deceleration */
--ease-out-quart: cubic-bezier(0.25, 1, 0.5, 1);

/* More dramatic */
--ease-out-quint: cubic-bezier(0.22, 1, 0.36, 1);

/* Confident and decisive */
--ease-out-expo: cubic-bezier(0.16, 1, 0.3, 1);

/* Smooth in and out */
--ease-in-out: cubic-bezier(0.65, 0, 0.35, 1);
```

### Spring Effect (CSS)

```css
/* Simulate Apple Spring */
@keyframes spring {
  0% { transform: scale(0.95); }
  60% { transform: scale(1.02); }
  100% { transform: scale(1); }
}
```

---

## Performance is Experience

### GPU Acceleration Principles

**Only animate two properties**:

```css
/* ✅ Correct - GPU accelerated */
transform: translateX(100px);
opacity: 0.5;
filter: blur(5px);

/* ❌ Wrong - Triggers reflow */
width: 100px;
height: 100px;
margin: 10px;
padding: 10px;
top: 10px;
left: 10px;
```

### Height Animation Technique

```css
/* ❌ Animating height triggers reflow */
height: auto;
transition: height 0.3s;

/* ✅ Use grid-template-rows */
display: grid;
grid-template-rows: 0fr;
transition: grid-template-rows 0.3s;

.card-expanded {
  grid-template-rows: 1fr;
}
```

---

## Accessibility

### prefers-reduced-motion

```css
/* Respect user preference */
@media (prefers-reduced-motion: reduce) {
  *, *::before, *::after {
    animation-duration: 0.01ms !important;
    transition-duration: 0.01ms !important;
  }
}
```

### Preserve Functional Motion

```css
/* Keep progress bar */
@media (prefers-reduced-motion: reduce) {
  .progress-bar {
    animation: none;
    /* Still visible, but static */
  }
}
```

---

## Output Format

### CSS Variables

```css
:root {
  /* Durations */
  --duration-instant: 50ms;
  --duration-fast: 100ms;
  --duration-normal: 200ms;
  --duration-slow: 300ms;
  --duration-slower: 400ms;

  /* Easings */
  --ease-out-quart: cubic-bezier(0.25, 1, 0.5, 1);
  --ease-out-expo: cubic-bezier(0.16, 1, 0.3, 1);
  --ease-in-out: cubic-bezier(0.65, 0, 0.35, 1);

  /* Combinations */
  --transition-fast: all var(--duration-fast) var(--ease-out-quart);
  --transition-normal: all var(--duration-normal) var(--ease-out-expo);
}
```

### Tailwind Extension

```javascript
// tailwind.config.js
theme: {
  extend: {
    transitionDuration: {
      '100': '100ms',
      '200': '200ms',
      '300': '300ms',
    },
    transitionTimingFunction: {
      'spring': 'cubic-bezier(0.25, 1, 0.5, 1)',
    }
  }
}
```

---

## Motion Anti-Patterns (Based on Impeccable)

**DON'T use bounce or elastic easing**—these were trendy in 2015 but now feel tacky and amateurish. Real objects don't bounce when they stop—they decelerate smoothly.

**DON'T animate layout properties** (width, height, padding, margin)—use transform and opacity only. Animating layout properties triggers reflow and hurts performance.

**DON'T animate everything**—animation fatigue is real. Use purposeful animations that enhance understanding.

**DON'T ignore prefers-reduced-motion**—35% of adults over 40 have vestibular disorders. This is not optional.

---

## Checklist (Designer Perspective)

- [ ] Does the motion have physical meaning?
- [ ] Is there immediate feedback after user action?
- [ ] Is the duration "instant"? (<300ms)
- [ ] Is reduced motion supported?
- [ ] Are only transform/opacity used?
- [ ] Does it enhance understanding rather than distract?

---

## Professional Terminology

| Term | Definition |
|------|------------|
| **Spring** | Spring animation |
| **Damping** | Damping coefficient |
| **Easing** | Easing curve |
| **Overshoot** | Overshoot effect |
| **Stagger** | Staggered animation |
| **Motion Path** | Motion path |
| **Parallax** | Parallax effect |
| **Keyframe** | Keyframe |
| **FPS** | Frames per second |
| **GPU Acceleration** | GPU acceleration |
