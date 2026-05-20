# cell-reader

> Bilingual Full-Paper Markdown Reader for Cell Press | Cell Press 论文双语全文 Markdown 阅读器

---

## 功能 | Features

- 📖 将 Cell Press 论文解析为结构化 Markdown
- 🌐 中英双语对照阅读
- 🏗️ 自动识别 Cell Press 独有结构（Summary、Highlights、eTOC、STAR Methods）
- 📊 Key Resources Table 格式化渲染
- 🔑 AI 生成 Key Findings Summary
- 📋 术语表自动生成
- 📱 输出兼容 Obsidian/Notion/Typora

---

## 适用期刊 | Target Journals

所有 Cell Press 期刊：Cell、Molecular Cell、Cell Stem Cell、Cell Reports、Cell Systems、Immunity、Neuron、Current Biology 等。

---

## 快速使用 | Quick Start

```
请帮我阅读这篇论文 [DOI/PDF/URL]，生成双语 Markdown 版本
```

**输出模式：**
- `完整版` — 全文双语（默认）
- `精简版` — Summary + Highlights + Key Findings
- `方法版` — 聚焦 STAR Methods
- `讨论版` — Introduction + Discussion + Limitations

---

## 输出示例 | Output Example

```markdown
# Single-cell atlas reveals...
# 单细胞图谱揭示...

## Summary | 摘要
> **English:** Here we present...
> **中文：** 本研究展示了...

## Highlights | 亮点
| # | English | 中文 |
|---|---------|------|
| 1 | Novel cell type identified | 发现新细胞类型 |
```

---

## 特殊处理 | Special Handling

- 基因名保留英文斜体（*TP53*）
- 统计数据不翻译
- 图表引用保留原格式
- 物种名保留拉丁文

---

## 安装 | Installation

参见 [根目录 README](../README.md)。

---

## 许可 | License

[MIT](../LICENSE)
