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

## 安装方法

### 下载 ZIP

1. 点击 **Code**
2. 选择 **Download ZIP**
3. 解压文件

无需安装 Git 或其他开发工具。

### Git

```bash
git clone https://github.com/YanYunSY/kaoyan-english-2-skill.git
```

---

## 在 ChatGPT 中使用

新建 Project，并上传：

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

新建 Project，并添加：

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

将仓库克隆或下载到本地：

```bash
git clone https://github.com/YanYunSY/kaoyan-english-2-skill.git
```

在 Codex 中打开项目目录，并让 Codex 读取：

```text
SKILL.md
references/
examples/
templates/
```

如已有学习状态文件，将其放入项目或一并提供。

---

## 在 DeepSeek Harness 中使用

将仓库下载或克隆到本地，并作为工作目录或指令来源加载。

确保 Harness 可以读取：

```text
SKILL.md
references/
examples/
templates/
```

如已有学习状态文件，同时提供该文件。

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

---

## 项目结构

```text
kaoyan-english-2-skill/
├── README.md
├── SKILL.md
├── templates/
├── references/
└── examples/
```

## License

MIT
