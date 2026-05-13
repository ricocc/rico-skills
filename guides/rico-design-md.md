# Rico Design MD - Design System Document Generator

Convert any website into a complete design system document, or convert between design token formats (DESIGN.md, tokens.json, variables.css, theme.css).

---

## What Can This Skill Do?

### Core Features

1. **Website to Design System** - Input any website URL, extract its design tokens, colors, typography, spacing, shadows, and component styles
2. **Multiple Output Formats** - Generate DESIGN.md, preview.html, tokens.json (DTCG), variables.css, and theme.css (Tailwind v4)
3. **Format Conversion** - Convert between any supported formats (e.g., DESIGN.md to tokens.json, variables.css to DESIGN.md)
4. **Visual Preview** - Generate a self-contained preview.html page that showcases the entire design system

### Use Cases

- Need a design system document for an existing website
- Want to extract design tokens for implementation
- Need to convert between design token formats
- Want a visual reference page for a brand's design system

---

## Trigger Methods

This skill supports two trigger modes:

**Mode 1: Explicit Command (rico prefix)**

| Command | Output |
|---------|--------|
| `rico DESIGN.md [url]` | DESIGN.md + preview.html (default) |
| `rico preview [url]` | preview.html only |
| `rico tokens [url]` | tokens.json only |
| `rico variables [url]` | variables.css only |
| `rico theme.css [url]` | theme.css only |
| `rico 全部输出 [brand]` | All 5 files |
| `rico 把 DESIGN.md 转为 tokens` | Format conversion |

**Mode 2: Natural Language**

```
Create a DESIGN.md for linear.app
Extract design tokens from stripe.com
Generate a preview for github.com
Analyze GitHub's design system
```

---

## Output Structure

All generated files are saved in the `themes/{brand-slug}/` directory:

```
themes/{brand-slug}/
├── DESIGN.md         # Full style reference (default output)
├── preview.html      # Visual design system preview (default output)
├── tokens.json       # DTCG format design tokens
├── variables.css     # CSS custom properties
└── theme.css         # Tailwind v4 @theme
```

---

## Workflow

### Workflow 1: Generate DESIGN.md + Preview (Default)

```
User: rico DESIGN.md https://linear.app
    ↓
Step 1: Gather visual data
  • Screenshot hero, nav, CTAs, cards, typography, footer
  • Inspect DevTools for CSS variables, @font-face, computed styles
    ↓
Step 2: Extract design tokens
  • Colors → semantic tokens (canvas, surface-1, ink, accent-blue, etc.)
  • Typography → font families, sizes, weights, line-height, letter-spacing
  • Spacing → base unit detection (4px or 5px grid)
  • Radius → xs to full scale
  • Shadows → full CSS syntax
    ↓
Step 3: Document components with all states
  • Navigation, Buttons, Inputs, Cards, Footer
  • Include hover, focus, active, selected states
    ↓
Step 4: Write brand voice (5-8 sentences as design critique)
    ↓
Step 5: Write Do's / Don'ts (7-8 each, referencing specific tokens)
    ↓
Step 6: Generate DESIGN.md + preview.html
```

### Workflow 2: Single Format Output

```
User: rico tokens https://stripe.com
    ↓
Generate tokens.json only (DTCG format)
```

### Workflow 3: Full Output (All 5 Files)

```
User: rico 全部输出 github
    ↓
Generate all 5 files:
  • DESIGN.md, preview.html, tokens.json, variables.css, theme.css
```

### Workflow 4: Format Conversion

```
User: rico 把 DESIGN.md 转为 tokens
    ↓
Parse existing DESIGN.md → generate tokens.json
```

---

## Output Format Details

### DESIGN.md

A comprehensive markdown document containing:

- Brand voice and design philosophy
- Color system with semantic token names
- Typography scale with font-feature-settings
- Spacing system
- Border radius scale
- Shadow specifications
- Component documentation (with all states)
- Do's and Don'ts (referencing specific tokens)

### preview.html

A self-contained, single-file visual design system reference page:

- Linear top-to-bottom layout (no bento grid)
- Sections: Hero → Colors → Gradients → Typography → Spacing & Shapes → Shadows → Depth & Surfaces → Components → Do's & Don'ts
- Download links for all spec files
- Sticky nav with section anchors
- Scroll-triggered entrance animations
- Responsive (mobile-first)
- Works with `file://` protocol (no external dependencies except Google Fonts)

### tokens.json

DTCG (Design Tokens Community Group) standard format:

- Each token includes `$description` explaining its intended use
- Grouped by category: colors, typography, spacing, radius, shadows
- Compatible with style dictionary and token transformers

### variables.css

CSS custom properties grouped by:

- Colors, Font Families, Type Scale, Weights
- Spacing, Layout, Border Radius, Shadows, Surfaces

### theme.css

Tailwind v4 `@theme` format for direct integration with Tailwind CSS v4.

---

## Usage Examples

### Example 1: Generate Design System from Website

```
User: rico DESIGN.md https://linear.app

AI: [Extracts design tokens from Linear's website]
    [Generates themes/linear/DESIGN.md + themes/linear/preview.html]

    Generated 2 files:
    • themes/linear/DESIGN.md - Full style reference
    • themes/linear/preview.html - Visual preview
```

### Example 2: Extract Tokens Only

```
User: rico tokens https://github.com

AI: [Extracts tokens from GitHub]
    [Generates themes/github/tokens.json]

    Generated DTCG tokens with 87 tokens across 6 categories.
```

### Example 3: Convert Between Formats

```
User: rico 把 DESIGN.md 转为 tokens

AI: [Parses existing DESIGN.md]
    [Converts markdown tables to DTCG format]

    Generated themes/github/tokens.json
```

### Example 4: Full Output

```
User: rico 全部输出 github

AI: [Generates all 5 files in themes/github/]
    • DESIGN.md
    • preview.html
    • tokens.json
    • variables.css
    • theme.css
```

---

## Edge Cases

| Scenario | Handling |
|----------|----------|
| SPA / client-rendered | Use view-source + network tab for CSS files |
| Compressed CSS | Use DevTools computed styles panel |
| Multi-theme (light/dark) | Ask user which theme to document; offer separate `dark/` subdirectory |
| Auth-gated pages | Focus on public marketing pages |
| Missing token categories | Skip sections and note the gap (never fabricate values) |

---

## File Structure

```
skills/
└── rico-design-md/
    ├── SKILL.md                          # Core skill definition
    └── references/
        ├── DESIGN-TEMPLATE.md            # Template for new DESIGN.md files
        └── themes-github/                # Reference example (GitHub)
            ├── DESIGN.md                 # Complete DESIGN.md example
            ├── github-preview.html       # Visual preview example
            ├── tokens.json               # DTCG format reference
            ├── variables.css             # CSS custom properties reference
            └── theme.css                 # Tailwind v4 @theme reference
```

---

## FAQ

### How is this different from rico-ui-ux-themes?

- **rico-ui-ux-themes**: Applies existing design themes to optimize your website's visual design
- **rico-design-md**: Extracts design systems FROM websites and generates documentation/tokens

### Can I use the generated tokens in my project?

Yes. All output formats are production-ready:
- `tokens.json` works with style dictionary and token transformers
- `variables.css` can be imported directly
- `theme.css` integrates with Tailwind v4

### What if the website has both light and dark modes?

The skill will ask which mode to document. If the dark mode is visually distinct (e.g., Linear, Supabase), it offers to generate a separate `themes/{brand}-dark/` subdirectory.

---

**Last Updated**: 2026-05-13

**Maintainer**: [@ricouii](https://x.com/ricouii)

**Blog**: [rico'blog](https://ricoui.com)

**Status**: Active Development
