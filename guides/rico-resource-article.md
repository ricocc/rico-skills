# Rico Resource Article - Detailed Guide

Resource recommendation article generator that creates high-quality curated content through multi-turn interaction.

---

## Core Features

- **Intelligent Step-by-Step Generation**: Collect candidates → User confirmation → Generate titles → Generate article
- **Wide Domain Support**: Tools, resources, component libraries, plugins, websites, frameworks, services, etc.
- **Multiple Generation Modes**: Smart step-by-step, one-shot, outline-based generation
- **Professional Format Standards**: Complete Front Matter + Standard article structure
- **Bilingual Support**: Chinese and English input/output
- **Optional Screenshots**: Automatically add screenshots for recommended websites

---

## Trigger Rules

### ✅ Will Trigger Skill

Must include both: **Generation Action** + **Article Type**

```
Generate a recommendation article about shadcn/ui
Write a tool recommendation article
Create a resource list article
Recommend 8 component libraries and generate article
Write a recommendation article about React hooks
```

### ❌ Will NOT Trigger Skill

Only asking or conversing, without article generation intent:

```
Recommend 8 component libraries
What are some good tools
What are some React hooks
```

---

## Generation Modes

### Mode 1: Smart Step-by-Step Generation (Recommended)

```
User: Generate a recommendation article about mesh gradient generators, recommend 3

AI: Collecting candidate items...

    Here are 3 candidates:

    1. Mesh Gradients
       - URL: https://www.meshgradients.com/
       - Reason: Simple and intuitive, one-click random generation
       - Differentiator: Rich built-in presets, supports PNG/SVG export

    2. CSS Hero Mesher
       - URL: https://csshero.org/mesher/
       - Reason: Focused on frontend developers, outputs CSS code directly
       - Differentiator: WYSIWYG, responsive-friendly

    3. Mesh Gradient Generator
       - URL: https://github.com/nicepkg/mesh-gradient-background-generator
       - Reason: Open source and free, supports offline use
       - Differentiator: Customizable features, batch export support

    Please confirm to continue?

User: Confirm

AI: Please select title style:

    A. Pain Point Style
       - A1. Say Goodbye to Boring Backgrounds! 3 Mesh Gradient Tools
       - A2. Design Inspiration Dried Up? Try These 3 Gradient Tools

    B. Exploration Style
       - B1. Inspiration Exploration: 3 Niche Mesh Gradient Generators
       - B2. Deep Dive: Gradient Tools for More Textured Backgrounds

    C. Recommendation Style
       - C1. 3 Mesh Gradient Tools to Make Your Design Stand Out
       - C2. Curated Selection: Niche and Useful Gradient Generators

    Please select (e.g., A1) or suggest modifications.

User: B1

AI: [Generate complete article...]
```

### Mode 2: One-Shot Generation

User knows exactly what they want, generate directly:

```
User: Generate a recommendation article about Figma plugins, recommend 5, use "Curated Selection" style title

AI: [Directly generate complete article, no multi-turn confirmation needed]
```

### Mode 3: Outline-Based Generation

User already provided a list:

```
User: Generate article based on this outline:

1. Navbar Gallery https://www.navbar.gallery/ navigation components
2. SupaHero https://supahero.io/ hero section components
3. Cta Gallery https://www.cta.gallery/ CTA components

AI: [Generate complete article based on outline]
```

---

## Article Structure

### Front Matter (Metadata)

```yaml
---
title: Selected Title
publishDate: 2026-03-11
read: 5
description: English subtitle describing the article
tags:
  - Chinese Tag
  - English Tag
img: "/assets/blog/cover-filename.jpg"
img_alt: "Image description"
---
```

### Opening Paragraphs (3-4 paragraphs)

- Background: Industry status and problems
- Value: Core significance of the topic
- Lead-in: Content to be recommended in the article

### Body (Recommended Items)

```markdown
### 1. Project Name

- URL: [https://example.com](https://example.com)
- Description: Core positioning, main features, problems solved...
- Advantages: Unique value, applicable scenarios...

    ![project-name.jpg](project-name.jpg)
```

### Closing Summary

- Subheading that elevates the theme (## Heading 2)
- 3-4 paragraphs of summary, combining trends with suggestions

---

## Writing Style Requirements

### Avoid Common AI Writing Issues

| Issue | ❌ Wrong Example | ✅ Correct Example |
|-------|------------------|-------------------|
| Over-parallelism | "It has efficiency, flexibility, and scalability" | "It's efficient and flexible, easy to scale" |
| Vague description | "This tool is very powerful with very rich features" | "Contains 200+ components, covering forms, navigation, etc." |
| Three-part formula | "Not only... but also... and..." | Use natural and varied sentence structures |
| Negative parallelism | "It doesn't need complex config, doesn't need extra dependencies" | "Simple config, zero dependencies" |

### Writing Principles

- Professional but not obscure
- Each recommendation has clear use cases
- Original content, don't copy official descriptions
- Don't add author signature

---

## Optional Screenshot Feature

After article generation, you can choose to automatically add screenshots.

### Supported Services

| Service | Free Quota | Speed | API Key |
|---------|-----------|-------|---------|
| **ScreenshotOne** | 100/month | 2-5 seconds | Required |
| **urlscan.io** | 5,000/day | 10-30 seconds | Required |

### Configuration

```bash
# Create config directory
mkdir -p .rico-skills

# Copy example config
cp .env.example .rico-skills/.env

# Edit .rico-skills/.env
SCREENSHOTONE_ACCESS_KEY=your_key
URLSCAN_API_KEY=your_key
SCREENSHOT_DEFAULT_SERVICE=screenshotone
SCREENSHOT_DEFAULT_SIZE=1600x900
```

### Get API Key

- **ScreenshotOne**: https://screenshotone.com/ (Free registration, 100/month)
- **urlscan.io**: https://urlscan.io/ (Login → Settings → API Keys)

### Screenshot Sizes

| Size | Aspect Ratio | Use Case |
|------|--------------|----------|
| 1920×1080 | 16:9 | Full HD |
| 1600×900 | 16:9 | **Default** - Blog articles |
| 1440×900 | 16:10 | Mac style |
| 1200×800 | 3:2 | Tablet devices |

You can specify when requesting: "Use 1920×1080 screenshots"

---

## FAQ

### Skill not triggering?

Ensure both are included:
1. **Generation Action**: generate, write, create, help me write
2. **Article Type**: recommendation article, resource list article

### Generated article too long/short?

You can specify when confirming the candidate list:
- "Keep each description to 2 sentences"
- "Make each recommendation more detailed, 3-4 sentences"

### Want to adjust style?

After generation, you can adjust with natural language:
- "Make the tone more professional"
- "Add some usage suggestions"
- "Add another summary paragraph at the end"

---

## Complete Example

```
User: Generate a recommendation article about online design tools, recommend 5 niche and useful ones

AI: [Collect candidates]

User: Confirm, use exploration style title

AI: [Generate title options]

User: B2

AI: [Generate complete article]

    Need to add screenshots?
    - Enter "n" to skip
    - Enter "y" to use ScreenshotOne
    - Enter "u" to use urlscan.io

User: y

AI: [Generate screenshots and insert into article]

    ✅ Added 5 screenshots
```

---

## File Location

```
skills/
└── rico-resource-article/
    ├── SKILL.md          # Core skill definition
    └── evals/
        └── evals.json    # Test cases
```

---

**Last Updated**: 2026-03-11
