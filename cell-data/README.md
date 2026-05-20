# cell-data

> Data and Code Availability / Key Resources Table for Cell Press | Cell Press 数据可用性声明与关键资源表

---

## 功能 | Features

- 🗂️ 自动生成 **Key Resources Table**（Cell Press 必填）
- 📋 撰写 **Data and Code Availability** 声明
- 🔍 验证 accession numbers 格式（GEO、PDB、PRIDE 等）
- ✅ RRID 格式检查与匹配
- 📦 RESOURCE AVAILABILITY 小节生成（Lead Contact / Materials / Data）
- 🔗 合规性自动审查（检查缺失项与格式错误）

---

## 适用期刊 | Target Journals

Cell、Molecular Cell、Cell Stem Cell、Cell Reports、Cell Systems、Cell Chemical Biology、Cell Host & Microbe、Immunity、Neuron、Developmental Cell、Current Biology 等所有 Cell Press 期刊。

---

## 快速使用 | Quick Start

```
请帮我生成 Key Resources Table，我的实验用了：
- RNA-seq 数据已存入 GEO (GSE200001)
- Anti-H3K4me3 抗体 (Abcam, ab8580)
- DESeq2 v1.40 进行差异分析
- 自写 Python 代码在 GitHub (https://github.com/mylab/analysis)
```

---

## Cell Press 核心要求 | Key Requirements

| 要求 | 说明 |
|------|------|
| Key Resources Table | STAR Methods 开头必填，按标准分类 |
| RRID | 所有抗体、细胞系必须提供 |
| Accession Numbers | 高通量数据必须存入公共数据库 |
| 代码公开 | 自定义代码需 GitHub + Zenodo DOI |
| Lead Contact | 必须声明资源获取联系人 |

---

## 输出结构 | Output Structure

1. **Key Resources Table** — Markdown 表格
2. **RESOURCE AVAILABILITY** — STAR Methods 标准三小节
3. **合规检查清单** — ✅/❌ 逐项报告

---

## 安装 | Installation

参见 [根目录 README](../README.md)。

---

## 许可 | License

[MIT](../LICENSE)
