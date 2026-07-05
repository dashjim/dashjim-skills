# dashjim-skills

个人 Claude Code / Claude Agent Skills 集合，附中文高考语文教研语料与研究成果。

## 目录结构

```
dashjim-skills/
├── skills/                          # Claude Agent Skills
│   ├── chinese-mcq-coach/           # 语文【选择题】解题教练
│   └── chinese-subjective-coach/    # 语文【主观题】答题教练（配套）
├── exam-corpus/                     # 上海各区高三语文模拟卷语料（阅读题+答案）
│   ├── shanghai-2024-yuwen-gaosan/  # 2024届 一模+二模（16区，-阅读.md）
│   ├── shanghai-2025-yuwen-yimo/    # 2025届 一模（含6份-原卷.md带官方评分说明）
│   ├── shanghai-2025-yuwen-ermo/    # 2025届 二模
│   ├── shanghai-2026-yuwen-yimo/    # 2026届 一模
│   └── shanghai-2026-yuwen-ermo/    # 2026届 二模（10区全为-原卷.md带官方评分说明）
└── research/
    └── 语文主观题研究/               # 从语料到 skill 的教研研究成果
```

## Skills

| Skill | 说明 |
|-------|------|
| [chinese-mcq-coach](./skills/chinese-mcq-coach) | 语文**选择题**解题教练：逐项文本比对、指认干扰项属于哪类思维陷阱、给答案和理由。 |
| [chinese-subjective-coach](./skills/chinese-subjective-coach) | 语文**主观题**答题教练：判文体→定题型→按官方评分说明反推的"答案必含要素"逐点组织答案，并能给学生答案按采分点打分。经双盲质检 42/42 验证。 |

两个技能配套：选择题教"排除干扰项"，主观题教"命中采分点"，共同内核都是**六亲不认地比对原文 / 对齐官方采分**。

## 语料与研究

- `exam-corpus/` — 上海 16 区 2024–2026 届高三语文一模/二模阅读题。其中 `-原卷.md` 为**题目原文 + 官方完整答案（含评分说明，逐字照录）**，`-阅读.md` 为答案要点精简版。
- `research/语文主观题研究/` — 以 18 份含官方评分说明的原卷为实证，反推出**分文体（论述/文学/诗歌/文言记叙/文言论说）的答题模板库**，即 `chinese-subjective-coach` 的知识来源。研究方法与关键决策见该目录下 `CLAUDE.md`。

## 使用方式

将某个 skill 目录复制到你的 skills 目录即可：

```bash
cp -r skills/chinese-subjective-coach ~/.claude/skills/
```

之后在 Claude Code 中会按 skill 的触发条件自动调用。

## 声明

语料整理自公开网络（21世纪教育网等可免费查看全文的来源），仅供个人教研学习使用。
