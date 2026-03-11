# Rico UI/UX Themes - Website Design Optimization Skill

One-click visual and interaction design optimization for websites. Supports 20 built-in themes, custom theme generation, and design reverse engineering from any website.

---

## What Can This Skill Do?

### Core Features

1. **Smart Design Optimization** - Analyze existing code, automatically optimize color, typography, spacing, border-radius, shadows, and interactions
2. **Apply Design Systems** - Apply mature design systems to your projects for visual consistency
3. **Generate Themes from Websites** - Input any website URL to extract design patterns and create reusable theme documents
4. **Natural Language Adjustments** - Describe changes in plain language: "make colors lighter", "increase border-radius"

### Use Cases

- Website visual design needs professional polish
- Want to reference design styles from established products
- Need consistent design systems across different projects
- Starting from scratch and need design guidance

---

## Installation

### Quick Install (Recommended)

```bash
npx @ricocc/rico-ui-ux-themes
```

That's it! Restart Claude Desktop, then use `rico optimize design` or natural language commands.

### Manual Download

1. Download [ZIP](https://github.com/ricocc/rico-ui-ux-themes/archive/refs/heads/main.zip)
2. Extract and place the `rico-ui-ux-themes` folder to your Claude skills directory:
   - macOS/Linux: `~/.claude/skills/`
   - Windows: `%USERPROFILE%\.claude\skills\`
3. Restart Claude Desktop

### Clone via Git

```bash
git clone https://github.com/ricocc/rico-ui-ux-themes.git ~/.claude/skills/
```

Restart Claude Desktop after cloning.

### Verify Installation

```
rico list themes
```

If you see a list of 20 themes, installation is successful.

---

## Trigger Methods

This skill supports two trigger modes:

**Mode 1: Explicit Command (rico prefix)**
```
rico optimize design
rico use Claude style
rico create theme: stripe.com
rico list themes
```

**Mode 2: Natural Language**
```
Optimize this website's visual design
Apply Airbnb style to this page
Generate a theme from apple.com
```

---

## Optimization Workflows

### Workflow 1: One-Click Optimization

```
User: rico optimize this website
    ↓
AI reads code
    ↓
6-Dimension Analysis:
  • Color (contrast, saturation, brand usage)
  • Typography (font size, line-height, weight, family)
  • Spacing (grid system, whitespace, compactness)
  • Border Radius (consistency, style unity)
  • Shadow (weight, consistency, meaning)
  • Interaction (button/link states, animations, feedback)
    ↓
Output optimized code + design decisions explained
```

### Workflow 2: Apply Specific Style

```
User: rico use Claude style for this page
    ↓
Load theme file (claude.md)
    ↓
Analyze differences between current code and theme
    ↓
Output optimized code matching the theme
```

### Workflow 3: Generate Theme from Website

```
User: rico create theme: duolingo.com
    ↓
Fetch target page content
    ↓
Visual Reverse Engineering:
  • Extract color system
  • Analyze typography standards
  • Identify spacing patterns
  • Parse component design
    ↓
Generate 14-chapter theme document
    ↓
Save to references/styles/duolingo.md
    ↓
Show preview, await confirmation
    ↓
Ask if user wants to apply to project
```

---

## Supported Tech Stacks

Auto-detects and adapts to:

| Tech Stack | Support | Special Handling |
|------------|---------|------------------|
| React | ✅ Full | JSX, styled-components, CSS Modules |
| Vue | ✅ Full | Vue SFC, scoped styles |
| Angular | ✅ Full | Component styles, global styles |
| Mini Programs | ✅ Full | rpx, custom components |
| HTML/CSS | ✅ Full | Native CSS, CSS variables |
| Sass/SCSS | ✅ Full | Variables, mixins, nesting |
| Tailwind | ✅ Full | Theme config, custom classes |
| Next.js | ✅ Full | CSS Modules, Tailwind |

---

## Built-in Themes (20 Themes)

### By Use Case

**Developer Tools** - Claude, Minimal Blue, Marketplace Dark, SaaS Dark, Agent Dark

**Business & Enterprise** - Professional Blue, Trust Finance, Dashboard Clean

**Creative Design** - Retro Vibrant, Creative Gallery, Neo-Brutalist, Creative Vitality

**Audio & Music** - Radio Static, Record Club, Spotify

**E-commerce** - Vibrant Commerce

**Brand Styles** - Airbnb, Linear, Notion, Duolingo

### View Theme Details

```
rico list themes              # List all themes
rico show Claude theme        # View detailed info about a theme
```

---

## Usage Examples

### Example 1: Quick Optimization

```
User: rico optimize this login page

AI: I analyzed your code and found these issues:
    1. Primary button contrast ratio insufficient (2.1:1, recommended 4.5:1)
    2. Input border-radius inconsistent (4px vs 8px)
    3. Form spacing too tight, looks crowded
    4. Missing hover/focus state feedback

    Optimization plan:
    [Output optimized code]
```

### Example 2: Apply Style

```
User: rico use Linear style for this dashboard

AI: Linear style characteristics:
    • Dark background + subtle gradients
    • Small border-radius (4-6px) for professional feel
    • Compact layout, high information density
    • Fast animations (100-150ms)

    Applying these features to your dashboard:
    [Output optimized code]
```

### Example 3: Generate Theme

```
User: rico create theme: stripe.com

AI: Analyzing Stripe's design patterns...

    Extracted design system:
    • Primary: #0052CC (trust blue)
    • Border-radius: 8px (professional yet friendly)
    • Spacing: 8px grid system
    • Animations: 150-200ms ease-out

    Generated theme file: references/styles/trust-finance.md

    Confirm this theme? Can apply to your project after confirmation.
```

### Example 4: Natural Language Adjustments

```
User: rico optimize this page
AI: [Output optimized code]

User: Colors too dark
AI: Adjusting background from #0D1117 to #161B22 for better readability
    [Output adjusted code]

User: Make border-radius larger
AI: Increasing button radius from 6px to 10px, card radius from 8px to 12px
    [Output adjusted code]
```

---

## Theme File Structure

Each theme document contains 14 chapters:

1. **Design Philosophy** - Brand philosophy, core keywords
2. **Color System** - Primary, background, text, accent colors with usage guidelines
3. **Interaction Philosophy** - Animation principles, feedback mechanisms
4. **Layout Principles** - Spacing strategy, grid system
5. **Component Decisions** - Why buttons/inputs/cards are designed this way
6. **Application Scenarios** - Suitable projects, how to adapt
7. **Common Mistakes** - What to avoid when using this theme
8. **Typography Scale** - Precise font size specifications
9. **Spacing System** - Precise spacing specifications
10. **Border Radius System** - Precise radius specifications
11. **Shadow Specifications** - Shadow weights and use cases
12. **Component Specifications** - Exact styles for buttons, inputs, cards
13. **Animation Specifications** - Duration, easing functions
14. **Suitable Scenarios** - Industry, product types

---

## File Structure

```
rico-ui-ux-themes/
├── SKILL.md              # Core skill definition
├── README.md             # This document
├── README-zh.md          # Chinese documentation
└── references/
    ├── docs/             # Design reference docs
    │   ├── color.md      # Color design guide
    │   ├── typography.md # Typography design guide
    │   └── ...
    └── styles/           # Theme files (20 built-in + user-generated)
        ├── claude.md
        ├── minimal-blue.md
        └── ...
```

---

## FAQ

### Can I use the optimized code directly?

Yes, the output includes complete CSS variables, component styles, responsive design, and accessibility support (WCAG 2.1 AA). Ready to use in your project.

### Can generated themes be shared?

Yes, themes are saved as standard Markdown files in `references/styles/`. Share with team members or reuse across projects.

### Can I modify existing themes?

Yes, after generating a theme, use natural language to adjust: "make colors lighter", "change border-radius to 12px".

### How to choose the right theme?

Based on your product type:
- Developer Tools → Claude, Minimal Blue, Marketplace Dark
- Enterprise SaaS → Professional Blue, Trust Finance
- Creative Brands → Retro Vibrant, Neo-Brutalist
- Audio Products → Radio Static, Spotify

---

## Version History

- **v1.0** - Initial release

---

**Last Updated**: 2026-03-11

**Maintainer**:  [@ricouii](https://x.com/ricouii)

**Blog**: [rico'blog](https://ricoui.com)

**Status**: ✅ Active Development 

