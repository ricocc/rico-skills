# Rico Writer - Chinese Humanized Writing & De-AI Editor

Write, expand, polish, or diagnose Chinese text so it reads specific, clear, and opinionated. The skill preserves facts and the author's voice while removing the recognizable patterns of AI-generated prose.

---

## What Can This Skill Do?

### Core Features

1. **De-AI polishing** - Remove binary-contrast shells ("不是A，而是B"), pseudo-insight markers ("本质上""更重要的是"), lecturing openers ("记住这句话"), and unsupported hype ("必备神器")
2. **Fact-safe rewriting** - Names, numbers, dates, technical terms, test conditions, and sources are preserved. The author's stance and certainty level are never flattened or upgraded ("可能" never becomes "已经")
3. **Anthropomorphic verb cleanup** - "吃参考图" → "支持参考图输入", "给模型喂素材" → "把素材提供给模型", with context-aware judgment instead of a hard word ban
4. **Four working modes** - Write from notes (新写), expand (扩写), polish (润色), or diagnose with quoted examples (诊断)
5. **Non-intrusive structure** - The skill does not dictate openings, article structure, or endings; they follow the author's material

### Use Cases

- Polish a draft that reads like AI wrote it, while keeping your judgment intact
- Expand short notes into a full article without inventing experiences or data
- Turn a product review into an X/Twitter thread that keeps your stance
- Diagnose why a piece of writing feels off, with concrete rewrites

---

## Trigger Methods

**Natural language (typical requests):**

```
帮我把这段文章去 AI 味润色一下
把我的笔记扩写成一篇 800 字的公众号文章
这段文案帮我写得像人说话一点
把这篇评测改写成推文，保留我的判断
诊断一下这篇文章哪里有 AI 味
```

**Not triggered for:**

- Pure translation (把这段翻译成英文)
- Proofreading only (帮我检查错别字)
- Pure formatting (把这个 markdown 排版整理一下)

---

## How It Works

### Style Rules (the short version)

| Category | Rule | Example |
| -------- | ---- | ------- |
| Contrast shells | State the judgment directly | "去 AI 味不是改口语，而是保住判断" → "改稿时要保留作者的判断" |
| Anthropomorphic verbs | Say what the feature actually does | "吐 GIF" → "生成 GIF" |
| Punctuation | Double quotes "", no corner quotes 「」, no em-dashes in original prose | Use commas or sentence breaks |
| Comparisons | Claims need a scenario and evidence | No "效率翻倍""必备神器" without support |
| Structure | Does not impose opening/ending patterns or article templates | Openings and structure follow the author's material |

### Content Boundaries

- Never fabricate experiences, usage durations, quotes, data, or product features
- Decision thresholds ("先攒够 X 小时再买") need a basis; the skill will not invent them during expansion
- Others' opinions and original analyses get attribution; direct quotes keep their source
- First person is kept only when the source material is first-person ("我测了" requires an actual test)

### Delivery

By default the skill delivers only the finished text. Analysis or before/after comparisons are provided when you ask for them.

---

## Evaluation Results

Benchmarked with 3 tasks (de-AI polish, note expansion, review-to-tweet), with vs. without the skill, 31 objective assertions:

- **With skill: 100% pass rate** vs. without skill: 87.3%
- The skill prevented: fabricated decision thresholds, anthropomorphic verbs, em-dash reliance, and uninvited extra recommendations that the baseline runs produced
