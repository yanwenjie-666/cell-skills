# cell-reader

> Bilingual Full-Paper Markdown Reader for Cell Press Papers | Cell Press 论文双语全文 Markdown 阅读器

## 概述 | Overview

本技能将 Cell Press 期刊论文（PDF 或在线全文）解析为结构化的双语 Markdown 文档，保留 Cell Press 独特的文章结构（Summary、Highlights、eTOC Blurb、STAR Methods 等），并提供中英对照阅读版本。输出适合用于学术阅读、组会分享、文献管理和后续分析。

---

## 适用场景 | When to Use

- 将 Cell/Molecular Cell/Neuron 等论文转为结构化 Markdown
- 生成中英双语对照版本，方便非英语母语研究者阅读
- 快速提取论文关键信息（Highlights、Summary、Key Findings）
- 为组会或文献综述准备结构化笔记
- 作为 cell-writing、cell-response 等技能的输入预处理

---

## Cell Press 文章结构 | Article Structure

Cell Press 论文具有独特的结构，与 Nature/Science 不同：

### 正文结构（按顺序）

```
1. Title
2. Authors & Affiliations
3. Summary (≤150 words, no citations)
4. Highlights (3-4 bullets, ≤85 chars each)
5. eTOC Blurb (~50 words)
6. Graphical Abstract
7. Introduction
8. Results
   - 每个 Results 小节以描述性标题命名
   - 包含对图的引用 (Figure 1A)
9. Discussion
10. Limitations of the study
11. STAR Methods
    - RESOURCE AVAILABILITY
      - Lead contact
      - Materials availability
      - Data and code availability
    - EXPERIMENTAL MODEL AND STUDY PARTICIPANT DETAILS
    - METHOD DETAILS
    - QUANTIFICATION AND STATISTICAL ANALYSIS
    - KEY RESOURCES TABLE
12. Supplemental information
13. Acknowledgments
14. Author contributions
15. Declaration of interests
16. References
17. Figure legends
```

---

## 工作流程 | Workflow

### Step 1: 输入处理

接受以下输入格式：
- PDF 文件（通过 bohrium-pdf-parser 解析）
- DOI（通过 API 获取元数据）
- 论文 URL（Cell.com 链接）
- 用户粘贴的全文文本

### Step 2: 结构识别

自动识别 Cell Press 特有结构：
- 检测 "Summary" 而非 "Abstract"
- 识别 "Highlights" 块
- 识别 "eTOC Blurb"
- 识别 "STAR Methods" 及其子节
- 识别 "Key Resources Table"
- 识别 "Declaration of Interests"
- 识别 "Lead Contact"

### Step 3: 双语翻译

对每个章节执行：
- 保留英文原文
- 生成对应中文翻译
- 专业术语保留英文，括号注释中文含义
- 基因名、蛋白名、通路名保留原文
- 统计数据和 p-value 保留原文

翻译原则：
- 学术翻译风格，非机械直译
- 保持段落对应关系
- 专有名词首次出现时注释，后续保留英文
- 图表引用保留英文格式 (Figure 1A)

### Step 4: 输出格式化

生成结构化 Markdown 文件：

```markdown
# [论文标题]
# [论文标题中文翻译]

**DOI:** 10.1016/j.cell.2024.xx.xxx
**Journal:** Cell | **Volume:** 187 | **Pages:** 1-15
**Published:** 2024-01-01

---

## Authors | 作者

[Author List with affiliations]

---

## Summary | 摘要

> **English:**
> [Original Summary text]

> **中文：**
> [翻译后的摘要]

---

## Highlights | 亮点

| # | English | 中文 |
|---|---------|------|
| 1 | [Highlight 1] | [翻译] |
| 2 | [Highlight 2] | [翻译] |
| 3 | [Highlight 3] | [翻译] |

---

## eTOC Blurb | 通俗摘要

> **English:** [Original eTOC]
> **中文：** [翻译]

---

## Introduction | 引言

### English
[Original text]

### 中文
[Translation]

---

## Results | 结果

### [Result Section Title] | [中文标题]

#### English
[Original text]

#### 中文
[Translation]

[... 每个 Results 小节重复此结构 ...]

---

## Discussion | 讨论

[Same bilingual structure]

---

## Limitations of the Study | 研究局限性

[Same bilingual structure]

---

## STAR Methods | 方法

### Key Resources Table

[Rendered as Markdown table]

### Experimental Model and Study Participant Details

[Bilingual]

### Method Details

[Bilingual]

### Quantification and Statistical Analysis

[Bilingual]

---

## Key Findings Summary | 核心发现总结

[AI-generated concise summary of main findings, 5-8 bullet points]

---

## Glossary | 术语表

| Term | 中文 | Definition |
|------|------|-----------|
| [Key term 1] | [翻译] | [Brief definition] |
```

### Step 5: 质量检查

- 确认所有章节完整无遗漏
- 检查翻译质量和术语一致性
- 验证图表引用编号正确
- 确保 Key Resources Table 正确渲染

---

## 输出选项 | Output Options

用户可以选择：

### 完整版（默认）
- 全文双语对照
- 包含所有章节
- 适合精读和文献管理

### 精简版
- 仅 Summary + Highlights + Key Findings
- 快速了解论文核心内容
- 适合文献筛选

### 方法版
- 重点展开 STAR Methods
- 包含 Key Resources Table
- 适合实验复现

### 讨论版
- Introduction + Discussion + Limitations
- 适合理解论文学术语境和争议

---

## 特殊处理规则 | Special Rules

### 图表引用
- 保留原文引用格式：`(Figure 1A)`, `(Figure S1B)`
- 不翻译图表编号

### 基因与蛋白命名
- 基因名斜体：*TP53*, *BRCA1*
- 蛋白名正体：p53, BRCA1
- 中文翻译中保留英文原名

### 统计信息
- 完整保留：`(p < 0.001, n = 3, Student's t test)`
- 不翻译统计术语

### 引用格式
- 正文引用保留：`(Smith et al., 2020)`
- 不翻译参考文献

### 物种名
- 保留拉丁文斜体：*Mus musculus*, *Drosophila melanogaster*
- 可在首次出现时加中文注释

---

## 与其他 cell-skills 的协作 | Integration

- **cell-citation**: 提取参考文献列表供引用管理
- **cell-writing**: 提供结构模板参考
- **cell-response**: 理解原文作为审稿回复的基础
- **cell-paper2ppt**: 提供结构化内容用于 PPT 制作
- **cell-data**: 提取 Key Resources Table 信息

---

## 示例用法 | Example Usage

**用户**: 帮我读这篇 Cell 论文 [提供 PDF/DOI/URL]，生成双语版本

**助手**:
1. 解析论文结构
2. 识别 Cell Press 特有元素
3. 逐章节翻译
4. 生成结构化 Markdown
5. 输出 Key Findings Summary

---

## 质量标准 | Quality Standards

- 翻译准确率 > 95%
- 结构完整性：所有 Cell Press 必需章节均被识别
- 术语一致性：同一术语全文统一翻译
- 专有名词保留：基因/蛋白/通路名不意译
- 格式规范：Markdown 渲染无错误
- 输出文件可直接用于笔记软件（Obsidian、Notion）

---

## 错误处理 | Error Handling

| 情况 | 处理方式 |
|------|---------|
| PDF 解析失败 | 提示用户提供文本或尝试 DOI 获取 |
| 结构不完整 | 标注缺失部分，按可用内容输出 |
| 非 Cell Press 论文 | 提醒用户并按通用学术论文结构处理 |
| 图片/公式无法提取 | 标注 [Figure X: 描述] 占位 |
| 付费墙内容 | 提示用户提供全文 |
