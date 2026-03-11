---
name: rico-resource-article
description: |
  Resource recommendation article generator with multi-turn workflow and domain adaptation.
  Creates structured articles with verifiable data, proper formatting, and professional style.
  Use when user explicitly requests to generate/write/create a recommendation article (生成/写/创建 + 推荐文章/资源列表).
  Must include both action + article intent. Don't trigger on simple questions like "推荐几个工具".

---

# Resource Recommendation Article Generator

This skill helps you create high-quality resource recommendation articles through a multi-turn interactive workflow, ensuring accurate content, complete structure, and professional style.

## Core Features

- **Intelligent Step-by-Step Generation**: Collect candidates → User confirmation → Generate titles → Generate article
- **Domain Adaptation**: Auto-detect topic domain (Design/Development/Marketing/Product/Content) and apply professional terminology and writing style
- **Broad Domain Support**: Technical tools, design resources, development frameworks, online services, physical products, etc.
- **Multiple Generation Modes**: Smart step-by-step, one-shot, outline-based generation
- **Professional Format Standards**: Complete Front Matter and standard article structure
- **Data Accuracy**: Only use verifiable data (GitHub Stars, component counts, official metrics)

# Triggers

This skill supports two trigger modes:

**Mode 1: Explicit Command (rico article prefix)**
- rico article [topic] / rico 文章 [主题]
- rico article 8 design tools / rico 文章 8个设计工具

**Mode 2: Natural Language (explicit article intent required)**
- "Generate a recommendation article about shadcn/ui"
- "写一篇工具推荐文章"
- "Create a resource list article"

**Important**: This skill ONLY triggers when user explicitly wants to generate an article.
Do NOT trigger for simple questions like "recommend 8 tools" or "有哪些好用的工具" - answer directly.

# Examples

**Trigger examples:**
- rico article 8 React hooks libraries
- rico 文章 10个设计工具
- Generate a recommendation article about shadcn/ui
- 写一篇 Figma 插件推荐文章

**Do NOT trigger examples (just asking or conversing):**
- "推荐 8 个组件库" - Answer directly
- "What are some good tools?" - Conversational inquiry
- "Generate 8 resources" - Unclear request without article intent
- "What plugins do you recommend?" - Question-only inquiry
- "生成 8 个资源" - 无明确文章生成意图的模糊请求
- "推荐几个好用的插件" - 单纯询问，不生成文章


---

## 🎯 Mode Selection and Priority

**Default Mode**: Intelligent Step-by-Step Generation

**Mode Selection Priority**:
1. **User explicitly specifies mode** → Use requested mode
2. **User provides outline list** → Use Outline-Based Generation
3. **User only needs simple list** → Use Quick Generation
4. **Default fallback** → Intelligent Step-by-Step Generation

**When in doubt, always use Intelligent Step-by-Step Generation** as it ensures highest quality through user confirmation.

---

## 🌟 Recommended Mode: Intelligent Step-by-Step Generation

This is the smartest, most controllable generation mode, ensuring article quality through multi-turn interaction.

### Workflow

```
User inputs topic and quantity
  ↓
Step 0: Domain Detection (Auto-detect topic domain)
  ↓
Step 1: Collect candidate items (URL + recommendation reason + differentiating features + verifiable data)
  ↓
User confirms candidate list
  ↓
Step 2: Generate 6 title options (pain-point, exploratory, recommendation)
  ↓
User selects title
  ↓
Step 3: Generate complete article with domain-specific writing style
  ↓
Step 4: Ask about screenshots (Optional - ALWAYS ask after article generation)
```

### Step 0: Domain Detection

**Auto-detect the topic domain and apply corresponding writing template**

#### Detection Rules

| Domain | Keywords (EN/CN) | Target Audience | Focus Areas |
|--------|-----------------|----------------|-------------|
| **Design** | Figma, Sketch, UI, UX, design system, component, mockup, prototype, 插件, 设计, 组件库, 设计系统 | Designers | 创意效率, 视觉质量, 设计规范, Design System, 交付流程 |
| **Development** | React, Vue, Angular, API, framework, library, TypeScript, npm, 框架, 库, 开发 | Developers | 技术栈, 性能优化, 代码质量, GitHub Stars, 社区生态 |
| **Marketing** | SEO, ROI, conversion, A/B test, analytics, email marketing, 转化率, 营销, 分析 | Marketers | ROI, 数据驱动, 转化效果, 受众分群, 自动化 |
| **Product** | Prototype, user research, roadmap, collaboration, 原型, 用户调研, 路线图 | Product Managers | 功能完整性, 团队协作, 用户价值, 决策支持 |
| **Content** | Writing, CMS, publishing, editing, 写作, 编辑, 发布 | Content Creators | 创作效率, 内容质量, 分发渠道, AI 辅助 |
| **General** | *fallback* | General Users | 易用性, 功能全面, 实用性 |

#### Detection Process

```
1. Extract keywords from user topic
2. Match against domain keyword library
3. Calculate confidence score based on keyword matches
4. If confidence ≥80%: Auto-select domain and inform user
5. If confidence 50-79%: Ask user to confirm
6. If confidence <50%: Use General template
```

#### Example Interaction

**High Confidence (Auto-select):**
```markdown
### User Input
"生成一篇 Figma 插件推荐文章，推荐 6 个"

### AI Response
🔍 **检测到领域: Design (设计领域)**

基于关键词 "Figma" + "插件"，将使用设计领域专业模板，侧重：
- ✅ 设计工作流集成
- ✅ 创意效率提升
- ✅ Design System 兼容性

[继续执行 Step 1: 收集候选项目...]
```

**Medium Confidence (Ask User):**
```markdown
### User Input
"生成一篇图片压缩工具推荐文章"

### AI Response
🤔 **检测到多个可能的领域方向**

"图片压缩工具" 可以是：
- A. 面向设计师（设计工作流、批量处理、保持质量）
- B. 面向开发者（API 集成、自动化处理、性能优化）

请问您希望侧重哪个方向？(回复 A 或 B，或直接跳过使用通用模板)
```

---

### Step 1: Collect Candidate Items

Based on user's topic requirements, collect matching projects/websites/tools and list them in the following format:

**Candidate List Format:**

```
**1. [Project Name]**
- URL: {{website link}}
- Recommendation reason: {{2-3 sentences explaining why it's worth recommending}}
- Differentiating features: {{How it differs from similar projects}}
- Data: {{Verifiable metrics - GitHub Stars, component counts, official numbers}}

**2. [Project Name]**
...
```

**⚠️ DATA ACCURACY RULES (CRITICAL):**

**1. Only Use Verifiable Data**
- ✅ **USE**: GitHub Stars, GitHub Forks, NPM weekly downloads, Component/Template counts (from official site)
- ✅ **USE**: Contributor count, Last updated date, License type, Tech stack details
- ❌ **DON'T USE**: User counts, Customer numbers, Efficiency percentages, Fake metrics
- ❌ **DON'T USE**: "100万+ 用户", "效率提升 10 倍", "转化率提升 25%" (unless officially verified)

**2. How to Collect Data**
- Visit GitHub page → Get Stars, Forks, Contributors, Last Updated
- Visit official site → Get component/template counts, feature lists
- Visit NPM page → Get weekly/monthly download counts
- If unsure about data → Either omit or mark as "approximate"

**⚠️ CRITICAL RULES (MUST FOLLOW):**

**1. NEVER Hallucinate Projects or URLs**
- ❌ DO NOT invent or fabricate project names, URLs, or websites
- ❌ DO NOT create fake resources or fictional tools
- ✅ ONLY recommend real, verifiable projects that actually exist
- ✅ If unsure about a project's existence, either skip it or ask the user

**2. Verify URLs Before Listing**
- ✅ Ensure URLs are accessible and valid
- ✅ If a URL seems suspicious or broken, note it for user verification
- ❌ DO NOT include projects with broken or dubious URLs

**Important: If you encounter these situations, ask the user first:**
- Topic direction is unclear
- Insufficient candidate items (inform how many you found)
- Multiple related sub-topics discovered, need to confirm focus
- Certain project URLs need verification
- **Unable to find enough real, verifiable candidates** (tell user and ask for guidance)

After listing candidates, **ALWAYS wait for user confirmation**, tell the user:
```
Above are {{number}} candidate items. Please confirm:
1. Do you need to adjust any items?
2. Do you need to add or remove any items?
3. Reply 'y' or 'yes' to confirm and proceed
```

### Step 2: Generate Title Options

After user confirms the candidate list, generate **6 article titles in different styles** based on these items:

```
### Please select your preferred title style:

**A. Pain-Point Type**
- A1. {{title}}
- A2. {{title}}

**B. Exploratory Type**
- B1. {{title}}
- B2. {{title}}

**C. Recommendation Type**
- C1. {{title}}
- C2. {{title}}

Please tell me which title you choose (e.g., A1), or suggest modifications.
```

**Title Style References:**
- **Pain-Point Type**: Say no to homogenization!, Break through bottlenecks!, Farewell to XXX
- **Exploratory Type**: Inspiration exploration!, In-depth analysis!, XXX exploration
- **Recommendation Type**: Curated, Essential, Must-know, Make XXX, XXX essentials

### Step 3: Generate Complete Article

After user selects a title, generate the complete article.

**First, determine the article folder path:**

1. Translate the Chinese title to a descriptive English slug
2. Use lowercase, hyphen-separated format
3. Inform the user: "Article will be saved to: `{{article-slug}}/index.md`"
4. If using screenshots, they will be saved in the same folder

**Example:**
```
Title: 精选 4 款最受欢迎的渐变生成器，每个设计师都值得收藏
Slug: featured-4-most-popular-gradient-generators
Path: featured-4-most-popular-gradient-generators/index.md
```

Then proceed with generating the article content.

## Article Structure Standards

### File Organization

**Article files should follow this structure:**

```
{{article-slug}}/
└── index.md          # Article content
├── screenshot-1.png   # Screenshots (if any)
├── screenshot-2.png
└── ...
```

**Path Explanation:**
- Articles are saved in current working directory
- Folder name: `{{article-slug}}/` (e.g., `featured-4-most-popular-gradient-generators/`)
- Article file: always `index.md`
- Screenshots: saved in the same folder as article

**Cover Image Location (separate from article folder):**
```
assets/blog/
└── cover-{{article-slug}}.jpg  # Manually added cover images
```

**Naming rules:**
- **Article folder**: lowercase English, hyphen-separated, descriptive and concise
  - Example: `shadcn-ui-component-libraries/`, `featured-4-most-popular-gradient-generators/`
  - Rule: Translate Chinese title to English, use lowercase, connect with hyphens
  - Format: `[adjective]-[number]-[category]-[items]` or similar descriptive pattern
  - Examples:
    - "精选 4 款最受欢迎的渐变生成器" → `featured-4-most-popular-gradient-generators/`
    - "设计师必备的 8 个 Figma 插件" → `essential-8-figma-plugins-for-designers/`
    - "2026 年最佳 Vue 组件库" → `best-vue-component-libraries-2026/`
- **File**: always `index.md`
- **Screenshots**: saved in same folder as article, named after project (e.g., `cssgradient-io.png`)

### 1. Front Matter (Metadata)

```yaml
---
title: {{user selected title}}
publishDate: {{today's date: YYYY-MM-DD}}
read: {{estimated reading time in minutes, typically 6-12}}
description: {{English subtitle, concise summary for SEO}}
tags:
  - {{English tag1}}
  - {{English tag2}}
  - {{Chinese tag1}}
  - {{Chinese tag2}}
img: "/assets/blog/cover-{{article-slug}}.jpg"
img_alt: "{{Chinese description of cover image}}"
---
```

**Important Notes:**
- **img** and **img_alt** are manually added cover images (not auto-generated)
- Image path should follow pattern: `/assets/blog/cover-{{article-slug}}.jpg`
- **description** should be in English, concise and SEO-friendly
- **read** is estimated reading time in minutes
- **tags** should include both Chinese and English keywords (4-6 items total)

### 2. Opening Paragraphs (3-4 paragraphs)

- **Paragraph 1**: Present industry background and current status
- **Paragraph 2**: Explain core value and significance of the topic
- **Paragraph 3**: Introduce the content to be recommended in the article
- **Paragraph 4** (optional): Explain why these resources are being recommended

### 3. Body Content

Write content for each confirmed item in the following format:

```markdown
### {{number}}. {{Project Name}}

- **官网**: [{{URL}}]({{URL}})
- **简介**: {{Core positioning, main functions, problems solved}}, covering {{specific content scope}}, {{special features/characteristics}}.
- **优势**: {{Why it's worth recommending, unique value, applicable scenarios, problems solved}}.
```

**Body Requirements:**
- Number of recommended items: As requested by user, typically 6-12
- Arrange in logical order (from basic to advanced, or from general to specialized)
- Description should explain core positioning and main content scope
- Advantages should highlight differentiated value and applicable scenarios
- Language should be professional but accessible, target reader appropriate

**Aggregation Platforms (if applicable):**

If there are aggregation platforms, list them separately:

```markdown
Additionally, here are {{number}} aggregation platforms that collect {{platform purpose}}:

### {{number}}. {{Project Name}}
...
```

### 4. Conclusion (2 parts)

- **Subheading** (## level-2 heading): Should elevate the theme, not too generic
  - Example: ## Vibe Coding: Returning Design to "Creation" Itself
  - Or: ## Componentized Inspiration: Focusing Creativity on the Core

- **Summary paragraphs** (3-4 paragraphs):
  - Explain the overall value of these resources
  - Connect with current trends (e.g., AI assistance, automation)
  - Provide usage recommendations
  - Encourage reader action

**Do not add author byline.**

---

### Step 4: Ask About Screenshots (ALWAYS ask after article generation)

**After article generation is complete, ALWAYS ask the user:**

```markdown
✅ Article generated successfully! Saved to: `{{article-slug}}/index.md`

📸 Would you like to add screenshots for the recommended websites?

Quick Options:
- Type "n" or "no" - Skip screenshots
- Type "y" or "yes" - Use default service (ScreenshotOne)
- Type "u" or "urlscan" - Use urlscan.io (requires API key)

Default size: 1600×900 (16:9) - Best for blog articles
```

**If user says "no" or "n":** Skip and end the workflow.

**If user says "yes" or "y":** Proceed to screenshot process (see 📸 Optional: Add Screenshots section below).

**If user wants custom size:** Accept and proceed with specified dimensions.

---

## 📌 Other Generation Modes

### Mode 1: One-Shot Generation

For scenarios where user knows exactly what they want and doesn't need multiple confirmations.

**Workflow:**
1. Understand user's topic
2. Collect candidate items directly
3. Generate one attention-grabbing title
4. Generate complete article

**Article Format**: Same as above (Front Matter + intro + body + conclusion)

### Mode 2: Outline-Based Generation

For scenarios where user has already provided a candidate list.

**Workflow:**
1. Read the outline provided by user
2. Write description and advantages for each item
3. Generate title
4. Generate complete article

**Additional Handling:**
- If outline includes category tags (e.g., 3D, Animated, Minimal), reflect them in the "Advantages" section of corresponding items
- If outline includes URLs, verify link validity
- Adjust item count based on outline content

### Mode 3: Quick Generation

Generate only the recommendation list, without intro, conclusion, or Front Matter.

```markdown
### {{number}}. {{Project Name}}

- **官网**: [{{URL}}]({{URL}})
- **简介**: {{1-2 sentences}}
- **优势**: {{1-2 sentences}}
```

**Note:** Images are not included in quick generation mode. Users can manually add screenshots if needed.

---

## Writing Style Requirements

1. **Professional**: Accurate terminology, clear logic
2. **Practical**: Each recommendation has clear use cases and value points
3. **Readable**: Moderate paragraph length, avoid lengthy discourse
4. **Natural**: Avoid common AI writing issues (excessive parallelism, vague descriptions, three-part rule, negative parallelism, vague attribution)
5. **Original**: Avoid copying official introductions, rephrase in your own words

### Avoid Common AI Writing Issues

**Issue 1: Excessive Parallelism**
- ❌ "It has efficiency, flexibility, and scalability."
- ✅ "It's efficient and flexible, with easy scalability."

**Issue 2: Vague Descriptions**
- ❌ "This component library is very powerful and feature-rich."
- ✅ "Contains 200+ components, covering forms, data display, navigation, and other scenarios."

**Issue 3: Three-Part Rule**
- ❌ "Not only... but also... and..." / "Whether... or... all..."
- ✅ Use natural, varied sentence structures

**Issue 4: Negative Parallelism**
- ❌ "It doesn't need complex configuration, additional dependencies, or learning curve."
- ✅ "Simple configuration, zero dependencies, fast to get started."

**Issue 5: Vague Attribution**
- ❌ "Many people believe..." / "It is well known that..."
- ✅ Directly state opinions or provide specific data sources

---

## Special Notes

### Content Guidelines

- Tags should include Chinese and English keywords, 4-6 items
- URLs must be accurate and clickable
- Avoid exaggerated promotion, maintain objectivity and professionalism
- **Do not add author byline**
- **Images are optional** - users can manually add screenshots to the generated article if needed

### ⚠️ Safety and Compliance Rules (CRITICAL)

**1. Prohibited Content**
- ❌ DO NOT recommend pirated, cracked, or illegal software/resources
- ❌ DO NOT promote copyright-infringing content
- ❌ DO NOT recommend resources that violate terms of service
- ❌ DO NOT include adult content, gambling, or illegal activities
- ✅ ONLY recommend legitimate, legal, and ethical resources

**2. Accuracy Requirements**
- ❌ DO NOT hallucinate or fabricate projects, URLs, or websites
- ❌ DO NOT create fictional resources or tools
- ✅ ONLY recommend real, verifiable projects
- ✅ If insufficient real candidates exist, inform the user and ask for guidance

**3. Verification**
- ✅ Verify that recommended resources actually exist
- ✅ Ensure URLs are accessible and safe
- ❌ DO NOT include suspicious or broken URLs without warning the user

**4. Disclosure**
- ✅ If you're uncertain about a resource's legitimacy, note it
- ✅ If knowledge base has no matching content, tell user honestly
- ❌ DO NOT make up recommendations to satisfy the request

---

## Mode Selection Guide

| User Need | Recommended Mode | Reason |
|---------|---------|------|
| "Recommend X items... and generate an article" | Intelligent Step-by-Step | Let user participate in confirmation, highest quality |
| "Generate a recommendation article about XXX" | Intelligent Step-by-Step | Multi-turn interaction ensures accuracy |
| Provided an outline list | Outline-Based Generation | Quick completion, user confirmed content |
| Only need recommendation list | Quick Generation | Concise and efficient |
| Clear topic and quantity | One-Shot Generation | Fast output |

---

## Complete Example

### User Input:
"Write a recommendation article about shadcn/ui component libraries, recommend 8"

### AI Step 1: Collect Candidate Items

```
Here are 8 collected shadcn/ui component libraries:

**1. [Aceternity UI]**
- URL: https://ui.aceternity.com/
- Recommendation reason: Hottest component library in shadcn/ui ecosystem, 120k+ developers using it
- Differentiating features: Deeply integrated with Framer Motion, extensive visual effects components

**2. [Kibo UI]**
- URL: https://www.kibo-ui.com/
- Recommendation reason: Fills gaps in shadcn/ui's advanced components
- Differentiating features: Provides color picker, rich text editor and other advanced components

...

Above are 8 candidate items. Please confirm:
1. Do you need to adjust any items?
2. Do you need to add or remove any items?
3. Reply 'y' or 'yes' to confirm and proceed
```

### User: y

### AI Step 2: Generate Title Options

```
### Please select your preferred title style:

**A. Pain-Point Type**
- A1. Say No to Homogenization! 8 Curated Shadcn/UI Component Libraries
- A2. Break Through Design Bottlenecks! 8 Must-Try Shadcn/UI Extension Libraries

**B. Exploratory Type**
- B1. Inspiration Exploration! 8 Shadcn/UI-Focused Component Libraries
- B2. In-Depth Analysis: 8 Efficiency-Boosting Shadcn/UI Resources

**C. Recommendation Type**
- C1. 8 Shadcn/UI Component Libraries to Double Development Efficiency
- C2. Developer Essentials: 8 Quality Shadcn/UI Extension Libraries

Please tell me which title you choose (e.g., A1), or suggest modifications.
```

### User: A1

### AI Step 3: Generate Complete Article

**File structure:**
```
content/shadcn-ui-component-libraries/
└── index.md
```

**Content:**
```markdown
---
title: Say No to Homogenization! 8 Curated Shadcn/UI Component Libraries
publishDate: 2026-03-03
read: 8
description: Top 8 Awesome Shadcn UI Component Libraries
tags:
  - Shadcn UI
  - Component Libraries
  - UI组件库
  - 组件库推荐
img: "./cover-shadcn-ui.jpg"
img_alt: "8 Curated Shadcn/UI Component Libraries"
---

shadcn/ui is one of the hottest component systems today...

### 1. Aceternity UI

- **官网**: [https://ui.aceternity.com/](https://ui.aceternity.com/)
- **简介**: Hottest component library in shadcn/ui ecosystem with 120k+ developers, covering 200+ production-quality components...
- **优势**: Deeply integrated with Framer Motion and Tailwind CSS, providing glow cards, text gradients, 3D globe and other unique visual components...

...
```

---

## 📸 Optional: Add Screenshots

After article generation, offer users the option to add screenshots for recommended websites.

### When to Ask

Ask after article generation is complete:

```markdown
✅ Article generated successfully!

Would you like to add screenshots for the recommended websites?

Quick Options:
- Type "n" or "no" - Skip screenshots
- Type "y" or "yes" - Use default service (ScreenshotOne)
- Type "u" or "urlscan" - Use urlscan.io (requires API key)

Current default: ScreenshotOne (JPG format, smaller file size)
Default size: 1600×900 (16:9) - 适合博客文章

💡 **自定义截图尺寸 / Customize Screenshot Size:**
   Just mention it when requesting / 在请求时直接说明:
   - "Use 1920×1080" / "用 1920×1080 截图"
   - "Screenshot at 1440×900" / "截图尺寸 1440×900"
```

### Service Selection

If user chooses "yes" (uses default) or selects a specific service:

**If user selected "yes" (default service):**
```markdown
Using default service: ScreenshotOne

✓ Fast (2-5 seconds per screenshot)
✓ 100 free screenshots/month
✗ Requires API key
```

**If user wants to compare services:**
```markdown
Available screenshot services:

【ScreenshotOne】
✓ Fast (2-5 seconds)
✓ 100 free screenshots/month
✗ Requires API key

【urlscan.io】
✓ Free: 5,000 Public Scans/day
✓ Free: 1,000 Unlisted Scans/day  
✓ Free: 50 Private Scans/day
✗ Requires API key
✗ Slower than ScreenshotOne

Default: ScreenshotOne (configured in .env)
```

### Configuration Check

**IMPORTANT: Always check .env file first before asking user**

**Step 1: Check if .env file exists and has API key**

```
Check order:
1. .rico-skills/.env (project-level)
2. ~/.rico-skills/.env (user-level)

If API key found → Use it directly ✓
If not found → Go to Step 2
```

**Step 2: If no API key configured**

```markdown
Checking ScreenshotOne configuration...

⚠️ API Key not found in .env file

Get your free API key:
1. Visit: https://screenshotone.com/
2. Sign up (free, 2 minutes)
3. Copy your API Key

Choose how to configure:

[A] 💾 Create .env file (Recommended) - Key will be saved for future use
[B] 🔑 Enter API key now (One-time) - Key will only be used for this session
[C] ⏭️ Skip screenshots - Add manually later

Please reply A, B, or C:
```

**If user selects [A] - Create .env file:**
```markdown
Great! I'll create the .env file for you.

Please enter your API Key: [wait for user input]

✓ Creating .rico-skills/.env file...
✓ Saving API key...
✓ Configuration complete! Key saved for future use.

Now proceeding with screenshots...
```

**If user selects [B] - One-time use:**
```markdown
Please enter your API Key (will be used for this session only): [wait for user input]

✓ Key received. Proceeding with screenshots...
(Note: You'll need to enter the key again next time)
```

**If user selects [C] - Skip:**
```markdown
✓ Skipping screenshots. You can add them manually later.

Manual screenshot guide:
- Save screenshots to: say-goodbye-to-stock-photos-3-ai-image-generators/
- Recommended size: 1600×900 (16:9)
- Naming: {website-name}.png
```

**For urlscan.io (same flow):**
```markdown
Checking urlscan.io configuration...

⚠️ API Key not found in .env file

Get your free API key:
1. Visit: https://urlscan.io/user/ (login required)
2. Go to Settings → API Keys
3. Copy your API Key

Choose how to configure:

[A] 💾 Create .env file (Recommended) - Save for future use
[B] 🔑 Enter API key now (One-time) - Use for this session only
[C] ⏭️ Skip screenshots - Add manually later

Please reply A, B, or C:
```

**After saving to .env, show confirmation:**
```markdown
✓ API key saved to .rico-skills/.env

Your configuration:
- Service: ScreenshotOne
- API Key: sk_•••••••••••••••• (hidden)
- Default size: 1600×900

This key will be automatically used for future screenshot requests.
```

### Screenshot Dimensions

**Default Screenshot Size: 1600×900 (16:9)**

This is the optimal size for most blog and article layouts, providing:
- Clear visibility of website details
- Good aspect ratio for responsive design
- Reasonable file size for web loading

**Customize Screenshot Size:**

If you need different dimensions, specify when requesting screenshots:

```markdown
Example requests:
- "使用 1920×1080 尺寸截图"
- "用 1440×900 截图"
- "截图尺寸设为 1200×800"
- "Take screenshots at 1920×1080"
```

**Available Sizes:**
| Size | Aspect Ratio | Best For |
|------|--------------|----------|
| 1920×1080 | 16:9 | Full HD displays |
| 1600×900 | 16:9 | **Default** - Blog posts |
| 1440×900 | 16:10 | Mac-style displays |
| 1200×800 | 3:2 | Tablets, smaller screens |
| 1200×600 | 2:1 | Wide banners |
| 1200×900 | 4:3 | Traditional displays |

**Note:** urlscan.io has limited size options (typically 1920×1080 or similar). For custom sizes, use ScreenshotOne or manual screenshot tools.

### Screenshot Process

Once configured:

**For ScreenshotOne:**
```markdown
Found 8 URLs to screenshot

[1/8] Capturing https://ui.aceternity.com/...
  Waiting for screenshot...
✓ aceternity-ui.png (2.3s)

[2/8] Capturing https://www.kibo-ui.com/...
✓ kibo-ui.png (1.8s)

...

✓ Screenshots completed: 8/8
Saved to: ./ (current directory)
```

**For urlscan.io:**
```markdown
Found 8 URLs to screenshot

[1/8] Submitting scan for https://ui.aceternity.com/...
  Scan UUID: abc123-def456-ghi789
  Waiting for scan to complete...
  Downloading screenshot...
✓ aceternity-ui.png (8.2s)

[2/8] Submitting scan for https://www.kibo-ui.com/...
  Scan UUID: xyz789-uvw456-rst123
  Waiting for scan to complete...
  Downloading screenshot...
✓ kibo-ui.png (7.5s)

...

✓ Screenshots completed: 8/8
Saved to: ./ (current directory)
```

### Update Article with Screenshots

**After screenshots are saved, ALWAYS update the article to include images.**

For each recommended item, insert the screenshot image after the heading:

**Before (without screenshot):**
```markdown
### 1. Aceternity UI

- **官网**: [https://ui.aceternity.com/](https://ui.aceternity.com/)
- **简介**: ...
```

**After (with screenshot):**
```markdown
### 1. Aceternity UI

![Aceternity UI](aceternity-ui.jpg)

- **官网**: [https://ui.aceternity.com/](https://ui.aceternity.com/)
- **简介**: ...
```

**Image insertion rules:**
1. Insert image immediately after the item heading (`### N. Project Name`)
2. Use format: `![Project Name](filename.jpg)`
3. Alt text should be the project name or brief description
4. Image files should be in the same directory as index.md

**After updating the article, show confirmation:**
```markdown
✓ Article updated with 3 screenshots

Updated sections:
- Section 1: meshgradients-com.jpg
- Section 2: csshero-mesher.jpg
- Section 3: nicepkg-mesh-gradient.jpg
```

### Screenshot File Naming

Screenshots are saved in the same directory as the article:

```
shadcn-ui-component-libraries/
├── index.md              # Article content
├── aceternity-ui.png     # Screenshot 1
├── kibo-ui.png           # Screenshot 2
├── ...
└── footer-design.png     # Screenshot 8
```

**Naming rule:** `{project-name}.png`
- Extracted from domain or project name
- Lowercase, hyphen-separated
- Example: `aceternity-ui.png`, `kibo-ui.png`

### Error Handling

If screenshots fail:

```markdown
⚠️ Some screenshots failed:
- kibo-ui.png: Timeout (30s)
- footer-design.png: API rate limit

✓ Successful: 6/8
❌ Failed: 2/8

You can manually add these screenshots later if needed.
```

### Manual Screenshot Guide

If users prefer manual screenshots or hit API limits:

```markdown
## Manual Screenshot Guide

### System Tools
- Mac: Cmd+Shift+4 (select area)
- Windows: Win+Shift+S (select area)

### Online Tools
- Screenshot.guru: https://screenshot.guru/
- Screenshot.rocks: https://screenshot.rocks/

### Recommended Dimensions
- Default: 16:9 (1600×900)
- Alternatives: 16:10, 3:2, 2:1, 4:3

### File Organization
Save screenshots in the same directory as the article:
- Article: `content/shadcn-ui-component-libraries/index.md`
- Screenshots: `content/shadcn-ui-component-libraries/*.png`

This keeps related files together and makes management easier.
```
