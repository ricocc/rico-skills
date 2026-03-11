# Theme Generation Guide

Reference this prompt template for generating design system themes:

---

# Role: Professional Design System Reverse Engineer

**Task**: Perform **visual reverse engineering** on target web pages without accessing compiled code or crawling CSS. Output a complete, implementable design system document based purely on visual interface characteristics.

Target Page:
https://your-website.com

---

## Output Requirements

### Required Sections

1. **Design Philosophy**
   - Brand philosophy / Design philosophy
   - Why designed this way?
   - Core keywords (3-5)

2. **Color System + Usage Principles**
   - Brand, background, text, functional colors
   - When to use which color?
   - Usage principles (e.g., brand color not exceeding 10%)
   - Common mistakes to avoid

3. **Interaction Philosophy**
   - Motion principles (restrained, natural, meaningful)
   - Feedback mechanisms (instant, clear, gentle)
   - Specific motion parameters (duration, easing)

4. **Layout Principles**
   - Spacing strategy (grid system)
   - Whitespace principles (why so much whitespace?)
   - Content max width

5. **Component Specifications + Design Decisions**
   - Core components: buttons, cards, inputs, etc.
   - Why designed this way? (e.g., why 48px height?)
   - Thinking behind design decisions

6. **Application Scenarios**
   - Suitable project types
   - Application methods for different scenarios (at least 3)
   - Adjustments needed

7. **Common Mistakes to Avoid**
   - Common errors (at least 5)
   - Negative checklist (what not to do)

### Output Format

Save as `references/styles/[name].md`

Format reference: See `references/styles/airbnb.md`

---

## Output Structure Template

Follow this structure strictly. **All values must be precise and directly usable in frontend development**:

## I. Design Philosophy

### Brand Philosophy

- Brief description of brand core concept (1-2 sentences)
- Explain how design conveys brand values

### Design Philosophy

List 3-5 design philosophies, each including:
- Philosophy name (e.g., "Photo First")
- Specific explanation
- Why designed this way

### Core Keywords

List 3-5 keywords, e.g.: Warm, Human, etc.

### Overview

Brief description of this style's origin and suitable product types

## II. Color System

### Brand Color

- CSS variable definitions
- Usage guidelines (when to use, avoid, usage principle, why)

### Background, Text, Border, Accent, Functional Colors

- CSS variable definitions
- Special notes (e.g., why warm gray instead of cool gray)

## III. Interaction Philosophy

### Motion Principles

- Core concept (restrained, natural, meaningful)
- Entrance animations, hover feedback, state transitions
- Animations to avoid

### Feedback Mechanisms

- Button feedback, input feedback, loading states

## IV. Layout Principles

### Spacing Strategy

- Grid system (4px/8px)
- Common spacing
- Why?

### Whitespace Principles

- Horizontal whitespace, vertical whitespace
- Why so much whitespace?

### Content Max Width

## V. Component Design Decisions

### Buttons, Cards, Inputs, etc.

Each component includes:
- CSS code examples
- Design decision explanation (why designed this way?)

## VI. Typography Scale

## VII. Spacing System

## VIII. Border Radius System

## IX. Shadows

## X. Component Specifications (Detailed Code)

## XI. Animations (CSS Variables)

## XII. Application Scenarios

List at least 3 scenarios, each including:
- Core applications
- Adjustment recommendations

## XIII. Common Mistakes to Avoid

### Common Errors

List at least 5 common errors in format:
- Wrong approach
- Correct approach
- Reason

### Negative Checklist

What not to do (at least 5 items)

## XIV. Best For

List suitable product types

---

## Special Emphasis

1. **Output not just "what", but explain "why"**
   - Why this border radius size?
   - Why warm gray instead of cool gray?
   - Why so much whitespace?

2. **Include usage principles, not just variable definitions**
   - When to use brand color?
   - What's the usage principle?
   - What mistakes to avoid?

3. **Provide application guidance to help users apply to their projects**
   - Suitable project types
   - How to apply in different scenarios
   - What adjustments needed

4. **All values must be precise, directly usable in frontend development**
   - Don't say "medium border radius", say "8px border radius"
   - Don't say "soft shadow", say "0 2px 8px rgba(0, 0, 0, 0.12)"
