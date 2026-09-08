[README.md](https://github.com/user-attachments/files/31939170/README.md)
# Paper Summary Skill

一个面向 Codex 的文献阅读 Skill：对单篇中英文期刊论文或学位论文进行三层深度解构，输出结构化的 Markdown 阅读报告。

## 功能

Paper Summary 以“跨领域研究顾问”的视角处理一篇文献，报告分为三层：

- **第一层：宏观概览与核心提炼**：主要内容、核心思路、创新点、具体算法或论证过程。
- **第二层：核心章节微观解剖**：定位技术核心章节、摘录代表性原文，并做逻辑拆解、术语释义与隐含假设分析。
- **第三层：批判性评价与前瞻**：从同行评议视角分析优越性、研究不足与未来方向。

支持中文与英文学术文献。文献为英文时，分析报告默认仍以中文输出。

## 安装

将 `paper-summary/` 文件夹放入本地 skill 目录：

```text
~/.codex/skills/paper-summary/
```

Windows 示例路径：

```text
C:\Users\<用户名>\.codex\skills\paper-summary\
```

也可以在 Codex 中调用该 skill 的安装流程从本仓库安装。

## 使用

新建一个 Codex 任务，上传论文 PDF 或粘贴论文文本，然后输入：

```text
请使用 $paper-summary 对这篇文献执行三层深度解构，并输出 Markdown 报告。
```

需要快速概览时，可要求只输出第一层与第三层。

## 目录结构

```text
my-coding-trial/
├── paper-summary/
│   ├── SKILL.md              # Skill 指令主体
│   ├── README.md             # Skill 内说明
│   └── agents/
│       └── openai.yaml       # UI 元数据
```

## 输出示例

生成的报告默认包含以下章节：

```markdown
# 文献深度解构报告

## 文献信息
## 第一层：宏观概览与核心提炼
## 第二层：核心章节微观解剖
## 第三层：批判性评价与前瞻
```

## 说明

- 扫描版 PDF 若无可提取文本层，需要先进行 OCR 或提供文字版内容。
- 超长文献会自动优先解析摘要、引言与结论部分。
- 报告由模型根据文献内容生成，供学习与科研辅助使用，引用文献结论时请核对原文。
