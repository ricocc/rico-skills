---
name: rico-design-md
description: >
  Create design system documents from any website URL.
  Use this skill for: DESIGN.md, preview.html, design tokens, CSS variables, style references,
  brand analysis, or format conversion between DESIGN.md/tokens.json/variables.css/theme.css.
  Trigger on: "create a DESIGN.md", "extract design tokens", "analyze [brand]'s design system",
  "reverse-engineer [url]'s visual style", "rico DESIGN.md", "rico tokens", "rico 全部输出".
  Covers: DESIGN.md, preview.html, tokens.json (DTCG), variables.css, theme.css (Tailwind v4).
---

# Get Design MD

Convert any website into design system documents, or convert between formats.

## Do's

- **Read the reference example first.** Before generating any format, read the matching file
  in `references/themes-github/` to match structure exactly. This prevents format drift.
- **Use semantic token names.** Name tokens by role (ink, surface-1, accent-blue) not by
  appearance (vapor-white, charcoal-canvas) — unless the descriptive name is the brand's own.
- **Capture full CSS syntax for shadows.** Write `rgba(255,255,255,0.1) 0 0.5px 0 0.5px`,
  not "subtle shadow". Downstream consumers need parseable values.
- **Document every observed component state.** Hover, focus, active, selected — each state
  changes CSS properties. Missing states mean incomplete implementation.
- **Verify color values against screenshots.** CSS inspection can miss overlay effects,
  gradient blends, and browser-specific rendering. Cross-check with visual evidence.
- **Provide open-source font substitutes.** Proprietary fonts (GT Walsheim, Söhne) need
  alternatives (Mona Sans, Inter, DM Sans) for anyone implementing the design.
- **Include `$description` in tokens.json.** Each token needs a human-readable description
  explaining its intended use — this is the DTCG standard and prevents misuse.
- **Write brand voice as design critique.** The overview paragraph should read like a designer
  describing the brand's visual personality, not a feature list.

## Don'ts

- **Don't invent placeholder values.** If a token category is missing from the source
  (e.g., no shadows observed), skip it and note the gap. Fabricated values break trust.
- **Don't mix tokens from multiple themes.** If a site has light and dark modes, ask the
  user which to document. If the dark mode is visually distinct (e.g., Linear, Supabase),
  offer to generate a separate `dark/` subdirectory with its own 4 files. Never blend
  tokens from both themes into one document.
- **Don't use generic Do's/Don'ts in DESIGN.md.** Every rule must reference a specific
  token or property. "Use good contrast" is useless; "Reserve accent-blue for hyperlinks
  and focus rings only" is actionable.
- **Don't omit letter-spacing and line-height.** Typography tokens without these are
  incomplete — tracking and leading define the brand voice as much as font-size.
- **Don't flatten complex shadows into single values.** Layered shadows (light-edge + drop)
  must be preserved as-is, not simplified to a single `box-shadow`.
- **Don't skip the brand voice paragraph.** It's the design rationale that guides future
  decisions. Without it, the document is just a token dump.

## Trigger Behavior

| Command | Output |
|---------|--------|
| `rico DESIGN.md [url]` | DESIGN.md + preview.html (default) |
| `rico preview [url]` | preview.html only |
| `rico tokens [url]` | tokens.json only |
| `rico variables [url]` | variables.css only |
| `rico theme.css [url]` | theme.css only |
| `rico 全部输出 [brand]` | All 5 files (DESIGN.md + preview.html + tokens + variables + theme) |
| `rico 把 DESIGN.md 转为 tokens` | Format conversion |

Natural language also triggers: "create a DESIGN.md for linear.app",
"extract design tokens from stripe.com", "generate preview for [url]".

## Output Structure

```
themes/{brand-slug}/
├── DESIGN.md         # Full style reference (default)
├── preview.html      # Visual design system preview (default)
├── tokens.json       # DTCG format tokens
├── variables.css     # CSS custom properties
└── theme.css         # Tailwind v4 @theme
```

**Default output:** `rico DESIGN.md [url]` generates both `DESIGN.md` and `preview.html`.

The `preview.html` is a self-contained, single-file design system reference page:
- Linear top-to-bottom layout (no bento grid) — content-adaptive, works with any brand
- Sections: Hero → Colors (with swatches) → Gradients → Typography (type scale + fonts) → Spacing & Shapes → Shadows → Depth & Surfaces → Components (with live previews) → Do's & Don'ts
- Download links for all spec files (DESIGN.md, tokens.json, variables.css, theme.css)
- Sticky nav with section anchors
- Scroll-triggered entrance animations
- Responsive (mobile-first)
- Based on the GitHub preview template at `references/themes-github/github-preview.html`


## Reference Examples

The `references/` directory contains template and example files.
Read the matching file before generating — structure must be consistent:

- **DESIGN.md template** → `references/DESIGN-TEMPLATE.md` — fill this template for new sites
- **DESIGN.md example** → `references/themes-github/DESIGN.md` — GitHub's complete output
- **preview.html example** → `references/themes-github/github-preview.html` — GitHub's visual preview
- **tokens.json** → `references/themes-github/tokens.json` — DTCG format reference
- **variables.css** → `references/themes-github/variables.css` — CSS custom properties reference
- **theme.css** → `references/themes-github/theme.css` — Tailwind v4 @theme reference


## Workflow

### Step 1 — Gather Visual Data

Screenshot hero, nav, CTAs, cards, typography sections, footer. Inspect DevTools for
CSS variables, `@font-face`, computed styles, box-shadow, border-radius, spacing.

**Why:** Screenshots capture decorative elements (gradients, glows, illustrations) that
CSS inspection alone misses.

### Step 2 — Extract Tokens

**Colors** — Map observed values to semantic tokens:

| Observed | Token | Type |
|----------|-------|------|
| Page bg | `canvas` | color |
| Card bg | `surface-1` | color |
| Elevated bg | `surface-2` | color |
| Primary text | `ink` | color |
| Secondary text | `ink-muted` | color |
| Link/accent | `accent-blue` | color |
| Success | `semantic-success` | color |
| Error | `semantic-error` | color |
| Border | `hairline` | color |
| Gradient | `gradient-{name}` | gradient |

**Typography** — Record fontFamily, fontSize, fontWeight, lineHeight, letterSpacing for each
font. Map sizes to tokens: 110px→display-xxl, 85px→display-xl, 62px→display-lg,
32px→display-md, 22px→headline, 15px→body, 14px→body-sm, 13px→caption, 12px→micro.

Check `font-feature-settings` for OpenType: cv01-99 (character variants), ss01-20
(stylistic sets), tnum (tabular), dlig (discretionary ligatures).

Font substitutes: GT Walsheim → Mona Sans/Geist/Inter 600-700. Söhne → Inter/DM Sans.

**Spacing** — Base unit detection: multiples of 4 → base=4px. Multiples of 5/10/15/20 → base=5px.

**Radius** — xs(4px)·sm(6px)·md(10px)·lg(15px)·xl(20px)·xxl(30px)·pill(100px)·full(9999px)

**Shadows** — Full CSS syntax only.

### Step 3 — Document Components

For each component, document all CSS properties including states:

```markdown
### Primary Button
**Role:** Main CTA
- background: `{colors.ink}` (#ffffff)
- color: `{colors.canvas}` (#0a0a0a)
- border-radius: `{rounded.pill}` (100px)
- padding: 10px 15px
- font: 14px/500/1.0/-0.14px
- hover: opacity 0.85
- active: transform scale(0.97)
```

Components: Navigation, Buttons (primary/secondary/translucent/icon), Pricing tabs,
Inputs (default/focused), Cards (standard/featured/spotlight), Comparison rows, Footer.

### Step 4 — Write Brand Voice

5-8 sentences as design critique: dominant surface → typeface personality → accent color
behavior → depth approach → signature rhythm break → component language.

### Step 5 — Write Do's / Don'ts

7-8 each. Every rule references a specific token with reasoning.

### Step 6 — Generate Outputs

Read the reference example, then generate requested file(s).

**Default:** Generate `DESIGN.md` + `preview.html`.

**preview.html generation:**
1. Read the template at `references/themes-github/github-preview.html`
2. Replace all CSS custom properties (`:root` variables) with the brand's tokens
3. Replace color swatches, type scale samples, spacing bars, radius boxes, shadow demos, depth levels, surface cards, and component previews with the brand's actual values
4. Replace the hero text, tags, and download links with brand-specific content
5. Replace the nav GitHub icon link with the brand's repository URL (if applicable)
6. Keep the overall structure and section order — only the content/tokens change
7. Use the brand's actual font family in type samples (with Inter as fallback)
8. Adjust component cards to match the brand's actual components (buttons, inputs, cards, navigation)

**Single-file principle:** preview.html must be fully self-contained (inline CSS, no external dependencies except Google Fonts). Must work when opened directly via `file://` protocol.

## Format Conversion

### DESIGN.md → tokens.json / variables.css / theme.css

Parse markdown tables → map to target format. Include `$description` from Role column.
Group variables.css by: Colors, Font Families, Type Scale, Weights, Spacing, Layout,
Border Radius, Shadows, Surfaces.

### tokens.json → DESIGN.md

Parse DTCG groups → generate markdown tables → infer components from token relationships.

### variables.css → DESIGN.md

Parse `:root {}` → group by prefix (--color-, --font-, --text-, --spacing-, --radius-)
→ generate tables.

### tokens.json ↔ variables.css ↔ theme.css

Direct mapping: `$value` → `--{name}: {value}` → `@theme { --{name}: {value} }`

## Edge Cases

- **SPA / client-rendered:** Use view-source + network tab for CSS files
- **Compressed CSS:** Use DevTools computed styles panel
- **Multi-theme:** Ask user which theme to document. If dark mode is visually distinct,
  offer a separate `themes/{brand}-dark/` subdirectory. Never mix tokens from both themes
- **Auth-gated:** Focus on public marketing pages
- **Missing tokens:** Skip sections rather than invent values