# cell-data

> Data and Code Availability / Key Resources Table — Cell Press 数据与代码可用性声明及资源表生成技能

## 概述 | Overview

本技能专门用于帮助研究者生成符合 Cell Press 投稿规范的 **Data and Code Availability** 声明、**Key Resources Table**（KRT）以及相关资源注册编号（accession numbers）。Cell Press 对数据共享和透明报告有严格要求，所有稿件必须在 STAR Methods 中包含 Key Resources Table，并在正文中提供完整的 Data and Code Availability 部分。

---

## 适用场景 | When to Use

- 生成或检查 Key Resources Table
- 撰写 Data and Code Availability 声明
- 整理 accession numbers（GEO、SRA、ENCODE、PDB、UniProt 等）
- 确认所有资源是否满足 Cell Press 的开放数据政策
- 检查代码仓库（GitHub、Zenodo、Figshare）是否符合规范
- 生成 STAR Methods 中 RESOURCE AVAILABILITY 小节

---

## Cell Press 数据政策核心要求 | Core Data Policy

### 1. Key Resources Table（必填）

所有 Cell Press 文章必须在 STAR Methods 开头包含 Key Resources Table，列出：

| REAGENT or RESOURCE | SOURCE | IDENTIFIER |
|---------------------|--------|------------|
| Antibodies | | |
| Bacterial and virus strains | | |
| Biological samples | | |
| Chemicals, peptides, and recombinant proteins | | |
| Critical commercial assays | | |
| Deposited data | | |
| Experimental models: Cell lines | | |
| Experimental models: Organisms/strains | | |
| Oligonucleotides | | |
| Recombinant DNA | | |
| Software and algorithms | | |
| Other | | |

### 2. Data and Code Availability 声明

必须包含以下要素：
- 原始数据和处理后数据的存放位置
- 所有软件的可获取性说明
- 任何其他再现研究所需的信息

### 3. Accession Numbers

- 所有高通量数据必须存入公共数据库
- 在文章接受前，accession numbers 必须激活（非 reviewer-only）
- 结构数据必须存入 PDB/EMDB
- 测序数据存入 GEO/SRA/ENA/DDBJ

### 4. 代码可用性

- 自定义代码必须公开（GitHub、Zenodo 等）
- 必须提供 DOI（推荐 Zenodo 存档）
- 如涉及商业限制，需说明替代获取途径

---

## 工作流程 | Workflow

### Step 1: 收集资源信息

从用户提供的稿件、实验记录或对话中提取：
- 所有抗体（来源、目录号、RRID）
- 细胞系（名称、来源、RRID）
- 实验动物品系
- 关键试剂和商业试剂盒
- 测序数据类型及存放库
- 使用的软件及版本
- 自写代码的仓库地址

### Step 2: 验证标识符

- 检查所有 RRID 格式（RRID:AB_XXXXXXX）
- 验证 GEO accession 格式（GSExxx、GSMxxx）
- 确认 PDB ID 格式（4 字符）
- 检查 Addgene 质粒编号
- 验证 DOI 格式

### Step 3: 生成 Key Resources Table

按 Cell Press 标准分类格式输出：

```markdown
## KEY RESOURCES TABLE

| REAGENT or RESOURCE | SOURCE | IDENTIFIER |
|---------------------|--------|------------|
| **Antibodies** | | |
| Anti-GFP (rabbit polyclonal) | Abcam | Cat# ab290; RRID:AB_303395 |
| **Deposited data** | | |
| Raw RNA-seq data | This paper | GEO: GSE123456 |
| **Software and algorithms** | | |
| DESeq2 v1.38.0 | Love et al., 2014 | https://bioconductor.org/packages/DESeq2 |
| Custom analysis code | This paper | https://github.com/xxx; DOI: 10.5281/zenodo.xxx |
```

### Step 4: 撰写 Data and Code Availability 声明

使用 Cell Press 标准三段式结构：

```markdown
## Data and Code Availability

- All sequencing data have been deposited at GEO and are publicly available
  as of the date of publication. Accession numbers are listed in the
  key resources table.

- All original code has been deposited at [GitHub/Zenodo] and is publicly
  available as of the date of publication. DOIs are listed in the key
  resources table.

- Any additional information required to reanalyze the data reported in
  this paper is available from the lead contact upon request.
```

### Step 5: 生成 RESOURCE AVAILABILITY 小节

在 STAR Methods 开头部分输出：

```markdown
## RESOURCE AVAILABILITY

### Lead contact
Further information and requests for resources and reagents should be
directed to and will be fulfilled by the lead contact, [Name] ([email]).

### Materials availability
[Plasmids/cell lines/etc.] generated in this study [are available from
the lead contact / have been deposited at Addgene (ID: xxxxx)].

### Data and code availability
[如 Step 4 生成的内容]
```

### Step 6: 合规性检查

自动检查以下项目并报告：
- [ ] Key Resources Table 是否包含所有必需分类
- [ ] 所有抗体是否有 RRID
- [ ] 所有测序数据是否有 accession number
- [ ] 代码是否有 DOI 或永久链接
- [ ] Lead contact 信息是否完整
- [ ] Materials availability 是否明确
- [ ] 所有 identifier 格式是否正确
- [ ] Accession numbers 是否已激活（非 embargo）

---

## 输出格式 | Output Format

最终输出包含三个部分，均使用 Markdown 格式：

1. **Key Resources Table** — 完整表格
2. **RESOURCE AVAILABILITY** — STAR Methods 部分
3. **合规检查报告** — 列出通过/未通过项

---

## 常见数据库与格式 | Common Databases & Formats

| 数据类型 | 推荐数据库 | ID 格式 |
|---------|-----------|---------|
| RNA-seq/ChIP-seq | GEO | GSExxxxxx |
| 原始测序 | SRA | SRPxxxxxx |
| 基因组变异 | dbSNP/ClinVar | rs/RCV |
| 蛋白结构 | PDB | 4 字符 (如 7BV2) |
| 冷冻电镜 | EMDB | EMD-xxxxx |
| 代谢组 | MetaboLights | MTBLS |
| 蛋白组 | PRIDE | PXDxxxxxx |
| 单细胞 | cellxgene/GEO | dataset ID |
| 流式数据 | FlowRepository | FR-FCM-xxxx |
| 质粒 | Addgene | 5-6 位数字 |
| 代码 | Zenodo + GitHub | DOI |

---

## RRID 格式规范 | RRID Formatting

```
Antibodies:     RRID:AB_XXXXXXX
Cell lines:     RRID:CVCL_XXXX
Organisms:      RRID:IMSR_XXX:XXXX
Software:       RRID:SCR_XXXXXX
Plasmids:       Addgene_XXXXX
```

查询网址: https://scicrunch.org/resources

---

## 注意事项 | Important Notes

1. **Cell Press 强制要求**：不提供 Key Resources Table 将导致格式退回
2. **RRID 必须精确**：错误 RRID 会被审稿人标记
3. **数据必须公开**：接受后即公开，不允许永久 embargo
4. **代码要可运行**：仅提供代码不够，需有文档和示例数据
5. **版本号很重要**：所有软件必须标注精确版本
6. **"N/A" 不能滥用**：如果某类资源确实未使用，可省略该行；但不能用 "N/A" 代替缺失信息
7. **每个资源一行**：不要合并多个抗体到一行

---

## 与其他 cell-skills 的协作 | Integration

- **cell-writing**: 生成 STAR Methods 时调用本技能填充 Key Resources Table
- **cell-polishing**: 润色时检查 Data Availability 声明的语言
- **cell-figure**: 图表中使用的软件信息需要同步到 KRT
- **cell-citation**: 引用的数据库工具需要在 KRT 中列出

---

## 示例对话 | Example Usage

**用户**: 我的文章用了 RNA-seq（存 GEO）、CRISPRi screen、3 个抗体，自己写了 Python 分析代码。帮我生成 Key Resources Table 和 Data Availability。

**助手**: 好的，我需要确认以下信息：
1. GEO accession number 是多少？
2. 三个抗体的名称、来源公司、目录号？
3. CRISPRi library 来源？
4. Python 代码的 GitHub 地址？是否已存档到 Zenodo？

[收集信息后生成完整表格和声明]

---

## 质量标准 | Quality Standards

- Key Resources Table 至少包含 3 个有效分类
- 所有 identifier 经过格式验证
- Data Availability 声明覆盖原始数据、处理数据、代码三方面
- Lead Contact 信息完整
- 无 placeholder（如 "XXX"、"TBD"）出现在最终输出中
- 美式英语（deposited, not "deposited"; analyzed, not "analysed"）
