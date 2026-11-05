# rico-skills

English | [中文](README.zh.md)

Claude Code Skills for content creation, design optimization, and resource curation.

---

## Installation

### Quick Install

```bash
npx skills add https://github.com/ricocc/rico-skills
```

### Or via Plugin Marketplace

```bash
/plugin marketplace add ricocc/rico-skills
```

**Note**: Plugin marketplace requires the repository to be published to GitHub.

---

## Available Skills

### rico-resource-article

**Resource Recommendation Article Generator** - Create high-quality curated content articles through multi-turn interaction.

**Trigger when**: User explicitly wants to generate a recommendation article (must include action + article intent)

```
# ✅ Correct triggers
Write a recommendation article about shadcn/ui component libraries, recommend 8
生成一篇关于 shadcn/ui 组件库的推荐文章，推荐 8 个
帮我写一个 Figma 插件推荐文章
Create a resource list article about Python frameworks

# ❌ Don't trigger (just answering questions)
What are good React component libraries?
推荐 8 个组件库
```

**Workflow:**
1. **Collect** - AI gathers candidate items based on topic
2. **Confirm** - User confirms the list
3. **Title** - AI generates 3 title options, user selects
4. **Article** - Full article with Front Matter, descriptions, screenshots

**Output:**
- Markdown article with YAML Front Matter
- Each item: name, description, key features, official link
- Optional automatic screenshots via ScreenshotOne or urlscan.io

📄 **Detailed Guide**: [guides/rico-resource-article.md](guides/rico-resource-article.md)

---

### rico-ui-ux-themes

**Website Design Optimization** - One-click visual design optimization with 20 built-in themes.

This skill supports **two trigger modes**:

**Mode 1: Explicit Commands (with rico prefix)**

```
rico optimize this website
rico use Claude style
rico create theme: stripe.com
```

**Mode 2: Natural Language**

```
Make my website look more professional
帮我优化一下这个页面的设计
Make it look like Linear
```

**Available Commands:**

| Command | Description |
|---------|-------------|
| `rico use [theme] style` | Apply built-in theme |
| `rico create theme: [url]` | Generate theme from website |
| `rico list themes` | Show all available themes |
| `rico show [theme] theme` | View theme details |
| `rico combine [theme-A] colors + [theme-B] borders` | Mix themes |

**20 Built-in Themes:**
- Developer Tools: Claude, Minimal Blue, Marketplace Dark, SaaS Dark
- AI Agents: Agent Dark, Creative Vitality
- Enterprise: Professional Blue, Trust Finance, Dashboard Clean
- Creative: Retro Vibrant, Creative Gallery, Neo-Brutalist
- Audio/Music: Radio Static, Record Club, Spotify
- E-commerce: Vibrant Commerce
- Brand Style: Airbnb, Linear, Notion, Duolingo

**Fine-tuning (natural language):**
```
User: Colors too dark → AI adjusts lighter
User: Larger border-radius → AI increases to 12px
```

📄 **Detailed Guide**: [guides/rico-ui-ux-themes.md](guides/rico-ui-ux-themes.md)

---

### rico-design-md

**Design System Document Generator** - Convert any website into design system documents, or convert between design token formats.

**Trigger when**: User wants to create DESIGN.md, extract design tokens, analyze a brand's design system, or convert between formats.

```
# ✅ Correct triggers
rico DESIGN.md https://linear.app
rico tokens https://stripe.com
rico 全部输出 github
Create a DESIGN.md for linear.app
Extract design tokens from stripe.com
分析 GitHub 的设计系统

# Format conversion
rico 把 DESIGN.md 转为 tokens
```

**5 Output Formats:**

| File | Format | Description |
| ------ | -------- | ------------- |
| `DESIGN.md` | Markdown | Full style reference with brand voice, tokens, components |
| `preview.html` | HTML | Self-contained visual design system preview page |
| `tokens.json` | DTCG JSON | Standard design tokens, compatible with style dictionary |
| `variables.css` | CSS | CSS custom properties grouped by category |
| `theme.css` | CSS | Tailwind v4 `@theme` format |

**Default:** `rico DESIGN.md [url]` generates both `DESIGN.md` + `preview.html`.

**Output saved to:** `themes/{brand-slug}/`

📄 **Detailed Guide**: [guides/rico-design-md.md](guides/rico-design-md.md)

---

### rico-writer

**Chinese Humanized Writing & De-AI Editor** - Write, expand, polish, or diagnose Chinese text so it reads specific, clear, and opinionated, like a real person wrote it.

**Trigger when**: User asks to write, expand, polish, or diagnose Chinese articles, tweets, product intros, reviews, tutorials, or asks to remove AI flavor / sound more human.

```
# ✅ Correct triggers
帮我把这段文章去 AI 味润色一下
把我的笔记扩写成一篇公众号文章
Rewrite this review as a Chinese X/Twitter thread, keep my judgment
这段文案帮我写得像人说话一点

# ❌ Don't trigger (pure translation / proofreading / formatting)
把这段翻译成英文
帮我检查错别字
把这个 markdown 排版整理一下
```

**What it does:**
- Preserves facts, numbers, technical terms, the author's stance and certainty level
- Removes binary-contrast shells ("不是A，而是B"), pseudo-insight markers ("本质上""更重要的是"), lecturing openers ("记住这句话"), and unsupported hype ("必备神器")
- Replaces anthropomorphic verbs ("给模型喂素材" → "把素材提供给模型")
- Enforces punctuation conventions (double quotes instead of 「」, no em-dashes in original prose)
- Never fabricates experiences, usage durations, data, or decision thresholds
- Does not dictate openings, article structure, or endings - they follow the author's material

📄 **Detailed Guide**: [guides/rico-writer.md](guides/rico-writer.md)

---

## Skill Overview

| Skill | Purpose | Key Features |
| ------- | --------- | -------------- |
| **rico-resource-article** | Generate curated content articles | Step-by-step workflow, any domain, optional screenshots |
| **rico-ui-ux-themes** | Optimize website design | 20 themes, reverse engineer any site, natural language tweaks |
| **rico-design-md** | Extract design systems from websites | 5 output formats, format conversion, visual preview |
| **rico-writer** | Chinese writing & de-AI polishing | Fact-safe rewriting, sentence-pattern & punctuation rules, articles to tweets |

---

## Configuration

### Basic Usage
All skills work out of the box. No configuration required.

### Optional: Screenshot Service

For automatic screenshots in `rico-resource-article`:

```bash
mkdir -p .rico-skills
cp .env.example .rico-skills/.env
# Add your API keys to .rico-skills/.env
```

**Services:**
- [ScreenshotOne](https://screenshotone.com/) - 100/month free
- [urlscan.io](https://urlscan.io/) - 5,000/day free


---

## Update

```bash
/plugin
# Navigate to Marketplaces → rico-skills → Update marketplace
```

---


## License

MIT License

---




**Last Updated**: 2026-11-05

- **Github**: [@ricocc](https://github.com/ricocc)

- **X**:  [@ricouii](https://x.com/ricouii)

- **Blog**: [ricoui.com](https://ricoui.com)

- **WeChat**: Rico的设计漫想

<p align="left">
  <img src="https://ricoui.com/assets/about/wx.png" alt="WeChat QR" width="600">
</p>
