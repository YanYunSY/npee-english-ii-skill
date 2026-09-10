# 考研英语二长难句写作训练 Skill

## Skill 简介

面向 **考研英语二** 的 AI 学习 Skill。

支持：

- 长难句翻译
- 写作批改
- 词汇与语法训练
- 错误追踪
- 阶段性诊断

暂不包含完整阅读理解、完形填空和新题型专项。

如已有学习状态记录，直接上传并继续使用；如没有，可直接开始训练，后续通过 `整理` 生成学习状态文件。

---

## 安装

### 项目内安装

在需要使用 Skill 的项目目录中运行：

```bash
npx skills add YanYunSY/npee-english-ii-skill
```

安装后仅对当前项目生效。按提示选择使用的工具；首次运行需要安装 Node.js。

### 手动下载

1. 点击 **Code**
2. 选择 **Download ZIP**
3. 解压文件

这种方式不需要 Git。

---

## 在 ChatGPT 中使用

下载并解压后，新建 Project，并上传：

```text
SKILL.md
references/
examples/
templates/
```

如已有自己的学习状态文件，同时上传该文件。

随后输入：

```text
开始训练
```

完成训练后可输入：

```text
整理
```

用于生成或更新学习状态记录。

---

## 在 Claude 中使用

在 Claude Project 中添加：

```text
SKILL.md
references/
examples/
templates/
```

如已有学习状态文件，同时添加。

将 `SKILL.md` 作为主要训练规则使用，即可开始训练。

---

## 在 Codex 中使用

完成项目内安装后，新建对话并输入：

```text
$npee-english-ii-skill 开始训练
```

也可以直接输入“开始训练”，由 Codex 自动选择 Skill。

如已有学习状态文件，将其一并提供。

---

## 在 DeepSeek Harness 中使用

将整个 Skill 文件夹放到项目目录：

```text
.dsh/skills/npee-english-ii-skill/
```

重新开启会话后输入“开始训练”。如已有学习状态文件，同时提供该文件。

---

## 常用指令

```text
开始训练
下一组
继续
讲一下这句
整理
给我写作题
批改一下
```

---

## learning-state.md

用于记录：

- 词汇问题
- 语法问题
- 翻译错误
- 写作问题
- 学习进度

工作流程：

```text
训练 → 批改 → 整理 → 更新 learning-state.md → 继续训练
```

该文件用于在不同对话或平台间保留学习状态。

用户可选择在同一对话下不断练习更新learning-state.md；

也可选择保存learning-state.md并将其保存复制到其他对话或其他agent进行训练。

---

## 项目结构

```text
npee-english-ii-skill/
├── README.md
├── SKILL.md
├── templates/
├── references/
└── examples/
```

## License

MIT
