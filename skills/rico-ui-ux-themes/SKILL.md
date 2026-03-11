---
name: rico-ui-ux-themes
description: |
 UI/UX design optimization toolkit with 20 built-in themes and custom theme generation.
  Applies design systems with color, typography, spacing optimization for any tech stack.
  Use when user says "rico optimize", "rico 优化设计", "rico use style", "rico 用风格", 
  or asks to optimize website design/优化网站设计, apply a theme/应用主题, generate themes/生成主题.

license: MIT
metadata:
  author: RicoUI (@ricouii)
  version: 1.0.0
  user-invocable: true
---

# Triggers

This skill supports two trigger modes:

**Mode 1: Explicit Command (rico prefix)**
- rico optimize design / rico 优化设计
- rico use [theme] style / rico 用 [主题] 风格
- rico create theme: [url] / rico 制作主题：[url]
- rico list themes / rico 有哪些主题

**Mode 2: Natural Language**
- "Optimize this website's visual design"
- "Apply Airbnb style to this page"
- "Generate a theme from stripe.com"

If command ambiguous, respond with help message listing examples.

# Examples

- rico optimize this website / rico 优化这个网站
- rico use Claude style / rico 用 Claude 风格
- rico create theme: duolingo.com / rico 制作主题：duolingo.com
- rico list themes / rico 有哪些主题
- Optimize my page design / 优化我的页面设计
- create theme for this project



# Core Instructions

1. **For optimization**: Analyze provided website or UI code, apply selected theme, and output adjusted CSS/JS/React/Vue code with proper design system implementation.

2. **For theme creation**: Use visual reverse engineering via webReader tool on provided URL to analyze design patterns, extract color schemes, typography, spacing, and generate complete 14-chapter theme documentation saved to `references/styles/[theme-name].md`.

3. **For theme application**: Load theme from `references/styles/`, analyze current code against design principles, perform 8-dimension check (color, typography, spacing, border-radius, shadow, interaction, icons, gradients), and generate optimized code with CSS variables and component styles.

4. **Natural language adjustments**: Handle requests like "make it more vibrant" by modifying color saturation, "increase rounded corners" by adjusting border-radius values, or "add more whitespace" by updating spacing system.

5. **Provide explanations**: Always explain key design decisions and "why" behind changes to help users understand the design system.

---

## Optimization Analysis Framework

Before optimization, analyze the current state and make informed decisions based on design principles.

### 1. Theme Mode Detection & Adaptation

→ *Consult [color reference](references/docs/color.md) for dual-mode color systems. Also see Impeccable's color principles below.*

**Impeccable Color Principles:**
- Use **OKLCH** color space for perceptually uniform palettes
- Add subtle brand hue to neutrals (tinted neutrals: chroma 0.01)
- Never use pure black (#000) or pure gray—always tint
- Follow 60-30-10 rule: 60% neutrals, 30% secondary, 10% accent

**DO**: Detect existing theme mode support in the project
**DO**: Check if selected theme has both light and dark color definitions
**DO**: Ensure optimized styles work in all detected modes
**DON'T**: Apply single-mode styles to a dual-mode project without adaptation
**DON'T**: Ignore existing dark mode implementation

**Detection Checklist:**
- Look for `prefers-color-scheme` media queries
- Look for `[data-theme]`, `[data-mode]`, `.dark`, `.dark-mode` selectors
- Look for CSS variables with `-dark` suffix or light/dark pairs

**Adaptation Decision Matrix:**

| Project Mode | Theme Support | Recommended Action |
|-------------|--------------|-------------------|
| Dual-mode | Both defined | Generate CSS variables for both modes |
| Dual-mode | Only dark | Option A: Generate light mode via OKLCH inversion; Option B: Ask user |
| Dual-mode | Only light | Option A: Generate dark mode via OKLCH inversion; Option B: Ask user |
| Light-only | Any | Apply light mode colors, adapt if theme is dark-first |
| Dark-only | Any | Apply dark mode colors, adapt if theme is light-first |

**When theme lacks a mode (e.g., Agent Dark only has dark colors):**
- Use OKLCH color space to generate complementary light/dark variants
- Maintain brand color hue while adjusting lightness
- Or inform user and ask for preference

**Dark Mode Specific (from Impeccable):**
- Dark mode is NOT inverted light mode
- Use lighter surfaces for depth (not shadows)
- Reduce text font weight slightly in dark mode
- Never use pure black—use oklch(12-18%) dark gray

### 2. Icon Handling

**Impeccable Interaction Principles:**
- Every interactive element needs 8 states: Default, Hover, Focus, Active, Disabled, Loading, Error, Success
- Focus rings: Use `:focus-visible`, never `outline: none` without replacement
- Touch targets: Minimum 44x44px

**DO**: Analyze icon purpose before making changes
**DO**: Preserve functional icons that convey meaning (navigation, actions, status)
**DO**: Adapt icon colors for theme consistency when appropriate
**DON'T**: Remove icons without understanding their purpose
**DON'T**: Replace icon systems without migration strategy

**Icon Analysis Framework:**

| Icon Type | Purpose | Optimization Approach |
|-----------|---------|----------------------|
| Functional | Navigation, actions, status indicators | Preserve, adapt color if needed |
| Decorative | Visual enhancement, brand identity | Can adapt style/color to match theme |
| Interactive | Buttons, toggles, clickable elements | Maintain recognizability, adapt to theme |
| Status | Success, error, warning indicators | Keep semantic meaning, adapt colors |

**Color Adaptation Guidelines:**
- SVG icons: Adjust `fill`, `stroke`, or use `currentColor`
- Icon fonts: Ensure font-family is maintained, adjust color property
- Image icons: Consider CSS filters for dark/light mode adaptation

### 3. Gradient Evaluation

**DO**: Understand gradient purpose before making changes
**DO**: Consider if gradient serves a functional role (CTA emphasis, visual hierarchy)
**DO**: Adapt gradient colors while preserving structure when appropriate
**DON'T**: Replace gradients with solid colors without evaluating purpose
**DON'T**: Ignore gradient's role in brand identity

**Gradient Analysis Framework:**

| Gradient Purpose | Example | Optimization Approach |
|-----------------|---------|----------------------|
| Brand identity | Hero backgrounds, signature buttons | Adapt colors, preserve gradient structure |
| CTA emphasis | Primary action buttons | Evaluate if theme's button style is more effective |
| Visual depth | Card backgrounds, overlays | Adapt to theme's depth language |
| Decorative | Accents, highlights | Consider theme's aesthetic direction |

**Decision Factors:**
- Does the selected theme have a specific gradient style?
- Is the gradient a key brand element or functional tool?
- Would solid colors better serve the theme's aesthetic?
- User preference (ask if unclear)

### 4. Typography Analysis

→ *Consult [typography reference](references/docs/typography.md). Also see Impeccable principles below.*

**Impeccable Typography Principles:**
- Use **modular scale** with fewer sizes but more contrast (xs, sm, base, lg, xl+)
- Choose distinctive fonts—avoid Inter, Roboto, Open Sans (too generic)
- Use `ch` units for measure (max-width: 65ch)
- Line-height scales inversely with line length
- Minimum 16px body text for accessibility
- Use `font-display: swap` and match fallback metrics

### 5. Spacing & Layout Analysis

→ *Consult [layout reference](references/docs/layout.md). Also see Impeccable principles below.*

**Impeccable Spatial Principles:**
- Use **4pt base grid** (not 8pt) for granularity: 4, 8, 12, 16, 24, 32, 48, 64, 96
- Use `gap` instead of margins for sibling spacing
- Cards are overused—use spacing and alignment for grouping
- Never nest cards inside cards
- Use container queries (`@container`) for component-level responsiveness
- Create hierarchy through multiple dimensions: size, weight, color, position, space

### 6. Motion & Animation Analysis

→ *Consult [motion reference](references/docs/motion.md). Also see Impeccable principles below.*

**Impeccable Motion Principles:**
- Use `prefers-reduced-motion` for accessibility (35% of adults over 40 have vestibular disorders)
- Exit animations should be ~75% of enter duration
- Use stagger with cap—don't stagger too many items
- Perceived performance: 80ms threshold feels instant

### 8-Dimension Analysis Checklist

When analyzing code, evaluate these dimensions and document findings:

1. **Color** - Contrast ratios (WCAG AA 4.5:1, AAA 7:1), saturation levels, brand color usage (≤10%), theme mode support, tinted neutrals
2. **Typography** - Font scale, line-height rhythm, weight distribution, font family choices (distinctive vs generic), readability
3. **Spacing** - Grid system used (4pt base), whitespace rhythm, compactness level, gap vs margin usage
4. **Border Radius** - Size consistency, style unity with theme, avoid over-rounding
5. **Shadow** - Weight, consistency, purpose (depth vs emphasis), subtle is better
6. **Interaction** - 8 states implemented, hover/focus/active states, animations, feedback mechanisms
7. **Icons** - System used, purpose classification, theme compatibility, accessibility
8. **Gradients** - Purpose identification, theme fit assessment, brand identity preservation

---

## Design Anti-Patterns (What NOT to Do)

Based on Impeccable's anti-patterns and common AI generation mistakes:

### Color Anti-Patterns
- **DON'T use gray text on colored backgrounds**—it looks washed out; use a shade of the background color instead
- **DON'T use pure black (#000) or pure white (#fff)**—always tint; they don't exist in nature
- **DON'T use the "AI color palette"**—cyan-on-dark, purple-to-blue gradients, neon accents on dark
- **DON'T overuse brand colors**—accent works because it's rare (≤10% of page)

### Typography Anti-Patterns
- **DON'T use overused fonts**—Inter, Roboto, Arial, Open Sans, system defaults (unless appropriate)
- **DON'T use monospace as lazy shorthand for "technical"**—it should serve a real purpose
- **DON'T use too many font sizes close together**—create muddy hierarchy; use fewer sizes with more contrast
- **DON'T ignore fallback fonts**—always define proper font stacks

### Layout Anti-Patterns
- **DON'T wrap everything in cards**—not everything needs a container
- **DON'T nest cards inside cards**—visual noise, flatten the hierarchy
- **DON'T use identical card grids**—same-sized cards repeated endlessly look templated
- **DON'T center everything**—left-aligned with asymmetry feels more designed
- **DON'T use the hero metric layout template**—big number, small label, gradient accent

### Visual Details Anti-Patterns
- **DON'T use glassmorphism everywhere**—blur effects should have purpose, not decorative
- **DON'T use sparklines as decoration**—tiny charts that convey nothing meaningful
- **DON'T use generic drop shadows**—safe and forgettable
- **DON'T use rounded rectangles with thick colored border on one side**—lazy accent that rarely looks intentional

### Motion Anti-Patterns
- **DON'T use bounce or elastic easing**—feels dated and tacky; real objects decelerate smoothly
- **DON'T animate layout properties** (width, height, padding, margin)—use transform and opacity only
- **DON'T animate everything**—animation fatigue is real
- **DON'T ignore prefers-reduced-motion**—35% of adults over 40 have vestibular disorders

### Interaction Anti-Patterns
- **DON'T remove focus indicators** without replacement—accessibility violation
- **DON'T use placeholders as labels**—they disappear on input
- **DON'T make every button primary**—hierarchy matters; use ghost buttons, text links
- **DON'T rely on gestures as the only way** to perform actions—provide visible fallbacks

### The AI Slop Test

**Critical quality check**: If you showed this interface to someone and said "AI made this," would they believe you immediately? If yes, that's the problem.

A distinctive interface should make someone ask "how was this made?" not "which AI made this?"

Review the anti-patterns above—they are the fingerprints of AI-generated work from 2024-2025.

---

## Quick Start

### First Time Use

#### 1. Choose a Theme

```
rico 用 Claude 风格 / rico use Claude style
rico 看看有哪些主题 / rico list themes
```

#### 2. Optimize a Page

```
rico 帮我优化这个网站 / rico optimize this website
rico 优化我的首页 / rico optimize my homepage
```

#### 3. Generate Custom Theme

```
rico 制作主题：stripe.com / rico create theme: stripe.com
rico 参考 apple.com 做主题 / rico create theme from: apple.com
```

### Example Conversations

#### User: rico 用 Airbnb 风格优化我的首页 / rico use Airbnb style for my homepage

**AI Response:**

Understood, I'll apply these Airbnb style characteristics:

- Warm coral red primary color (#FF5A5F)
- Large rounded corners (8-12px)
- Generous whitespace, highlight images
- Restrained brand color usage (≤ 10%)

[Reading code and generating optimized code...]

#### User: rico 看看 Trust Finance 主题 / rico show Trust Finance theme

**AI Response:**

**Trust Finance Style**
- Position: Fintech, Banking, B2B
- Primary: Deep Blue #0052CC (secure & trustworthy)
- Secondary: Gold #FFAB00 (wealth & success)
- Features: Small border-radius 6-8px (professional), restrained animations, generous whitespace

Best for: Banking, payments, insurance, enterprise services

---

## Unified Prefix

All commands MUST use the `rico` prefix to trigger this skill.

### Supported Actions (Chinese / English)

**1. One-Click Optimization**
```
rico 帮我优化这个网站
rico optimize this website
rico 让页面更好看
rico improve this page design
rico 优化设计
rico optimize design
rico 优化我的页面
rico optimize my page
```

**2. Style Selection**
```
rico 用 [主题名] 风格
rico use [theme-name] style
rico 用 Claude 风格优化
rico optimize with Claude style
```

**3. Theme Generation**
```
rico 制作主题：[URL]
rico create theme: [URL]
rico 参考 [URL] 做主题
rico create theme from: [URL]
```

**4. Theme Application**
```
rico 用这个主题优化
rico apply this theme
rico 用 Minimal Blue 风格设计
rico design with Minimal Blue style
```

**5. Theme Management**
```
rico 有哪些主题
rico list themes
rico 看看 [主题名] 主题
rico show [theme-name] theme
rico 删除 [主题名] 主题
rico delete [theme-name] theme
```

---

## Built-in Themes (20 Themes)

### Developer Tools Class

| Theme Name | File | Description | Best For |
|------------|------|-------------|----------|
| **Claude** | `claude.md` | Warm white + ocher orange, rational & warm | AI products, dev tools, tech docs |
| **Minimal Blue** | `minimal-blue.md` | Dark BG + blue accent, minimal & professional | Code editors, AI assistants, dev tools |
| **Marketplace Dark** | `marketplace-dark.md` | Dark theme + code aesthetics | Dev marketplaces, tech resources, open source directories |
| **SaaS Dark** | `saas-dark.md` | Monitoring dark theme, real-time status | DevOps, monitoring, observability platforms |
| **Agent Dark** | `agent-dark.md` | Deep black + vibrant purple, artistic | AI agents, creative studios, experimental projects |

### Business & Enterprise Class

| Theme Name | File | Description | Best For |
|------------|------|-------------|----------|
| **Professional Blue** | `professional-blue.md` | Stable blue + clear hierarchy | SaaS, B2B, enterprise apps, analytics |
| **Trust Finance** | `trust-finance.md` | Deep blue + gold, secure & professional | Fintech, banking, B2B, insurance |
| **Dashboard Clean** | `dashboard-clean.md` | Clean admin, data-focused | Enterprise dashboards, admin panels, B2B platforms |

### Creative Design Class

| Theme Name | File | Description | Best For |
|------------|------|-------------|----------|
| **Retro Vibrant** | `retro-vibrant.md` | High saturation + bold visual | Coffee brands, fashion, indie music, art exhibitions |
| **Creative Gallery** | `creative-gallery.md` | Image grid + visual first | Design resources, inspiration galleries, portfolios |
| **Neo-Brutalist** | `neo-brutalist.md` | Bold borders + solid shadows | Creative agencies, fashion brands, indie games |
| **Creative Vitality** | `creative-vitality.md` | Vibrant orange + gradients, dynamic | Creative studios, art products, design agencies |

### Media & Culture Class

| Theme Name | File | Description | Best For |
|------------|------|-------------|----------|
| **Radio Static** | `radio-static.md` | B&W dominant + TV static | Community radio, podcasts, audio blogs |
| **Record Club** | `record-club.md` | Vinyl aesthetic + warm earth tones | Record stores, music platforms, vinyl communities |

### Commerce Class

| Theme Name | File | Description | Best For |
|------------|------|-------------|----------|
| **Vibrant Commerce** | `vibrant-commerce.md` | Orange-red + yellow, action-oriented | E-commerce, retail, shopping, flash sales |

### Brand Style Class

| Theme Name | File | Description | Best For |
|------------|------|-------------|----------|
| **Airbnb** | `airbnb.md` | Warm coral + generous whitespace | Travel, hospitality, sharing economy |
| **Linear** | `linear.md` | Sleek dark + refined interactions | Productivity tools, SaaS apps |
| **Notion** | `notion.md` | Clean minimal + content-focused | Knowledge management, documentation |
| **Duolingo** | `duolingo.md` | Playful bright + gamified elements | Education, language learning, gamification |
| **Spotify** | `spotify.md` | Dark theme + vibrant green accent | Music streaming, media apps |

---

## Theme Generation Workflow

```
User Input: rico 制作主题：[URL]
    ↓
┌─────────────────────────────────────────┐
│  1. Fetch target page (webReader tool)   │
│  2. Visual reverse engineering           │
│  3. Generate design system doc           │
│  4. Save to references/styles/[name].md  │
│  5. Show preview, await confirmation    │
│  6. Ask if apply to project              │
└─────────────────────────────────────────┘
```

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

---

## Theme Application Workflow

```
User Input: rico 用 [主题] 风格优化
    ↓
┌─────────────────────────────────────────┐
│  1. Load theme from references/styles/    │
│  2. Detect project theme mode support     │
│  3. Check theme's light/dark definitions │
│  4. Determine adaptation strategy        │
│  5. Analyze code: 8-dimension check     │
│  6. Apply Impeccable design principles   │
│  7. Generate optimized code              │
│  8. Explain key decisions               │
└─────────────────────────────────────────┘
```

### Analysis Dimensions (8-Dimension Check)

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

## Theme File Structure

```
references/styles/
├── claude.md              # Built-in - Claude style
├── minimal-blue.md        # Built-in - Minimal Blue
├── marketplace-dark.md    # Built-in - Marketplace Dark
├── saas-dark.md           # Built-in - SaaS Dark
├── agent-dark.md          # Built-in - Agent Dark
├── professional-blue.md   # Built-in - Professional Blue
├── trust-finance.md       # Built-in - Trust Finance
├── dashboard-clean.md     # Built-in - Dashboard Clean
├── retro-vibrant.md       # Built-in - Retro Vibrant
├── creative-gallery.md    # Built-in - Creative Gallery
├── neo-brutalist.md       # Built-in - Neo-Brutalist
├── creative-vitality.md   # Built-in - Creative Vitality
├── radio-static.md        # Built-in - Radio Static
├── record-club.md         # Built-in - Record Club
├── vibrant-commerce.md    # Built-in - Vibrant Commerce
├── airbnb.md              # Built-in - Airbnb style
├── linear.md              # Built-in - Linear style
├── notion.md              # Built-in - Notion style
├── duolingo.md            # Built-in - Duolingo style
├── spotify.md             # Built-in - Spotify style
└── [user-generated].md    # Custom themes
```

---

## Complete Example Conversation

### Scenario: Generating and Applying a Theme

#### User: rico 制作主题：stripe.com

**AI Response:**

[Fetching stripe.com via webReader...]

Analyzing Stripe's visual design...
- Deep blue primary (#0052CC) conveying trust
- Clean gradients for depth
- 8px border-radius (professional but friendly)
- Generous whitespace for readability
- Fast animations (100-150ms)

Generating theme file...

**Preview: Trust Finance Style**
- Position: Fintech, Banking, B2B
- Primary: #0052CC (blue - secure & trustworthy)
- Secondary: #FFAB00 (gold - wealth & success)
- Border-radius: 6-8px
- Animations: 150-200ms
- Spacing: 8px grid, generous whitespace

✅ Saved to: `references/styles/trust-finance.md`

确认这个主题吗？/ Confirm this theme?

#### User: 确认

**AI Response:**

✅ Theme confirmed!

需要应用到项目吗？/ Apply to project?

#### User: 应用到我的登录页 / Apply to my login page

**AI Response:**

[Reading login page code...]

**Analysis Results:**
- Project mode: Dual-mode detected (supports light/dark via `prefers-color-scheme`)
- Theme mode: Claude theme has both light and dark definitions ✓
- Icons: Found 5 functional icons (navigation), 2 status icons
- Gradients: Found 1 gradient button (CTA)

**Applying Claude style with Impeccable principles:**

**Key Decisions:**
1. Theme mode: Dual-mode CSS variables generated
2. Icons: Preserved all functional icons, adapted colors for theme consistency
3. Gradient: Preserved CTA gradient, adapted brand colors to Claude's ocher orange
4. Applied 8-dimension check:
   - Color: Adjusted to warm white tones, OKLCH recommended
   - Typography: Changed to distinctive font (not Inter), 14px base
   - Spacing: 4pt grid system, compact layout
   - Border-radius: 6px for buttons, 8px for cards
   - Shadow: Subtle shadows for depth
   - Interaction: 8 states implemented, focus-visible rings added
   - Icons: Preserved with theme-compatible colors
   - Gradients: Preserved CTA gradient structure

**Generated code includes:**
- CSS variables for both light and dark modes
- prefers-reduced-motion support
- WCAG AA compliant contrast ratios

[Generating optimized code...]

---

## Bilingual Support

This skill supports both Chinese and English commands seamlessly.

### Chinese Examples (中文示例)

```
rico 用 Claude 风格优化这个页面
rico 制作主题：stripe.com
rico 看看有哪些主题
rico 优化我的登录页
```

### English Examples (英文示例)

```
rico optimize this page with Claude style
rico create theme: stripe.com
rico list all themes
rico optimize my login page
```

Both language inputs will trigger the same functionality.

---

## Theme Naming Convention

All themes follow **"Style + Color/Feature"** naming:

**Developer Tools:**
- Minimal Blue（极简蓝）
- Marketplace Dark（市场深色）
- SaaS Dark（SaaS 深色）
- Agent Dark（智能体深色）

**Business & Enterprise:**
- Professional Blue（专业蓝）
- Trust Finance（信任金融）
- Dashboard Clean（清爽仪表盘）

**Creative Design:**
- Retro Vibrant（复古鲜艳）
- Creative Gallery（创意画廊）
- Neo-Brutalist（新粗野主义）
- Creative Vitality（创意活力）

**Media & Culture:**
- Radio Static（广播噪点）
- Record Club（唱片俱乐部）

**Commerce:**
- Vibrant Commerce（活力电商）

**Brand Styles:**
- Airbnb、Linear、Notion、Duolingo、Spotify

This naming convention helps users quickly understand each theme's core characteristics and applicable scenarios.

---

## Technical Stack Support

Automatically adapts to: React, Vue, Angular, Mini Programs, Pure HTML, Sass/SCSS, Tailwind, Next.js

| Tech Stack | Support | Special Handling |
|------------|---------|-----------------|
| **React** | ✅ Full | JSX, styled-components, CSS Modules |
| **Vue** | ✅ Full | Vue SFC, scoped styles |
| **Angular** | ✅ Full | Component styles, global styles |
| **Mini Programs** | ✅ Full | rpx, custom components |
| **HTML/CSS** | ✅ Full | Native CSS, CSS variables |
| **Sass/SCSS** | ✅ Full | Variables, mixins, nesting |
| **Tailwind** | ✅ Full | Theme config, custom classes |
| **Next.js** | ✅ Full | CSS Modules, Tailwind |

Auto-detects tech stack and generates appropriate code format.

---

## Best Practices

### Choosing the Right Theme

1. **Developer Tools** → Claude, Minimal Blue, Marketplace Dark, SaaS Dark
2. **AI Agents & Creative Studios** → Agent Dark, Creative Vitality
3. **Enterprise Apps** → Professional Blue, Trust Finance, Dashboard Clean
4. **Creative Brands** → Retro Vibrant, Creative Gallery, Neo-Brutalist
5. **Audio & Music** → Radio Static, Record Club, Spotify
6. **E-commerce** → Vibrant Commerce
7. **Brand Style** → Airbnb, Linear, Notion, Duolingo

### Combining Themes

Reference multiple themes' design elements:

```
rico use Minimal Blue colors + Neo-Brutalist borders
```

### Fine-tuning Themes

Adjust after generation:

```
rico create theme: example.com
User: Colors too dark
AI: Adjusting lighter...

User: Larger border-radius
AI: Increasing to 12px...
```

---

## Output Format

Optimized code includes:

1. **CSS Variables** - Complete color, spacing, typography system with appropriate theme mode support (using OKLCH recommended)
2. **Component Styles** - Button, input, card, navigation styles adapted to theme
3. **Responsive Design** - Mobile, tablet, desktop breakpoints
4. **Accessibility** - WCAG 2.1 AA compliant (4.5:1 for text, 3:1 for UI)
5. **Code Comments** - Explanation of key design decisions and rationale
6. **Icon Handling** - Icons preserved or adapted with explanation
7. **Gradient Handling** - Gradients preserved, adapted, or replaced with explanation
8. **Motion Support** - Include prefers-reduced-motion support

**Output should include a brief decision summary:**
- Theme mode strategy applied (dual-mode / single-mode)
- Icon handling decisions with rationale
- Gradient handling decisions with rationale
- Key Impeccable principles applied

---

## Integration with AI Tools

This skill integrates with:
- **webReader tool** - Fetch target pages for theme generation
- **Read tool** - Read existing code files
- **Write/Edit tools** - Generate optimized code
- **Bash tool** - Execute file operations

---

## File Management

### Theme Storage Location

All themes are stored in: `references/styles/[theme-name].md`

### User-Generated Themes

Custom themes are automatically saved and can be:
- Listed via: `rico list themes`
- Viewed via: `rico show [theme-name] theme`
- Applied via: `rico use [theme-name] style`
- Deleted via: `rico delete [theme-name] theme`
