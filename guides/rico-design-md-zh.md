# Rico Design MD - 设计系统文档生成器

将任意网站转换为完整的设计系统文档，或在不同设计令牌格式之间转换（DESIGN.md、tokens.json、variables.css、theme.css）。

---

## 这个技能能做什么？

### 核心功能

1. **网站转设计系统** - 输入任意网站 URL，自动提取设计令牌、颜色、排版、间距、阴影和组件样式
2. **多种输出格式** - 生成 DESIGN.md、preview.html、tokens.json（DTCG）、variables.css 和 theme.css（Tailwind v4）
3. **格式转换** - 在任意支持的格式之间转换（如 DESIGN.md 转 tokens.json、variables.css 转 DESIGN.md）
4. **可视化预览** - 生成一个独立的 preview.html 页面，展示完整的设计系统

### 适用场景

- 需要为现有网站生成设计系统文档
- 想要提取设计令牌用于开发实现
- 需要在不同设计令牌格式之间转换
- 想要一个品牌设计系统的可视化参考页面

---

## 触发方式

本技能支持两种触发模式：

**模式 1：显式命令（rico 前缀）**

| 命令 | 输出 |
|------|------|
| `rico DESIGN.md [url]` | DESIGN.md + preview.html（默认） |
| `rico preview [url]` | 仅 preview.html |
| `rico tokens [url]` | 仅 tokens.json |
| `rico variables [url]` | 仅 variables.css |
| `rico theme.css [url]` | 仅 theme.css |
| `rico 全部输出 [品牌]` | 全部 5 个文件 |
| `rico 把 DESIGN.md 转为 tokens` | 格式转换 |

**模式 2：自然语言**

```
为 linear.app 创建 DESIGN.md
提取 stripe.com 的设计令牌
生成 github.com 的预览页面
分析 GitHub 的设计系统
```

---

## 输出结构

所有生成的文件保存在 `themes/{brand-slug}/` 目录下：

```
themes/{brand-slug}/
├── DESIGN.md         # 完整样式参考（默认输出）
├── preview.html      # 可视化设计系统预览（默认输出）
├── tokens.json       # DTCG 格式设计令牌
├── variables.css     # CSS 自定义属性
└── theme.css         # Tailwind v4 @theme
```

---

## 工作流程

### 流程一：生成 DESIGN.md + 预览（默认）

```
用户：rico DESIGN.md https://linear.app
    ↓
步骤 1：收集视觉数据
  • 截图 Hero、导航、CTA、卡片、排版、页脚
  • 检查 DevTools 中的 CSS 变量、@font-face、计算样式
    ↓
步骤 2：提取设计令牌
  • 颜色 → 语义令牌（canvas、surface-1、ink、accent-blue 等）
  • 排版 → 字体族、字号、字重、行高、字间距
  • 间距 → 基础单位检测（4px 或 5px 栅格）
  • 圆角 → xs 到 full 的完整刻度
  • 阴影 → 完整 CSS 语法
    ↓
步骤 3：文档化组件（含所有状态）
  • 导航、按钮、输入框、卡片、页脚
  • 包含 hover、focus、active、selected 状态
    ↓
步骤 4：撰写品牌声音（5-8 句设计评论）
    ↓
步骤 5：撰写 Do's / Don'ts（各 7-8 条，引用具体令牌）
    ↓
步骤 6：生成 DESIGN.md + preview.html
```

### 流程二：单一格式输出

```
用户：rico tokens https://stripe.com
    ↓
仅生成 tokens.json（DTCG 格式）
```

### 流程三：全部输出（5 个文件）

```
用户：rico 全部输出 github
    ↓
生成全部 5 个文件：
  • DESIGN.md、preview.html、tokens.json、variables.css、theme.css
```

### 流程四：格式转换

```
用户：rico 把 DESIGN.md 转为 tokens
    ↓
解析已有的 DESIGN.md → 生成 tokens.json
```

---

## 输出格式详解

### DESIGN.md

一份全面的 Markdown 文档，包含：

- 品牌声音和设计理念
- 颜色系统（含语义令牌名称）
- 排版刻度（含 font-feature-settings）
- 间距系统
- 圆角刻度
- 阴影规格
- 组件文档（含所有状态）
- Do's & Don'ts（引用具体令牌）

### preview.html

一个独立的、单文件的可视化设计系统参考页面：

- 线性从上到下布局（非 bento 网格）
- 章节顺序：Hero → 颜色 → 渐变 → 排版 → 间距与形状 → 阴影 → 深度与表面 → 组件 → Do's & Don'ts
- 所有规范文件的下载链接
- 粘性导航 + 章节锚点
- 滚动触发入场动画
- 响应式设计（移动优先）
- 支持 `file://` 协议直接打开（无外部依赖，仅 Google Fonts）

### tokens.json

DTCG（设计令牌社区组）标准格式：

- 每个令牌包含 `$description`，说明其预期用途
- 按类别分组：颜色、排版、间距、圆角、阴影
- 兼容 style dictionary 和令牌转换工具

### variables.css

CSS 自定义属性，按以下类别分组：

- 颜色、字体族、字号刻度、字重
- 间距、布局、圆角、阴影、表面

### theme.css

Tailwind v4 `@theme` 格式，可直接集成到 Tailwind CSS v4 项目。

---

## 使用示例

### 示例 1：从网站生成设计系统

```
用户：rico DESIGN.md https://linear.app

AI：[从 Linear 网站提取设计令牌]
    [生成 themes/linear/DESIGN.md + themes/linear/preview.html]

    已生成 2 个文件：
    • themes/linear/DESIGN.md - 完整样式参考
    • themes/linear/preview.html - 可视化预览
```

### 示例 2：仅提取令牌

```
用户：rico tokens https://github.com

AI：[从 GitHub 提取令牌]
    [生成 themes/github/tokens.json]

    已生成 DTCG 令牌，包含 6 个类别共 87 个令牌。
```

### 示例 3：格式转换

```
用户：rico 把 DESIGN.md 转为 tokens

AI：[解析已有的 DESIGN.md]
    [将 Markdown 表格转换为 DTCG 格式]

    已生成 themes/github/tokens.json
```

### 示例 4：全部输出

```
用户：rico 全部输出 github

AI：[在 themes/github/ 下生成全部 5 个文件]
    • DESIGN.md
    • preview.html
    • tokens.json
    • variables.css
    • theme.css
```

---

## 边界情况处理

| 场景 | 处理方式 |
|------|----------|
| SPA / 客户端渲染 | 使用 view-source + 网络面板获取 CSS 文件 |
| 压缩的 CSS | 使用 DevTools 计算样式面板 |
| 多主题（亮色/暗色） | 询问用户要文档化哪个主题；提供独立的 `dark/` 子目录 |
| 需要登录的页面 | 聚焦公开的营销页面 |
| 缺失的令牌类别 | 跳过该章节并标注缺失（绝不编造值） |

---

## 文件目录

```
skills/
└── rico-design-md/
    ├── SKILL.md                          # 技能核心定义
    └── references/
        ├── DESIGN-TEMPLATE.md            # 新 DESIGN.md 的模板
        └── themes-github/                # 参考示例（GitHub）
            ├── DESIGN.md                 # 完整的 DESIGN.md 示例
            ├── github-preview.html       # 可视化预览示例
            ├── tokens.json               # DTCG 格式参考
            ├── variables.css             # CSS 自定义属性参考
            └── theme.css                 # Tailwind v4 @theme 参考
```

---

## 常见问题

### 这个技能和 rico-ui-ux-themes 有什么区别？

- **rico-ui-ux-themes**：将已有的设计主题应用到你的网站上进行视觉优化
- **rico-design-md**：从网站中提取设计系统，生成文档和令牌

### 生成的令牌可以直接在项目中使用吗？

可以。所有输出格式都是生产就绪的：
- `tokens.json` 可配合 style dictionary 和令牌转换工具使用
- `variables.css` 可直接导入
- `theme.css` 可集成到 Tailwind v4

### 如果网站同时有亮色和暗色模式怎么办？

技能会询问你要文档化哪个模式。如果暗色模式视觉上有明显差异（如 Linear、Supabase），会提供在独立的 `themes/{brand}-dark/` 子目录中生成。

---

**最后更新**：2026-05-13

**维护者**： [@ricouii](https://x.com/ricouii)

**博客**：[rico'blog](https://ricoui.com)

**状态**：✅ 活跃开发
