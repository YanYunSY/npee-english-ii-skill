# Kaoyan English II Assistant Skill

面向考研英语二学习者的自适应英语学习 Skill。

当前聚焦：

- 长难句翻译
- 写作
- 词汇语境训练
- 语法与句法讲解
- 错误追踪
- 阶段性诊断

当前不包含完整阅读理解、完形填空和新题型专项。

## 为什么这个 Skill 不依赖“模型记忆”

Skill 把学习状态显式存放在 `learning-state.md` 中，而不是要求模型长期“记住”某个词是否出错过。

推荐工作流：

> 训练 → 批改 → 整理 → 更新 learning-state.md → 下次继续读取

这样即使更换聊天、模型或平台，也能继续使用同一份学习状态。

## 仓库结构

```text
kaoyan-english-2-skill/
├── README.md
├── SKILL.md
├── LICENSE
├── templates/
│   └── learning-state.md
├── references/
│   ├── error-taxonomy.md
│   ├── progression-algorithm.md
│   ├── sentence-selection.md
│   └── vocabulary-strategy.md
└── examples/
    ├── translation-training.md
    ├── translation-review.md
    ├── vocabulary-review.md
    ├── stage-summary.md
    ├── explain-sentence.md
    └── writing-review.md
```

## 核心机制

### 1. 显式学习状态

记录：

- 词 / 搭配 / 结构 / 写作问题
- 状态：`new / unstable / mastered`
- 错误次数
- 连续正确次数
- 最近错误 / 正确日期
- 下一次复现轮次

模板见 `templates/learning-state.md`。

### 2. 明确的间隔复现

错误项首次出现后，在未来 1–3 轮内复现；连续正确后逐渐拉长到 2–4 轮、4–7 轮；连续 3 次跨语境正确后才进入 `mastered`。

具体规则见 `references/progression-algorithm.md`。

### 3. 可操作的难度自适应

连续 2 轮至少 75% 句子无重大结构 / 逻辑错误，才允许小幅升级难度。

如果一轮超过一半句子出现重大结构或逻辑错误，则保持或降低难度。

## 使用

### ChatGPT / Claude Project

1. 将 `SKILL.md` 作为项目核心指令；
2. 将 `references/` 和 `examples/` 作为参考文件；
3. 从 `templates/learning-state.md` 创建自己的学习状态文件；
4. 每次“整理”后更新该文件；
5. 新对话开始时重新提供当前学习状态。

### Codex / 其他 Agent

将仓库整体作为 Skill / instruction source 使用。只要 Agent 能读取 `SKILL.md` 和当前的 `learning-state.md`，就可以延续训练状态。

## 常用指令

- `开始训练`
- `下一组`
- `继续`
- `讲一下这句`
- `整理`
- `给我写作题`
- `批改一下`

## 规则权威来源

为避免不同文件之间出现规则漂移：

- 错误标签与长期 Category 映射：`references/error-taxonomy.md`
- 状态转换、间隔复现、复现配额、难度调度：`references/progression-algorithm.md`
- 句子来源、主题与素材质量：`references/sentence-selection.md`
- 词汇训练方法：`references/vocabulary-strategy.md`
- 当前学习状态数据：`templates/learning-state.md`

其余文件只引用这些规则，不重复定义。

## 设计原则

- 不依赖隐式长期记忆；
- 默认不提前告诉长难句出处；
- 默认不在出题阶段给提示；
- 优先根据显式错误状态调整训练；
- 写作遵循 `准确 > 清晰 > 自然 > 复杂`；
- 主要用“重复错误是否减少”衡量效果。

## License

MIT
