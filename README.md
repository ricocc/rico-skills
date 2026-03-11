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

## Skill Overview

| Skill | Purpose | Key Features |
|-------|---------|--------------|
| **rico-resource-article** | Generate curated content articles | Step-by-step workflow, any domain, optional screenshots |
| **rico-ui-ux-themes** | Optimize website design | 20 themes, reverse engineer any site, natural language tweaks |

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




**Last Updated**: 2026-03-

- **Github**: [@ricocc](https://github.com/ricocc)

- **X**:  [@ricouii](https://x.com/ricouii)

- **Blog**: [ricoui.com](https://ricoui.com)

- **WeChat**: Rico的设计漫想

<p align="left">
  <img src="https://ricoui.com/assets/about/wx.png" alt="WeChat QR" width="600">
</p>
