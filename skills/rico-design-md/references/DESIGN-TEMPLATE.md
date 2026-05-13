# {Brand Name} — Style Reference
> {One-line evocative tagline capturing the brand's visual personality}

**Theme:** {dark | light}

{One paragraph (5-8 sentences) describing the overall visual impression. Start with the dominant sensory quality (e.g., "a near-pure black artboard", "a soft warm background"). Describe the primary typeface personality, the accent color behavior, the surface/depth approach, and the component language. End with what makes this brand distinctive — the "rhythm break" or signature element. This paragraph should read like a design critique, not a spec sheet.}

## Tokens — Colors

| Name | Value | Token | Role |
|------|-------|-------|------|
| {Semantic Name} | `{hex}` | `--color-{token}` | {Primary page background / surface / text / accent / etc.} |
| ... | ... | ... | ... |

{If gradient or decorative accents exist, add a separate subsection:}

### Decorative / Gradient

| Name | Value | Token | Role |
|------|-------|-------|------|
| {Gradient Name} | `{hex}` | `--gradient-{token}` | {Decorative card / atmospheric / illustration} |

## Tokens — Typography

### {Font Family Name} — {Brief description of personality} · `--font-{token}`
- **Substitute:** {Open-source fallback}
- **Weights:** {400, 500, 600, ...}
- **Sizes:** {list all observed sizes}
- **Line height:** {values}
- **Letter spacing:** {values — negative for display, near-zero for body}
- **OpenType features:** {if any, e.g., "cv01", "cv05", "tnum"}
- **Role:** {Where this font appears in the brand}

{Repeat for each font family used. Usually 2-4 families: display, body, mono, optional specialty.}

### Type Scale

| Role | Size | Line Height | Letter Spacing | Token |
|------|------|-------------|----------------|-------|
| display | {xxl}px | {lh} | {ls}px | `--text-display` |
| ... | ... | ... | ... | ... |
| caption | {sm}px | {lh} | — | `--text-caption` |

{Include all distinct type roles observed. Typically 6-12 rows.}

## Tokens — Spacing & Shapes

**Density:** {compact | comfortable | generous}

### Spacing Scale

| Name | Value | Token |
|------|-------|-------|
| {xs/4/8/...} | {n}px | `--spacing-{name}` |

{List all observed spacing values, from smallest (4px) to largest section gap (96-160px).}

### Border Radius

| Name | Value | Token |
|------|-------|-------|
| {sm/8px/...} | {n}px | `--radius-{name}` |

{List all observed radius values. Include named radii for specific element types if distinct:}

| Element | Value |
|---------|-------|
| cards | {n}px |
| buttons | {n}px |
| inputs | {n}px |

### Shadows

| Name | Value | Token |
|------|-------|-------|
| {shadow-sm} | `{CSS shadow value}` | `--shadow-{name}` |

{List all observed shadow values. Include glow effects if brand uses them.}

### Layout

- **Section gap:** {n}px
- **Card padding:** {n}px
- **Element gap:** {n}px
- **Max content width:** {n}px (if constrained)

## Components

### {Component Name}
**Role:** {Primary action / Secondary action / Navigation / etc.}

{Describe CSS properties: backgroundColor, color, borderRadius, padding, fontSize, fontWeight, boxShadow, border, etc. Use inline property=value format. Include a 1-sentence usage note.}

{Repeat for each distinct component. Common components:}
- Primary Button
- Secondary Button / Ghost Button
- Link / Text Button
- Icon Button
- Card (standard / featured / etc.)
- Input Field
- Navigation
- Code Block
- Footer

## Surfaces

{If the brand uses a surface depth system, document it:}

| Level | Name | Value | Purpose |
|-------|------|-------|---------|
| 0 | {base} | `{hex}` | Base page background |
| 1 | {elevated} | `{hex}` | Secondary sections, cards |
| 2 | {floating} | `{hex}` | Elevated panels, modals |

## Do's and Don'ts

### Do
- {Actionable design rule with specific token/color reference}
- {7-8 rules covering: primary colors, typography, spacing, components, imagery}

### Don't
- {Anti-pattern to avoid with specific reasoning}
- {7-8 rules covering: color misuse, typography mistakes, spacing, component anti-patterns}

## Imagery

{One paragraph describing the visual language for imagery: product screenshots, illustrations, photography, icons. Describe density, framing, color treatment, and how imagery relates to the overall brand tone.}

## Layout

{One paragraph describing page structure: grid system, column arrangement, hero treatment, section rhythm, navigation pattern. Include max-width, responsive behavior, and spacing philosophy.}

## Agent Prompt Guide

{2-3 example prompts for AI agents to create specific sections/components using this design system. Include exact color values, font sizes, and spacing.}

## Similar Brands

- **{Brand}** — {One-line description of why it's similar}
- {4-6 brands with brief similarity notes}

## Quick Start

### CSS Custom Properties

```css
:root {
  /* Colors */
  --color-{token}: {hex};
  /* ... all color tokens ... */

  /* Typography — Font Families */
  --font-{token}: '{Font Name}', {fallbacks};

  /* Typography — Scale */
  --text-{role}: {size}px;
  --leading-{role}: {lh};
  --tracking-{role}: {ls}px;

  /* Spacing */
  --spacing-{name}: {value}px;

  /* Border Radius */
  --radius-{name}: {value}px;

  /* Shadows */
  --shadow-{name}: {CSS value};
}
```

### Tailwind v4

```css
@theme {
  /* Colors */
  --color-{token}: {hex};
  /* ... */
}