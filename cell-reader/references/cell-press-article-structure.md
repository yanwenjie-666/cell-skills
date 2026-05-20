# Cell Press Article Structure — Complete Reference

> 本文档详细描述 Cell Press 论文的完整结构，用于辅助 cell-reader 技能准确识别和解析各个章节。

---

## 文章类型 | Article Types

### Research Article (Article)
最主要的文章类型，全长研究论文。

### Resource
数据/工具/方法类资源论文，结构类似但 Results 偏重资源描述。

### Short Article / Report
Cell Reports 等期刊的短文，结构简化。

### Review / Perspective
综述类，无 STAR Methods。

---

## 完整结构详解 | Full Structure Breakdown

### 1. Title | 标题

- Cell 偏好有吸引力的、叙事性标题
- 通常不超过 120 个字符
- 避免缩写（除非极常见如 DNA、RNA）
- 常见模式：
  - "[机制/发现] [动词] [生物学功能]"
  - "A [Novel Thing] [reveals/enables/drives] [Biological Process]"

### 2. Author List | 作者列表

- 格式：First Name Middle Initial Last Name
- 并列第一作者标注数字上标
- 通讯作者标注星号 *
- Lead Contact 用特殊标记 (通常 #)

### 3. Affiliations | 单位

- 数字上标对应
- 包含完整地址

### 4. Contact Information | 联系信息

- Lead Contact 标注为 "Lead Contact"（非 Corresponding Author）
- 格式：*Correspondence: email@institution.edu

### 5. Summary | 摘要

**关键区别：Cell Press 使用 "Summary" 而非 "Abstract"**

规则：
- 最多 150 词
- 不含引用/参考文献
- 不使用缩写（除非标题中已定义）
- 单段，无分节
- 不含数字/统计
- 必须让非专业读者也能理解

结构模式：
```
[背景/问题 1-2句] → [方法概述 1句] → [主要发现 2-3句] → [意义/影响 1句]
```

### 6. Highlights | 亮点

**Cell Press 独有元素**

规则：
- 3 到 4 条（不能多也不能少）
- 每条 ≤85 个字符（含空格）
- 每条以动词或名词开头
- 不用句号结尾
- 不用缩写
- 纯文字，无特殊符号

示例：
```
• Single-cell atlas identifies 12 novel neuronal subtypes in human cortex
• CRISPR screen reveals TF network governing cell fate decisions
• Computational model predicts drug response with 90% accuracy
• In vivo validation confirms therapeutic potential of lead compound
```

### 7. eTOC Blurb | 通俗摘要

**Cell Press 独有元素** (electronic Table of Contents)

规则：
- 约 50 词（40-60 词范围）
- 通俗语言，面向广泛读者
- 第三人称（"Smith et al. show that..."）
- 一段话
- 解释 "为什么这篇文章重要"

格式模板：
```
[Author] et al. [discover/show/demonstrate/reveal] that [finding].
[Implication/significance in broader context].
```

### 8. Graphical Abstract | 图形摘要

**Cell Press 所有文章必须提供**

规格：
- 正方形，推荐 1200×1200 像素
- 最小 1000×1000 像素
- 白色背景
- 无多面板（单一视觉叙事）
- 从左到右或从上到下的信息流
- 字体 ≥12pt
- 不超过 4 种颜色
- 高清 300dpi

### 9. Introduction | 引言

Cell 风格特点：
- 叙事驱动，讲故事式
- 从广泛背景开始，逐步聚焦
- 明确提出假说或研究问题
- 最后一段概述 "Here, we..."
- 通常 4-6 段
- 引用丰富但有选择性

### 10. Results | 结果

Cell 风格特点：
- 每个小节有描述性标题（概括发现而非方法）
- 标题示例："A Novel Population of Stem Cells Drives Tissue Repair"（而非 "scRNA-seq Analysis"）
- 图文紧密结合
- 叙事流畅，不只是数据罗列
- 每段开头有过渡句连接上下文

### 11. Discussion | 讨论

- 开头总结核心发现
- 将结果放在领域背景中讨论
- 讨论机制和模型
- 承认局限性
- 提出未来方向
- 不重复 Results 的数据

### 12. Limitations of the Study | 研究局限性

**Cell Press 要求独立小节**
- 诚实列出技术和概念局限
- 2-4 点
- 建设性语气

### 13. STAR Methods

**Structured, Transparent, Accessible Reporting**

结构（严格按此顺序）：
```
STAR★METHODS

KEY RESOURCES TABLE
[完整的 Key Resources Table]

RESOURCE AVAILABILITY
  Lead contact
  Materials availability
  Data and code availability

EXPERIMENTAL MODEL AND STUDY PARTICIPANT DETAILS
  [实验模型详细信息]

METHOD DETAILS
  [详细方法描述]

QUANTIFICATION AND STATISTICAL ANALYSIS
  [统计方法，必须单独列出]
```

### 14. Supplemental Information | 补充信息

- 列出所有补充图/表
- 格式: "Figure S1. ..., related to Figure 1"

### 15. Acknowledgments | 致谢

- 基金支持
- 技术帮助
- 不含作者贡献

### 16. Author Contributions | 作者贡献

- CRediT 格式或叙述格式
- 每位作者的具体贡献

### 17. Declaration of Interests | 利益声明

**注意：不是 "Competing Interests" 或 "Conflict of Interest"**
- Cell Press 使用 "Declaration of Interests"
- 即使没有也要声明："The authors declare no competing interests."

### 18. References | 参考文献

- Cell Press 格式（非 Nature 格式）
- 正文引用：(Author et al., Year)
- 多引用：(Author1 et al., 2020; Author2 et al., 2021)
- 参考文献列表按字母顺序
- 格式: Author, A.B., Author, C.D., and Author, E.F. (Year). Title. Journal *Volume*, pages.

### 19. Figure Legends | 图注

- 位于参考文献之后
- 格式：Figure 1. [Title in bold]
- (A) 分面板描述
- 包含统计信息和样本量

---

## 识别关键词 | Detection Keywords

用于在 PDF/文本中识别各章节边界：

```python
SECTION_MARKERS = {
    "summary": ["Summary", "SUMMARY"],
    "highlights": ["Highlights", "HIGHLIGHTS", "In Brief"],
    "etoc": ["eTOC", "eTOC Blurb", "In Brief"],
    "graphical_abstract": ["Graphical Abstract", "GRAPHICAL ABSTRACT"],
    "introduction": ["Introduction", "INTRODUCTION"],
    "results": ["Results", "RESULTS"],
    "discussion": ["Discussion", "DISCUSSION"],
    "limitations": ["Limitations of the Study", "Limitations of the study",
                     "LIMITATIONS OF THE STUDY"],
    "star_methods": ["STAR Methods", "STAR★METHODS", "STAR*METHODS",
                     "Method Details", "EXPERIMENTAL PROCEDURES"],
    "key_resources": ["KEY RESOURCES TABLE", "Key Resources Table",
                      "Key resources table"],
    "acknowledgments": ["Acknowledgments", "ACKNOWLEDGMENTS"],
    "author_contributions": ["Author Contributions", "AUTHOR CONTRIBUTIONS",
                             "Author contributions"],
    "declaration": ["Declaration of Interests", "Declaration of interests",
                    "DECLARATION OF INTERESTS"],
    "references": ["References", "REFERENCES"],
    "figure_legends": ["Figure Legends", "FIGURE LEGENDS",
                       "Figure legends"],
    "supplemental": ["Supplemental Information", "SUPPLEMENTAL INFORMATION",
                     "Supplemental information"],
}
```

---

## 翻译术语标准化 | Translation Glossary

| English | 中文标准翻译 |
|---------|-------------|
| Summary | 摘要 |
| Highlights | 亮点/研究亮点 |
| eTOC Blurb | 通俗摘要 |
| Graphical Abstract | 图形摘要 |
| STAR Methods | STAR方法 |
| Key Resources Table | 关键资源表 |
| Lead Contact | 通讯联系人 |
| Declaration of Interests | 利益声明 |
| QUANTIFICATION AND STATISTICAL ANALYSIS | 定量与统计分析 |
| Limitations of the Study | 研究局限性 |
| Author Contributions | 作者贡献 |
| Supplemental Information | 补充信息 |
