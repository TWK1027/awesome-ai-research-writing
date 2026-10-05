---
name: awesome-ai-research-writing
description: 学术论文写作 Prompt 模板库（来自 MSRA / Seed / SH AI Lab 研究员与北大、中科大、上交硕博同学一线实战打磨）。覆盖中英论文互译（LaTeX / Word）、学术表达润色、去 AI 味、缩写、扩写、逻辑检查、实验数据分析、论文架构图绘制、图表标题生成、实验绘图类型推荐、Reviewer 视角审稿等 17 个写作模板场景。当用户要求翻译、润色、修改、审查、压缩、扩写学术论文或论文片段（中文 / 英文、LaTeX / Word），或需要论文写作辅助（架构图、绘图建议、图表标题、审稿视角检查）时使用。
---

# AI 学术论文写作模板库

本 Skill 提供 17 个经过一线科研实战打磨的学术写作 Prompt 模板（另含 1 条模型选择建议），每个模板都是完整可用的 Role/Task/Constraints 结构，直接代入用户内容即可执行。

## 使用流程

1. 判断用户需求所属场景（见下方导航表）。
2. 读取对应 reference 文件，取用其中完整模板。
3. 将模板 `# Input` 部分替换为用户真实内容，严格按模板要求执行。
4. 按模板规定的输出格式交付（多数为 Part 1 目标文本 + Part 2 中文直译/日志 的结构）。

## 场景导航

| 用户需求 | 使用模板 | 文件 |
|---|---|---|
| 中文草稿 → 英文 LaTeX 论文片段 | 中转英-latex | references/translate.md |
| 英文 LaTeX → 流畅中文理解 | 英转中-latex | references/translate.md |
| 中文草稿 → 英文 Word 纯文本 | 中转英-word | references/translate.md |
| 中文口语/零散要点 → 规范中文论文段落 | 中转中-word | references/translate.md |
| 英文论文深度润色（LaTeX） | 表达润色（英文论文） | references/polish.md |
| 中文论文段落审视润色（克制修改） | 表达润色（中文论文） | references/polish.md |
| 去 AI 味（英文 LaTeX，含 AI 高频词表） | 去 AI 味（LaTeX 英文） | references/polish.md |
| 去 AI 味（中文 Word 文本） | 去 AI 味（Word 中文） | references/polish.md |
| 微幅缩减英文 LaTeX（约 5-15 词） | 缩写 | references/writing-assist.md |
| 微幅扩写英文 LaTeX（约 5-15 词） | 扩写 | references/writing-assist.md |
| 论文终稿一致性与逻辑红线审查 | 逻辑检查 | references/writing-assist.md |
| 实验数据 → 顶会 LaTeX 分析段落 | 实验分析 | references/writing-assist.md |
| 方法描述 → 论文架构图（中/英两版 prompt） | 论文架构图 | references/figures.md |
| 实验数据 → 推荐最佳绘图方案 | 实验绘图推荐 | references/figures.md |
| 中文描述 → 英文图标题 | 生成图的标题 | references/figures.md |
| 中文描述 → 英文表标题 | 生成表的标题 | references/figures.md |
| 整篇论文 Reviewer 视角审视 | 论文整体审视（Reviewer） | references/review.md |

## 通用原则

- 模板必须完整使用，不要删减任何约束项。
- LaTeX 场景：转义特殊字符（`%`、`_`、`&`），保留 `$` 数学公式，禁加粗斜体，拒绝列表。
- Word 场景：输出纯文本，严禁 Markdown 符号，使用全角中文标点（中文场景）。
- 去 AI 味场景以"宁缺毋滥"为阈值，高质量原文直接判定"检测通过"，不强行修改。
- 模板中 `[Input]` 为占位符，执行时替换为用户内容。

## 模型建议（原仓库调研结论）

语言润色类任务：预算充足推荐 Claude 系列（Claude Fable 5、opus 4.6 / 4.7）；性价比选 Gemini-3.7-flash；受限环境选 qwen3.8-max；不推荐 GPT 系列（语言表达较僵硬、性价比低）。以实际效果为准。
