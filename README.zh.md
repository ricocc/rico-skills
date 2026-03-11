# rico-skills

[English](README.md) | 中文

Claude Code 技能集合，用于内容创作、设计优化和资源策展。

---

## 安装

### 快速安装

```bash
npx skills add https://github.com/ricocc/rico-skills
```

### 或通过插件市场

```bash
/plugin marketplace add ricocc/rico-skills
```

**注意**：插件市场需要将仓库发布到 GitHub。

---

## 可用技能

### rico-resource-article

**资源推荐文章生成器** - 通过多轮交互创建高质量的资源推荐类文章。

**触发条件**：用户明确表达生成文章的意图（必须同时包含动作 + 文章意图）

```
# ✅ 正确触发
生成一篇关于 shadcn/ui 组件库的推荐文章，推荐 8 个
帮我写一个 Figma 插件推荐文章
Write a recommendation article about React hooks

# ❌ 不触发（只是回答问题）
shadcn/ui 有哪些推荐的组件库？
推荐几个好用的工具
```

**工作流程：**
1. **搜集** - AI 根据主题搜集候选项目
2. **确认** - 用户确认列表内容
3. **标题** - AI 生成 3 个标题选项，用户选择
4. **文章** - 生成完整文章，包含 Front Matter、描述、截图

**输出：**
- Markdown 格式文章，带 YAML Front Matter
- 每个项目包含：名称、描述、核心特性、官方链接
- 可选自动截图（ScreenshotOne 或 urlscan.io）

📄 **详细指南**：[guides/rico-resource-article-zh.md](guides/rico-resource-article-zh.md)

---

### rico-ui-ux-themes

**网站设计优化** - 一键优化视觉设计，内置 20 种主题。

此技能支持**两种触发模式**：

**模式 1：显式命令（使用 rico 前缀）**

```
rico optimize this website
rico 用 Claude 风格优化这个页面
rico create theme: stripe.com
```

**模式 2：自然语言**

```
帮我优化一下这个页面的设计
Make my website look more professional
让它看起来像 Linear 的风格
```

**可用命令：**

| 命令 | 描述 |
|------|------|
| `rico use [主题] 风格` | 应用内置主题 |
| `rico 制作主题：[网址]` | 从网站生成主题 |
| `rico 有哪些主题` | 显示所有可用主题 |
| `rico 看看 [主题名] 主题` | 查看主题详情 |
| `rico 用 [主题A] 配色 + [主题B] 边框` | 混合主题 |

**20 种内置主题：**
- 开发者工具：Claude、Minimal Blue、Marketplace Dark、SaaS Dark
- AI Agents：Agent Dark、Creative Vitality
- 企业应用：Professional Blue、Trust Finance、Dashboard Clean
- 创意品牌：Retro Vibrant、Creative Gallery、Neo-Brutalist
- 音频/音乐：Radio Static、Record Club、Spotify
- 电子商务：Vibrant Commerce
- 品牌风格：Airbnb、Linear、Notion、Duolingo

**自然语言调整：**
```
用户：颜色太深了 → AI 调浅一点
用户：圆角再大些 → AI 增加到 12px
```

📄 **详细指南**：[guides/rico-ui-ux-themes-zh.md](guides/rico-ui-ux-themes-zh.md)

---

## 技能概览

| 技能 | 用途 | 核心特性 |
|------|------|----------|
| **rico-resource-article** | 生成资源推荐文章 | 分步流程、任意领域、可选截图 |
| **rico-ui-ux-themes** | 优化网站设计 | 20 种主题、逆向工程任意网站、自然语言调整 |

---

## 配置

### 基础使用
所有技能开箱即用，无需配置。

### 可选：截图服务

为 `rico-resource-article` 启用自动截图：

```bash
mkdir -p .rico-skills
cp .env.example .rico-skills/.env
# 在 .rico-skills/.env 中添加 API 密钥
```

**可用服务：**
- [ScreenshotOne](https://screenshotone.com/) - 免费额度 100 次/月
- [urlscan.io](https://urlscan.io/) - 免费额度 5,000 次/天



---

## 更新

```bash
/plugin
# 导航到 Marketplaces → rico-skills → Update marketplace
```


---

## 许可证

MIT License

---

**最后更新**：2026-03-11

- **维护者**：[推特@ricouii](https://x.com/ricouii)

- **博客**：[ricoui.com](https://ricoui.com)

- **微信公众号**: Rico的设计漫想

<p align="left">
  <img src="https://ricoui.com/assets/about/wx.png" alt="WeChat QR" width="600">
</p>
