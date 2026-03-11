# Layout Optimization Guide

> For general optimization workflow, see SKILL.md. This guide focuses on space and layout design decisions.

---

## First Principles of Layout

**Space is Information.**

Distance between elements = Relationship between elements.

- **Close** = Related
- **Far** = Independent
- **Whitespace** = Important

> "Whitespace is the most important, most underutilized element in design."
> — Massimo Vignelli

---

## Professional Layout Decision Framework

### 1. Visual Flow

**Question: How does the user's eye move?**

| Pattern | Use Case | Examples |
|---------|----------|----------|
| **F-pattern** | Text-heavy pages | Blogs, documentation |
| **Z-pattern** | Marketing landing pages | Landing Page |
| **Central** | Single focus | Detail pages, modals |
| **Grid** | Content browsing | Lists, galleries |

**Apple Approach**: iOS interfaces use F-pattern, content left-aligned, important actions on the left.

### 2. Proximity Principle

**From "The Non-Designer's Design Book":**

```
Related elements together
Unrelated elements apart

Distance = Relationship
```

**Case Comparison**:

```
❌ Wrong:
[Title] [Subtitle]
[Body content...]
---
[Another title]

✅ Correct:
[Title]
[Subtitle]
[Body content...]
─────────────
[Another title]
```

### 3. Container Thinking

**All content should have a "home".**

| Container Type | Apple Example | Airbnb Example |
|----------------|---------------|----------------|
| Card | App Store card | Property card |
| Section | Settings group | Filter panel |
| Sheet | Bottom slide-up | Detail modal |
| Dialog | Confirmation popup | Booking confirmation |

**Anti-pattern**: Content stacked directly without visual boundaries.

---

## Grid System

### Anti-Patterns (Based on Impeccable)

**DON'T use 8pt grid exclusively**—8pt is too coarse. You'll frequently need 12px (between 8 and 16), which breaks the system.

**Use 4pt base grid for granularity**: 4, 8, 12, 16, 24, 32, 48, 64, 96

**DON'T nest cards inside cards**—visual noise that flattens hierarchy. Use spacing, typography, and subtle dividers instead.

### Apple Grid (8pt Grid)

```
Base unit = 8px

8, 16, 24, 32, 40, 48, 64, 80, 96...
```

### IBM Grid (1px Grid)

```
Base unit = 1px (more precise)

1, 2, 4, 8, 16, 24, 32, 48, 64...
```

### Container Queries (Modern Responsive)

```css
/* Component-level responsive */
.card-container {
  container-type: inline-size;
  container-name: card;
}

@container card (min-width: 400px) {
  .card {
    display: grid;
    grid-template-columns: 1fr 2fr;
  }
}
```

---

## Responsive Strategy

### Apple Responsive Philosophy

**Content is like water.**

- iPhone: Full-width layout
- iPad: Sidebar + main content
- Mac: Multi-column layout

**Breakpoint Strategy**:

| Device | Breakpoint | Layout |
|--------|------------|--------|
| iPhone SE | <375px | Single column |
| iPhone | 375-414px | Single column |
| iPad Portrait | 768px | Two columns |
| iPad Landscape | 1024px | Sidebar + content |
| Mac | 1440px | Multi-column |

### Mobile First

```
1. Design mobile first (most constrained)
2. Progressively enhance to desktop

Ask at each step: How does larger screen "enhance" rather than "copy"?
```

---

## Spacing System

### Professional Spacing Ratios

```
base = 8px (Apple)
base = 4px (IBM)

space-1: 4px   /* Extra tight */
space-2: 8px   /* Tight */
space-3: 12px  /* Within component */
space-4: 16px  /* Standard */
space-5: 20px  /* Comfortable */
space-6: 24px  /* Between blocks */
space-8: 32px  /* Large blocks */
space-10: 40px /* Sections */
space-12: 48px /* Large spacing */
space-16: 64px /* Whitespace */
```

### Spacing Usage Decisions

| Scenario | Spacing | Principle |
|----------|---------|-----------|
| List items | 8-12px | Tight, related |
| Within card | 16px | Breathing room |
| Between blocks | 24-32px | Clear distinction |
| Between sections | 48px+ | Whitespace emphasis |

---

## Common Layout Patterns

### 1. Container + Content + Margin

```css
.container {
  max-width: 1200px;
  margin: 0 auto;
  padding: 0 16px;
}
```

### 2. Grid System

```css
.grid {
  display: grid;
  gap: 16px;
  grid-template-columns: repeat(4, 1fr);
}

@media (max-width: 768px) {
  .grid {
    grid-template-columns: repeat(2, 1fr);
  }
}

@media (max-width: 480px) {
  .grid {
    grid-template-columns: 1fr;
  }
}
```

### 3. Flex Layout

```css
.flex-center {
  display: flex;
  align-items: center;
  justify-content: center;
}

.flex-between {
  display: flex;
  align-items: center;
  justify-content: space-between;
}
```

---

## Alignment System

### Alignment is Order

| Alignment Type | Use Case | Examples |
|----------------|----------|----------|
| **Left** | Text content (default) | Body text, lists |
| **Right** | Numbers, actions | Prices, buttons |
| **Center** | Titles, cards | Hero, modals |
| **Justify** | Multi-line text (use sparingly) | Card body text |

**Apple Principle**: No more than 2 alignment types on the same page.

---

## Output Format

### CSS Variables

```css
:root {
  /* Spacing */
  --space-1: 4px;
  --space-2: 8px;
  --space-3: 12px;
  --space-4: 16px;
  --space-5: 20px;
  --space-6: 24px;
  --space-8: 32px;
  --space-10: 40px;
  --space-12: 48px;
  --space-16: 64px;

  /* Container */
  --container-sm: 640px;
  --container-md: 768px;
  --container-lg: 1024px;
  --container-xl: 1200px;

  /* Breakpoints */
  --breakpoint-sm: 640px;
  --breakpoint-md: 768px;
  --breakpoint-lg: 1024px;
  --breakpoint-xl: 1280px;
}
```

---

## Checklist (Designer Perspective)

- [ ] Does element distance express relationships?
- [ ] Is there visual flow guiding users?
- [ ] Is the grid unified (multiples of 8)?
- [ ] Is mobile "redesigned" rather than "compressed"?
- [ ] Is alignment consistent? (No more than 2 types)
- [ ] Do containers have boundary feel?

---

## Professional Terminology

| Term | Definition |
|------|------------|
| **Grid** | Grid system |
| **Gutter** | Grid spacing |
| **Margin** | Outer spacing |
| **Padding** | Inner spacing |
| **Container** | Layout container |
| **Breakpoint** | Responsive breakpoint |
| **Responsive** | Responsive design |
| **Adaptive** | Adaptive design |
| **Fluid** | Fluid layout |
| **Container Queries** | Container-based queries |
