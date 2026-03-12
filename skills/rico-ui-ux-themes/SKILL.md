---
name: rico-ui-ux-themes
description: |
  UI/UX design optimization toolkit with 20 built-in themes and custom theme generation.
  Applies design systems with color, typography, spacing optimization for any tech stack.
  Use when user says "rico optimize", "rico 优化设计", "rico use style", "rico 用风格", "rico theme","rico 应用主题", "rico 生成主题", "rico design".
license: MIT
metadata:
  author: RicoUI (@ricouii)
  version: 1.0.0
  user-invocable: true
---

# rico-ui-ux-themes

UI/UX design optimization toolkit with 20 built-in themes and custom theme generation.

## Workflow

```
[User Input] → [Read Current Project Code] → [Analyze 6 Issues] → [Select Mode] → [Confirm] → [Output]
```

**CRITICAL EXECUTION RULES:**
1. **NEVER** show welcome message or greeting
2. **ALWAYS** show selection menu A/B/C/D before execution
3. **ALWAYS** wait for user input after showing menu
4. **ALWAYS** confirm before making any changes
5. **NEVER** skip steps or auto-execute without user confirmation

**Key Notes:**
- Automatically read code from current working directory when triggered (e.g., "optimize this project/page/design"). No need to ask "which project".
- Language Rule: Detect from initial trigger (e.g., "rico 优化" = Chinese, "rico optimize" = English), then maintain consistent language throughout.
- Project mode detection: Only generate missing light/dark mode if explicitly requested; never force switch.
- Integration: Uses webReader (fetch URLs), Read/Write tools (code operations). All require confirmation.

### 4 Interaction Patterns

| Pattern | Trigger Examples |
|---------|-----------------|
| **Full Flow** | rico optimize, rico 优化网站设计 |
| **Direct Apply** | rico use Claude style, rico 用 Claude 风格 |
| **Generate Theme** | rico create theme: stripe.com |
| **Natural Language** | rico make it more vibrant |

## Triggers and Interaction Patterns

All commands use `rico` prefix. Supports 4 patterns:

| Pattern | Trigger Examples | Brief Flow |
|---------|------------------|------------|
| **Full Flow** | rico optimize, rico 优化, rico 优化网站设计, rico improve this page design, rico 让页面更好看 | [Read Code] → [Analyze] → [Menu A/B/C/D] → [Select] → [Confirm] → [Output] |
| **Direct Apply** | rico use [theme-name] style, rico 用 [主题名] 风格, rico 用 Claude 风格优化, rico use Minimal Blue colors + Neo-Brutalist borders | [Load Theme] → [Preview] → [Confirm] → [Apply] |
| **Generate Theme** | rico create theme: [URL], rico 制作主题：[URL], rico 参考 [URL] 做主题 | [Fetch URL] → [Extract] → [Generate Doc] → [Save] → [Confirm Apply?] |
| **Theme Management** | rico list themes, rico 有哪些主题, rico show [theme-name], rico 看看 [主题名] | [List/Show] → No further steps unless apply |

**Natural Language Support:** e.g., "rico make it more vibrant" → Map to Full Flow or Direct Apply based on intent.



## Selection Menu (Full Flow)

When user triggers "rico optimize", the workflow is:

```
[Read Current Project] → [Analyze 6 Dimensions] → [Show Menu A/B/C/D] → [User Selects] → [Confirm] → [Output]
```

**IMPORTANT:** Show the menu immediately after reading code. Do NOT ask "what do you want to do" or show welcome message.

### Show Selection Menu

- **A.** Optimize by design principles (no specific style)
- **B.** Select from built-in themes (20 themes)
- **C.** Generate theme from industry reference
- **D.** Custom theme (URL or from project)

Enter option (A/B/C/D):

---

### Option A: Design Principles

User inputs: A

```
📋 6-Dimension Analysis Results

1. [⚠️] Color    - Contrast 3.2:1, below WCAG AA
2. [⚠️] Typography - Inter font, unclear hierarchy
3. [⚠️] Spacing  - Inconsistent, no grid system
4. [✓]  Border-radius - Unified style
5. [⚠️] Shadow   - Too heavy
6. [⚠️] Interaction - Missing hover/focus states

Select optimization mode:
- a: All (recommended)
- b: Issues only (1,2,3,5,6)
- Or directly input numbers: 1,3 (custom), 3 (single)

Enter (a/b or numbers):
```


**Confirmation Dialog:**

```
📋 Ready to Optimize: Spacing

Actions:
• Establish unified 4pt grid
• Adjust gaps and margins
• Optimize whitespace rhythm

Confirm? (y/n)
```


---

### Option B: Built-in Themes

User inputs: B


```
📊 Project Analysis
Detected: SaaS / Enterprise App
Style: Professional, clean, data-driven

🎯 Recommended Themes:
   • 6. Professional Blue ⭐
         → Style: Stable blue + clear hierarchy
         → Match: 95%

   • 1. Claude
         → Style: Warm white + ocher orange
         → Match: 88%

   • 8. Dashboard Clean
         → Style: Clean admin, data-focused
         → Match: 85%

   • 7. Trust Finance
         → Style: Deep blue + gold
         → Match: 82%

   • 2. Minimal Blue
         → Style: Dark BG + blue accent
         → Match: 78%

• Enter number to select
• Enter L to view all themes (built-in + user-created)

Enter:

```

**After theme selection:**

```
Selected: 5. Agent Dark (Dark theme)

📋 Style Features:
   • Deep black background + vibrant purple accent
   • Modern & creative
   • Best for: AI agents, creative tools
   • Mode: Dark (single mode)

🔧 Actions:
   • Apply dark background (#0A0A0B)
   • Add purple accent (#A855F7)
   • Optimize border-radius to 8px

Confirm? (y/n)
```

### Option C: Industry Reference

User inputs: C


```
📊 Project Type Detection

Detected: SaaS / Enterprise
(If incorrect, enter correct type)

🌐 Industry Reference Websites:
   1. stripe.com
      → Style: Deep blue + gold accents, professional
      → Features: Minimal, whitespace, clear hierarchy

   2. linear.app
      → Style: Dark BG + purple gradient, modern tech
      → Features: Refined interaction, subtle animation

   3. notion.so
      → Style: White BG + minimal, content-first
      → Features: Clean, efficient, distraction-free

   4. figma.com
      → Style: Colorful gradient + vibrant purple
      → Features: Creative, professional, collaborative

   5. vercel.com
      → Style: B&W minimal + neon gradient
      → Features: Cool, modern, developer-friendly

   • Enter number to select
   • Enter URL to use custom website
   • Enter n to skip

Enter:
```

User inputs: 1


   📋 Actions:
   • Fetch stripe.com design features
   • Analyze color, typography, spacing system
   • Generate theme file
   • Apply to current project

   Confirm? (y/n)

---

### Option D: Custom Theme

User inputs: D

```
🎨 Custom Theme

1. Input URL
   → Example: apple.com

2. Generate from current project
   → Extract existing design

Enter option (1/2) or URL:
```

**If option 2 (generate from project):**


AI response:

```
📋 Actions:
• Analyze current project design features
• Extract color, typography, spacing system
• Generate theme file

Enter theme name: [my-brand]

Save location:
   1. Current project
      → references/styles/my-brand.md
      → Project-only access

   2. User global directory
      → ~/.rico/themes/my-brand.md
      → Available for all projects

Enter (1/2):
```


User inputs: 1

AI response:
Analyzing project design features...
Generating theme file...

✅ Theme saved to: references/styles/my-brand.md

Apply to optimization? (y/n)
```

**Option D Notes:**
- Supports URL input or generate from current project
- When generating from project, ask for theme name and save location
- Save location options: project or global

---

## 6-Dimension Analysis Framework

For detailed guidelines, see `references/docs/`.

| Dimension | Check Points | Reference |
|-----------|--------------|-----------|
| **1. Color** | Contrast (WCAG AA 4.5:1), brand usage ≤10%, saturation, light/dark mode | color.md |
| **2. Typography** | Hierarchy, line-height, font weight, alignment | typography.md |
| **3. Spacing** | Grid system (4pt), whitespace, alignment | layout.md |
| **4. Border-radius** | Consistency, unified style | component.md |
| **5. Shadow** | Hierarchy, meaning, avoid generic | component.md |
| **6. Interaction** | 8 states (default/hover/focus/active/disabled/loading/error/success), feedback | motion.md |

### Quick Analysis Checklist

| Issue Type | Common Problems |
|------------|-----------------|
| Color | Low contrast, color abuse, washout on colored bg |
| Typography | Inconsistent sizes, line-height, mixed fonts |
| Spacing | No grid, cramped, misaligned |
| Border-radius | Inconsistent sizes, mixed styles |
| Shadow | Too heavy, meaningless, generic |
| Interaction | Missing states, weak feedback |

For complete audit methodology, see `references/docs/polish.md`.

## Design Anti-Patterns

Based on Impeccable design principles:

### Visual
- **DON'T** use gray text on colored backgrounds → use tinted shade
- **DON'T** use pure black (#000) or white (#fff) → always tint
- **DON'T** use "AI color palette" (cyan-on-dark, purple gradients)
- **DON'T** overuse brand colors → accent ≤10%

### Layout
- **DON'T** wrap everything in cards
- **DON'T** nest cards inside cards
- **DON'T** center everything → asymmetry feels more designed

### Typography
- **DON'T** use overused fonts (Inter, Roboto, Arial)
- **DON'T** use too many similar font sizes → muddy hierarchy

### Motion
- **DON'T** use bounce easing → feels dated
- **DON'T** animate layout properties → use transform only
- **DON'T** ignore prefers-reduced-motion

### The AI Slop Test

If someone says "AI made this" and it's immediately obvious → that's the problem.
Distinctive design makes people ask "how was this made?" not "which AI?"

---

## Built-in Themes

**Theme Sources:**
- Built-in: 20 themes stored in `references/styles/`
- User-created: Any `.md` file in `references/styles/` is automatically available

When user creates a new theme (Option D), it is automatically added to the theme list.

### Developer Tools
| Theme | Description | Best For |
|-------|------------|----------|
| Claude | Warm white + ocher orange, rational & warm | AI products, dev tools |
| Minimal Blue | Dark BG + blue accent, minimal | Code editors, assistants |
| Marketplace Dark | Dark + code aesthetics | Dev marketplaces |
| SaaS Dark | Monitoring dark, real-time | DevOps, monitoring |
| Agent Dark | Deep black + vibrant purple | AI agents, creative |

### Business & Enterprise
| Theme | Description | Best For |
|-------|------------|----------|
| Professional Blue | Stable blue + clear hierarchy | SaaS, B2B |
| Trust Finance | Deep blue + gold | Fintech, banking |
| Dashboard Clean | Clean admin, data-focused | Enterprise dashboards |

### Creative Design
| Theme | Description | Best For |
|-------|------------|----------|
| Retro Vibrant | High saturation + bold | Fashion, art |
| Creative Gallery | Image grid + visual first | Portfolios, galleries |
| Neo-Brutalist | Bold borders + solid shadows | Creative agencies |
| Creative Vitality | Vibrant orange + gradients | Creative studios |

### Media & Culture
| Theme | Description | Best For |
|-------|------------|----------|
| Radio Static | B&W + TV static | Podcasts, radio |
| Record Club | Vinyl aesthetic + warm | Music platforms |

### Commerce
| Theme | Description | Best For |
|-------|------------|----------|
| Vibrant Commerce | Orange-red + yellow | E-commerce, retail |

### Brand Styles
| Theme | Description | Best For |
|-------|------------|----------|
| Airbnb | Warm coral + whitespace | Travel, hospitality |
| Linear | Sleek dark + refined | Productivity tools |
| Notion | Clean minimal + content | Documentation |
| Duolingo | Playful bright + gamified | Education |
| Spotify | Dark + vibrant green | Music streaming |

---

## Theme Generation

### Workflow
```
[URL] → [webReader fetch] → [Extract design] → [Generate 14-chapter doc] → [Save]
```

### Reference Documents

Use these docs from `references/docs/` when generating themes:

- **themes-guide.md** - 14-chapter template for theme structure
- **color.md** - Color system guidelines
- **typography.md** - Typography rules
- **layout.md** - Spacing/grid system
- **component.md** - Component design standards
- **motion.md** - Animation principles
- **polish.md** - 6-dimension audit framework

### Generated Theme Structure (14 Chapters)

Every generated theme includes:

1. **Design Philosophy** (设计核心理念)
   - Brand concept / Design philosophy
   - Core keywords (3-5)
   - Why this design?

2. **Color System + Usage Guidelines** (颜色系统 + 使用原则)
   - Primary, background, text, accent colors
   - When to use each color
   - Usage proportion rules
   - Common mistakes

3. **Interaction Philosophy** (交互理念)
   - Animation principles
   - Feedback mechanisms
   - Transition timing

4. **Layout Principles** (布局原则)
   - Spacing strategy (grid system)
   - Whitespace principles
   - Content max-width

5. **Component Design Decisions** (组件设计决策)
   - Why this height/radius/color?
   - Design rationale

6. **Application Scenarios** (应用场景)
   - Suitable project types
   - Adjustments for different scenarios

7. **Common Mistakes** (避免的误区)
   - 5+ common errors
   - Negative checklist

Plus 7 more chapters covering typography, spacing, shadows, components, animations, and use cases.


### Save Location
- Project: `references/styles/[theme-name].md`
- Global: `~/.rico/themes/[theme-name].md`

---

## Theme Application Workflow

```
User Input: rico apply [theme-name]
    ↓
┌──────────────────────────────────────────┐
│  1. Load theme from references/styles/   │
│  2. Detect theme mode (light/dark)      │
│  3. Switch project to theme's mode       │  ← Key: Apply dark → switch to dark
│  4. Analyze code: 6-dimension check     │
│  5. Apply theme colors, spacing, etc.   │
│  6. Generate optimized code             │
│  7. Explain key decisions               │
└──────────────────────────────────────────┘
```

**Theme Mode Application Rule:**
| Project Mode | Theme Mode | Action |
|--------------|------------|--------|
| Single (light/dark) | Dual (both) | Use only project's existing mode colors |
| Single (light/dark) | Single | Apply theme's defined mode |
| Dual (both) | Any | Apply theme's defined mode |

**Never force switch mode.** Theme's dual-mode is "supported", not "required".

### Analysis Dimensions

AI checks these design dimensions:

1. **Color** - Contrast ratios, saturation, brand color usage, light/dark theme support, tinted neutrals
2. **Typography** - Font size, line-height, weight, font family
3. **Spacing** - Grid system, whitespace, compactness
4. **Border Radius** - Size consistency, style unity
5. **Shadow** - Weight, consistency, meaningful
6. **Interaction** - Button/link states, animations, feedback
7. **Icons** - All original icons preserved (SVG, icon fonts, images)
8. **Gradients** - All gradient backgrounds preserved

---

## Design Reference Files

Located in `references/docs/`:

- **color.md** - Color design reference
- **component.md** - Component design reference
- **layout.md** - Layout design reference
- **motion.md** - Animation design reference
- **polish.md** - Design audit reference
- **themes-guide.md** - Theme generation prompt template
- **typography.md** - Typography design reference

---


### Mode Detection

| Project Mode | Theme Support | Action |
|--------------|---------------|--------|
| Dual-mode | Both defined | Generate CSS variables for both |
| Light-only | Any | Apply light mode only (don't auto-add dark) |
| Dark-only | Any | Apply dark mode only (don't auto-add light) |

**Note:** Only generate missing mode if user explicitly requests it. Don't auto-generate dark/light mode unless asked.

### Key Decisions to Explain

- Theme mode strategy
- Icon handling (preserve vs adapt)
- Gradient handling (preserve vs adapt)
- Impeccable principles applied

---

## Technical Stack Support

Auto-adapt to: React, Vue, Angular, HTML, Sass/SCSS, Tailwind, Next.js, Mini Programs

| Stack | Support | Handling |
|-------|---------|----------|
| React | Full | JSX, styled-components, CSS Modules |
| Vue | Full | Vue SFC, scoped styles |
| Angular | Full | Component styles |
| HTML/CSS | Full | CSS variables |
| Sass/SCSS | Full | Variables, mixins |
| Tailwind | Full | Theme config |
| Mini Programs | Full | rpx, custom components |

---

## Best Practices

### Choosing Theme

| Project Type | Recommended Themes |
|--------------|-------------------|
| Developer Tools | Claude, Minimal Blue, Marketplace Dark |
| AI Agents | Agent Dark, Creative Vitality |
| Enterprise | Professional Blue, Trust Finance |
| Creative Brands | Retro Vibrant, Neo-Brutalist |
| Audio/Music | Radio Static, Record Club, Spotify |
| E-commerce | Vibrant Commerce |
| Brand Style | Airbnb, Linear, Notion |

### Combining Themes
```
rico use Minimal Blue colors + Neo-Brutalist borders
```

### Fine-tuning
```
rico create theme: example.com
User: Colors too dark → AI: Adjusting lighter...
User: Larger border-radius → AI: Increasing to 12px...
```

---

## Output Format

Generated code includes:

1. **CSS Variables** - Complete system with OKLCH color space
2. **Component Styles** - Button, input, card, nav adapted to theme
3. **Responsive Design** - Mobile, tablet, desktop breakpoints
4. **Accessibility** - WCAG 2.1 AA compliant
5. **Code Comments** - Key design decisions explained
6. **Motion** - prefers-reduced-motion support

**Always include decision summary:**
- Theme mode strategy
- Icon/gradient handling rationale
- Impeccable principles applied

---

## Quick Examples

### User: rico optimize this website

```
[Read code] → [Analyze 6 dimensions] → [Show menu A/B/C/D] → [User selects] → [Confirm] → [Generate]
```

### User: rico use Claude style

```
[Load claude.md] → [Show style preview] → [Confirm] → [Apply to code]
```

### User: rico create theme: stripe.com

```
[Fetch stripe.com] → [Extract design] → [Generate doc] → [Save] → [Confirm] → [Apply?]
```

## Theme Naming Convention

All themes follow **"Style + Color/Feature"** naming.

This naming convention helps users quickly understand each theme's core characteristics and applicable scenarios.

---

## Integration

This skill integrates with:

- **webReader tool** - Fetch target pages for theme generation
- **Read tool** - Read existing code files
- **Write/Edit tools** - Generate optimized code

All operations require user confirmation before execution.
