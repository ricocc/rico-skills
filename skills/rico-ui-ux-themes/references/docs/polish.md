# Design Audit Guide

> For general optimization workflow, see SKILL.md. This guide focuses on professional methodology for design reviews.

---

## First Principles of Auditing

**Auditing is not finding faults, it's building design confidence.**

Good audits help teams:
- **Know what works** — Reinforce successful decisions
- **Know what to improve** — Prioritize issues
- **Know why** — Build design consensus

> "Critique is not about finding problems. It's about strengthening solutions."
> — From Airbnb Design Critique Method

---

## Professional Audit Framework

### 1. Three-Layer Review

| Layer | Question | Method |
|-------|----------|--------|
| **Strategic** | "Is this the right design?" | User goal alignment |
| **Execution** | "Is the design implemented well?" | Consistency check |
| **Edge** | "Are edge cases handled?" | Extreme testing |

### 2. Apple Design Review

**Apple Internal Review Questions**:

1. "If users could only remember one thing, what should it be?"
2. "Will this design be outdated in 10 years?"
3. "If we remove this element, can the function still work?"
4. "Will users feel 'designed at' or 'natural'?"

### 3. Airbnb Design Critique

**Questions for Every Review**:

```
1. What works well?
2. What could be improved?
3. What's missing?
4. What's confusing?
```

---

## Audit Dimensions

### 1. Accessibility (A11y)

| Check | Apple Standard | WCAG |
|-------|----------------|------|
| Contrast | 4.5:1 | AA |
| Focus visible | 2pt ring | Required |
| Touch target | 44x44pt | 44x44px |
| Animation | Reduced motion | Supported |

### 2. Consistency

| Dimension | Check |
|-----------|-------|
| Visual | Same elements look the same |
| Interaction | Same actions produce same results |
| Terminology | Same concepts use same words |

### 3. Performance

| Metric | Target |
|--------|--------|
| First Contentful Paint | <1.5s |
| Time to Interactive | <3s |
| Animation frame rate | 60fps |
| Layout shift | <0.1 |

---

## Review Report Structure

### Professional Report Template

```markdown
# Design Audit Report

## Executive Summary
- Overall health: X/10
- Key issues: X
- Immediate action needed: X
- Can optimize later: X

## Dimension Scores

### Usability
- [ ] Core flow clear
- [ ] States complete
- [ ] Feedback instant

### Consistency
- [ ] Components unified
- [ ] Interactions unified
- [ ] Language unified

### Elegance
- [ ] Has breathing room
- [ ] Has rhythm
- [ ] Has brand feel

## Issue List

### 🔴 P0 - Must Fix

**[Issue Name]**
- Location: xxx
- Impact: xxx
- Recommendation: xxx

### 🟡 P1 - Should Optimize

**[Issue Name]**
- Location: xxx
- Impact: xxx
- Recommendation: xxx

### 🟢 Positive Findings

**[What Works Well]**
- Analysis
- Recommendation to maintain

## Next Steps

1. Immediate: P0 issue fixes
2. This week: P1 optimizations
3. Planned: Architectural improvements
```

---

## Design Anti-Patterns Summary (Based on Impeccable)

### Visual Anti-Patterns

| Anti-pattern | Description | Solution |
|--------------|-------------|----------|
| **Christmas tree** | Too many colors | Simplify palette, follow 60-30-10 rule |
| **Prison bars** | Too many lines | Increase spacing, use whitespace |
| **Font explosion** | Too many font sizes | Reduce hierarchy, use modular scale |
| **Component orphans** | Components without containers | Unify layout |
| **Cards everywhere** | Wrapping everything in cards | Use spacing and alignment for grouping |
| **Nested cards** | Cards inside cards | Flatten hierarchy |

### The AI Slop Test

**Critical quality check**: If you showed this interface to someone and said "AI made this," would they believe you immediately? If yes, that's the problem.

A distinctive interface should make someone ask "how was this made?" not "which AI made this?"

Common AI-generated fingerprints:
- Inter font
- Purple gradients
- Cards on cards
- Generic icon + heading + text card patterns
- Gray text on colored backgrounds
- Rounded rectangles with generic shadows

---

## Checklist (Designer Perspective)

### Strategic Layer
- [ ] User goals clear
- [ ] Core flow smooth
- [ ] Value proposition clear

### Execution Layer
- [ ] Visual hierarchy correct
- [ ] Interactions consistent
- [ ] Motion natural
- [ ] Responsive adaptation

### Edge Layer
- [ ] Empty state designed
- [ ] Loading state has feedback
- [ ] Error state has explanation
- [ ] Offline state handled

### Accessibility
- [ ] Keyboard operable
- [ ] Screen reader readable
- [ ] Contrast meets AA
- [ ] Reduced motion supported

---

## Professional Terminology

| Term | Definition |
|------|------------|
| **Critique** | Design review |
| **Heuristic** | Heuristic evaluation |
| **A11y** | Accessibility |
| **Edge Case** | Edge situation |
| **Systemic Issue** | System-level problem |
| **Pattern** | Design pattern |
| **Anti-pattern** | Anti-pattern |
| **Debt** | Technical/design debt |
| **Health Check** | Health assessment |
| **Gap Analysis** | Gap analysis |
