# dashjim-skills

个人 Claude Code / Claude Agent Skills 集合。

## Skills

| Skill | 说明 |
|-------|------|
| [chinese-mcq-coach](./chinese-mcq-coach) | 高考/中考语文选择题解题教练：逐项文本比对、指认干扰项属于哪一类思维陷阱、给出答案和理由，并教会学生识别套路。 |

## 使用方式

将某个 skill 目录复制到你的 skills 目录即可：

```bash
cp -r chinese-mcq-coach ~/.claude/skills/
```

之后在 Claude Code 中会按 skill 的触发条件自动调用，或用对应的斜杠命令调用。
