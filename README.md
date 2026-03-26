<p align="center">
  <img src="docs/images/logo.png" alt="2sigma" width="120"/>
</p>

<h1 align="center">2sigma</h1>

<p align="center">
  <b>Your AI private tutor. Learn anything 10x faster.</b><br/>
  <b>AI 私教 · 十倍速进入任何领域</b>
</p>

<p align="center">
  <a href="#english">English</a> · <a href="#中文">中文</a> · <a href="#install">Install</a>
</p>

---

> **1984**, educational psychologist Benjamin Bloom published a finding that shook the academic world: a student who receives **1-on-1 tutoring** with **mastery-based progression** outperforms **98% of students** in traditional classrooms. He called it the **2-sigma problem** — because the effect was two standard deviations above the mean.
>
> The catch? One tutor per student doesn't scale. For decades, this remained an unsolved problem. **Until now.**

> **1984年**，教育心理学家布鲁姆发现：接受**一对一辅导**和**掌握式学习**的学生，能超过传统课堂中 **98%** 的学生。他称之为 **2-sigma 问题**——效果整整高出两个标准差。但一个学生配一个导师，成本太高了。这个问题悬而未决了几十年。**直到现在。**

---

<a name="english"></a>

## What is this?

**2sigma** is a skill for [Claude Code](https://docs.anthropic.com/en/docs/claude-code), [Codex](https://openai.com/index/codex/), and other AI agents. It turns your AI into a **Bloom-style private tutor** that:

- **Asks YOU questions** instead of waiting for you to ask — because when you're learning something new, you don't know what you don't know
- **Writes structured learning documents** to your local files — not trapped in a chat window that expires
- **Tracks your progress** with a knowledge tree — pick up where you left off, anytime
- **Adapts to your level** — struggling? it slows down. breezing through? it challenges you

### Why not just chat with AI?

Because chatting with AI gets the learning loop **backwards**.

|  | Traditional AI Chat | 2sigma |
|---|---|---|
| Who drives? | You ask, AI answers | **AI tutors, you respond** |
| Context | Chat dies after long conversations | **Files persist forever** |
| Progress | None. Start over every session. | **Knowledge tree + mastery tracking** |
| Difficulty | One-size-fits-all | **Adapts to YOUR comprehension** |
| Science | None | **Bloom's 2-sigma method** |

<p align="center">
  <img src="docs/images/comparison.png" alt="Traditional AI chat vs 2sigma" width="700"/>
</p>

## How it works

<p align="center">
  <img src="docs/images/learning-loop.png" alt="2sigma learning loop" width="500"/>
</p>

1. You say: **"Help me learn quantum computing"**
2. AI asks about your background and level
3. Generates `01.md` — written like a friend explaining, not a textbook lecturing
4. You answer questions at the end (designed to test *understanding*, not *memory*)
5. AI evaluates your overall comprehension, not just right/wrong
6. Generates `02.md` — adapted based on your answers
7. Repeat until mastery

## 6 Learning Modes

<p align="center">
  <img src="docs/images/six-modes.png" alt="Six learning modes" width="700"/>
</p>

| Mode | Trigger | What it does |
|------|---------|-------------|
| **Paper Reading** | "Help me read this paper" + PDF/DOI | Breaks down a research paper into digestible pieces |
| **Concept Learning** | "What is X?" / "Explain X" | Takes one concept from zero to mastery |
| **Domain Introduction** | "I want to learn about X field" | Builds a complete knowledge map with learning roadmap |
| **Tech Stack** | "How do I learn X framework?" | Understands a tool's philosophy and core usage |
| **Code Repo Reading** | Provide a GitHub URL or local path | Reads a codebase like reading a paper — architecture first, details on demand |
| **Exam Review** | "Quiz me on this book" + PDF/textbook | Progressive testing with weak-area drilling — feed it a whole book |

## The secret sauce

Most AI "tutors" ask you to recite what you just read. That's useless.

2sigma designs questions as a **confidence sandwich**:

1. **Accessible** — You can answer this. Builds confidence. But you must rephrase, not copy.
2. **Application** — Apply the concept to a scenario the document never mentioned.
3. **Challenge** (optional) — Synthesize, evaluate, or argue. Only when you're ready.

The AI evaluates your **overall comprehension**, not individual answers. Small mistakes get corrected and you move on. Fundamental misunderstandings trigger a re-teach from a different angle.

<p align="center">
  <img src="docs/images/progress-tree.png" alt="Knowledge tree" width="500"/>
</p>

<a name="install"></a>

## Install

### Claude Code

Open Claude Code and say:

> **"Help me install the 2sigma skill from `https://github.com/chenly255/2sigma`. Clone it to `~/.claude/skills/2sigma/`."**

### Codex

Open Codex and say:

> **"Clone `https://github.com/chenly255/2sigma` to `~/.codex/skills/2sigma/`."**

### Other agents (Trae, etc.)

Copy `SKILL.md` and `references/` to wherever your agent reads skill files. No platform-specific tools — works with any agent that can read/write files.

### PDF support (optional)

To feed PDFs (papers or textbooks), install [uv](https://docs.astral.sh/uv/):

```bash
curl -LsSf https://astral.sh/uv/install.sh | sh
```

First PDF conversion auto-downloads models. Subsequent runs use cache.

## First time setup

On first use, the skill asks a few questions to personalize your experience:

- **Language** — responds in whatever language you prefer
- **Your background** — so it picks analogies that click for you
- **Document length** — short (600w), medium (1000w), or long (1800w)
- **Paper source** — Zotero, PDF files, or online search

Saved once. Never asked again unless you want to change them.

---

<a name="中文"></a>

## 这是什么？

你有没有这种经历——想进入一个全新领域，入门书太浅看了没用，专业书又啃不动，每看一句话恨不得查半天？

**问题不在于你不够聪明。** 人类的大脑天生需要定制化学习——你需要有人根据你的理解程度，一步步带你走。这就是为什么一对一家教永远比大班课效果好。

但家教太贵了。一小时几百块，学一个新领域可能需要几十个小时。

**2sigma 把你的 AI 变成一个免费的一对一私教。** 不是那种你问它答的聊天机器人——而是它主动给你出题、判断你的理解程度、根据你的反馈调整教学节奏的 **2-sigma 级别的 AI 导师**。

### 为什么不能直接跟 AI 聊天学习？

因为聊天学习把学习流程**搞反了**。

当你接触一个完全陌生的领域时，核心困扰是：**你不知道你不知道什么**。你没法提出好问题，因为你还没有足够的知识储备来提问。

一对一辅导之所以有效，就是因为它让**导师主动提问**，你只需要想办法回答。2sigma 就是这个逻辑。

而且，普通 AI 聊天有一个致命问题：**对话框会过期**。你聊了两个小时学了一半，上下文满了，开新对话——你得从头给 AI 解释你学到哪了。

2sigma 把所有学习内容写成文件，存在你电脑上。**学习进度永远不会丢失。** 下次打开，知识树告诉你学到哪了，直接继续。

### 怎么用？

打开 Claude Code（或 Codex），直接说：

- "帮我学习量子计算"
- "帮我读这篇论文" + 丢一个 PDF
- "帮我复习这本书，准备考试"
- "帮我看看这个 GitHub 项目在干什么"

AI 会：
1. 问你的背景和了解程度
2. 生成第一篇学习文档（像朋友聊天一样讲解，不是教科书）
3. 文档末尾有针对性的提问——不是让你背诵，而是测试你真的理解了
4. 你回答后，AI 评估理解程度，决定继续推进还是换个角度再讲一遍

**这就是布鲁姆的 2-sigma 方法：一对一辅导 + 掌握式学习。**

### 安装

打开 Claude Code，说一句话：

> **"帮我把 `https://github.com/chenly255/2sigma` 克隆到 `~/.claude/skills/2sigma/`"**

就这样。

PDF 功能需要额外装 [uv](https://docs.astral.sh/uv/)：`curl -LsSf https://astral.sh/uv/install.sh | sh`

---

## Extending / 扩展

Want to add a new learning mode? See [references/extending.md](references/extending.md). Define trigger words, document sequence, and style rules. The mastery loop handles the rest.

想添加新的学习模式？查看 [references/extending.md](references/extending.md)。

## Project Structure

```
2sigma/
├── SKILL.md                  ← Core workflow (platform-agnostic)
├── references/
│   ├── onboarding.md         ← First-time user setup
│   ├── learning-modes.md     ← 6 mode specifications
│   ├── grading.md            ← Question design & evaluation
│   ├── writing-style.md      ← Tone, analogies, terminology
│   └── extending.md          ← How to add new modes
└── scripts/
    └── pdf_to_sections.py    ← PDF → per-section markdown (uv + Marker)
```

## Author

**Liying Chen** — PhD student @ [Sun Yat-sen University](https://www.sysu.edu.cn/) & [Guangzhou National Laboratory](https://www.gzlab.ac.cn/)

Advised by [Prof. Luyi Tian](https://scholar.google.com.au/citations?user=6G0fn6QAAAAJ&hl=en)

## License

MIT

---

<p align="center">
  <b>Stop satisfying AI's ego. Let AI serve yours.</b><br/>
  <b>别再"问" AI 了。让 AI 来"教"你。</b>
</p>
