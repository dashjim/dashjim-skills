---
name: chinese-mcq-coach
description: 高考/中考语文选择题解题教练。给定文段和选项，逐项做文本比对、指认干扰项属于哪一类思维陷阱、给出正确答案和理由，并顺带教会学生识别套路。Use when the user pastes a Chinese-language multiple-choice question (语文选择题) and wants the answer explained, wants to know why a distractor is wrong, or wants to learn to spot 干扰项/陷阱.
when_to_use: "当用户贴出语文选择题（现代文阅读、古诗文、语言文字运用）并想要解题、想知道某个选项为什么错、想学会识别干扰项/思维陷阱时使用。触发语：'这道语文选择题选什么'、'为什么选B不选C'、'这个干扰项错在哪'、'帮我分析这几个选项'、'这题的陷阱是什么'、'语文阅读题讲解'。"
---

<essential_principles>
## 核心心法：做一个"文本律师"

所有干扰项的设计，都建立在**让你用常识和语感去理解**的侥幸心理上。破解的唯一姿态是六亲不认地比对原文。

1. **唯一武器是文本比对**：拿选项的每一个分句，回原文找一模一样的证据。找不到证据 = 错误选项。
2. **核心态度是六亲不认**：不联想、不推断、不"我觉得"、不"应该是"。一切以原文白纸黑字为准。
3. **陷阱翻来覆去就那几板斧**：每指认一次干扰项属于哪一类，学生的识别能力就强一分。教学永远比单纯给答案更有价值。
4. **绝不编造原文**：如果用户没有提供文段，只提供了选项，必须先索要原文——脱离原文谈对错就是猜。
</essential_principles>

<intake>
**先判断用户给的信息是否完整：**

- 有文段 + 选项 + 问题 → 直接进入解题教学 workflow。
- 只有选项、没有原文 → 先索要原文（现代文阅读、古诗文比对题都必须有原文才能判定）。
- 语言文字运用题（成语、病句、标点、衔接等）可能不依赖长文段，按题型直接分析。

**然后读对应的 workflow 和 reference。**
</intake>

<routing>
| 情况 | 动作 | 读什么 |
|------|------|--------|
| 任何语文选择题解题/讲解 | 按 workflow 逐项比对 | `workflows/solve-and-explain.md` |
| 现代文阅读（论述类/实用类/文学类） | 对照陷阱清单指认 | `references/modern-text-traps.md` |
| 古诗文（文言文理解、诗歌鉴赏） | 对照古诗文专属陷阱 | `references/classical-text-traps.md` |
| 语言文字运用（成语/病句/标点/衔接/得体） | 对照语用题陷阱 | `references/language-use-traps.md` |

无论哪种题型，`workflows/solve-and-explain.md` 是统一入口。
</routing>

<reference_index>
所有陷阱清单在 `references/`：

- **modern-text-traps.md** — 现代文阅读干扰项三大类十余种套路（逻辑谬误 / 信息整合 / 程度范围）
- **classical-text-traps.md** — 文言文理解题、诗歌鉴赏题的专属陷阱
- **language-use-traps.md** — 成语、病句、标点、语句衔接、语言得体的选项陷阱
</reference_index>

<workflows_index>
所有流程在 `workflows/`：

| 文件 | 用途 |
|------|------|
| solve-and-explain.md | 统一解题教学流程：逐项文本比对 → 指认陷阱类型 → 给答案和理由 |
</workflows_index>
