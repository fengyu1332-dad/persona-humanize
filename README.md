# persona-humanize

> 把「一看就是 AI 写的」文字，改写成「一看就是某个具体的人写的」文字。
> Turn "obviously AI-written" text into "clearly written by a specific human" text.

---

## 这是什么 / What is this?

**中文**
`persona-humanize` 是一个 WorkBuddy 技能，专门用来**消除文本里的「AI 味」、注入「真人感」**。

它和普通的「降 AI 率 / 降重」工具不一样：后者大多只做同义词替换，治标不治本。本技能会——

- **识别并清除 AI 痕迹**：逻辑连接词脚手架（首先/其次/综上所述）、互联网黑话（赋能/抓手/闭环/底层逻辑）、排比对仗强迫症、抽象名词堆砌，以及那种没有立场、没有情绪、永远「客观中立」的机器感；
- **结合作者背景画像重写**：根据年龄、学历、职业、籍贯、语言习惯、性格，推导出一个「人设」，让文字像这个具体的人在说话，而不是一篇中立文章在陈述；
- **中英文分别处理**：中文和英文的「AI 味」来源完全不同，技能用两套独立词库和地道表达规则，绝不中英混杂、不做翻译腔。

**English**
`persona-humanize` is a WorkBuddy skill that **removes the "AI flavor" from text and injects a genuine "human voice."**

Unlike generic "AI-detection-evasion" or paraphrasing tools that only swap synonyms, this skill:

- **Detects and strips AI tells**: filler transitions (*firstly / secondly / in conclusion*), corporate jargon (*leverage / foster / empower*), forced parallelism, abstract-noun piles, and that emotionless, always-neutral "machine tone";
- **Rewrites against an author persona**: it builds a *persona* from age, education, profession, regional background, language habits, and personality — so the text sounds like *this specific person* talking, not an article stating;
- **Treats Chinese and English separately**: the sources of "AI smell" differ completely across languages, so it uses two independent pattern libraries and native phrasing rules — no Chinglish, no translationese.

---

## 核心特性 / Features

- **五步流程**：解析输入 → AI 味诊断 → 作者画像 → 重写 → 校验交付
- **六维作者画像**：年龄 / 学历 / 职业 / 籍贯 / 语言特点 / 性格
- **中英文双词库**：各自的地道替换建议 + 逐条「改写自查清单」
- **两条红线**：忠于原意（只改说法不改内容）、语言一致（中文进中文出，英文进英文出）
- **主输出即成品**：直接给你改写后的全文，不绕弯、不堆过程

---

## 使用方式 / How to Use

**中文**
在 WorkBuddy 里直接说：
> 帮我把这段去 AI 味，作者是 28 岁上海互联网产品经理、口语化、爱吐槽

技能即自动触发，按画像重写。

**English**
In WorkBuddy, just say:
> Rewrite this to remove the AI flavor — author is a 28-year-old Shanghai PM, casual, loves roasting.

The skill triggers automatically and rewrites to match the persona.

---

## 文件结构 / Structure

```
persona-humanize/
├── SKILL.md                            # 技能主文件（流程与规则）
└── references/
    ├── ai-flavor-patterns-zh.md        # 中文 AI 味特征词库与替换建议
    ├── ai-flavor-patterns-en.md        # 英文 AI 味特征词库与替换建议
    └── persona-style-guide.md          # 作者背景 → 语言风格画像映射方法论
```

---

## 为什么需要它 / Why it matters

AI 写作的通病是「正确、完整、平衡、规范、对称」——这恰恰是「不像人写」的根源。真人写作是有观点、有情绪、有取舍、有具体细节、甚至有不完美的。本技能做的，就是把前者改造成后者，并且**让每一个作者都保留自己的声音**。

AI writing tends to be "correct, complete, balanced, formal, symmetric" — which is exactly why it doesn't feel human. Human writing is opinionated, emotional, selective, concrete, and occasionally imperfect. This skill turns the former into the latter — and **keeps each author's own voice intact**.

---

*WorkBuddy skill · 结合作者背景画像 + 中英文分治的去 AI 味改写工具*
