# Cell Press Key Resources Table — 完整指南

> 基于 Cell Press STAR Methods Guidelines (2024) 整理

## 概述

Key Resources Table (KRT) 是 Cell Press 所有期刊的强制要求。该表必须出现在 STAR Methods 的 **最开头**，列出所有关键实验材料和计算资源，确保研究的可重复性。

---

## 表格结构

### 标准列

| 列名 | 说明 |
|------|------|
| REAGENT or RESOURCE | 资源的描述性名称 |
| SOURCE | 来源（公司名/实验室/数据库） |
| IDENTIFIER | 唯一标识符（目录号、RRID、accession） |

### 标准分类（按此顺序排列）

1. **Antibodies**
2. **Bacterial and virus strains**
3. **Biological samples**
4. **Chemicals, peptides, and recombinant proteins**
5. **Critical commercial assays**
6. **Deposited data**
7. **Experimental models: Cell lines**
8. **Experimental models: Organisms/strains**
9. **Oligonucleotides**
10. **Recombinant DNA**
11. **Software and algorithms**
12. **Other**

---

## 各分类详细说明

### Antibodies

每个抗体单独一行，包含：
- 靶标蛋白名称
- 宿主物种和克隆类型（monoclonal/polyclonal）
- 克隆号（如适用）

**示例：**

| REAGENT or RESOURCE | SOURCE | IDENTIFIER |
|---------------------|--------|------------|
| Rabbit polyclonal anti-H3K4me3 | Abcam | Cat# ab8580; RRID:AB_306649 |
| Mouse monoclonal anti-β-Actin (clone AC-15) | Sigma-Aldrich | Cat# A1978; RRID:AB_476692 |
| Goat anti-rabbit IgG-HRP | Jackson ImmunoResearch | Cat# 111-035-144; RRID:AB_2307391 |

**注意：**
- RRID 是必须的；查询 https://antibodyregistry.org/
- 格式: `RRID:AB_XXXXXXX`
- 一抗和二抗都要列出

### Deposited Data

| REAGENT or RESOURCE | SOURCE | IDENTIFIER |
|---------------------|--------|------------|
| Raw and processed RNA-seq data | This paper | GEO: GSE123456 |
| Single-cell RNA-seq data | This paper | GEO: GSE123457 |
| Crystal structure of protein X | This paper | PDB: 7ABC |
| Cryo-EM map of complex Y | This paper | EMDB: EMD-12345 |
| Proteomics data | This paper | PRIDE: PXD012345 |
| Previously published ChIP-seq | Smith et al., 2020 | GEO: GSE100000 |

**注意：**
- 区分 "This paper" vs 已发表数据的来源
- Accession number 必须在文章发表前激活
- 超级系列用 GSE，单样本用 GSM

### Software and Algorithms

| REAGENT or RESOURCE | SOURCE | IDENTIFIER |
|---------------------|--------|------------|
| R v4.3.1 | R Project | https://www.r-project.org/ |
| DESeq2 v1.40.2 | Love et al., 2014 | RRID:SCR_015687 |
| Seurat v5.0 | Hao et al., 2024 | RRID:SCR_007322 |
| Custom Python scripts | This paper | https://github.com/lab/project; Zenodo: 10.5281/zenodo.xxxxx |
| ImageJ/Fiji v2.14 | Schindelin et al., 2012 | RRID:SCR_002285 |
| GraphPad Prism v10 | GraphPad Software | RRID:SCR_002798 |

**注意：**
- 每个软件需要精确版本号
- 商业软件也需要 RRID
- 自写代码必须提供 URL + DOI

### Experimental Models: Cell Lines

| REAGENT or RESOURCE | SOURCE | IDENTIFIER |
|---------------------|--------|------------|
| HEK293T | ATCC | Cat# CRL-3216; RRID:CVCL_0063 |
| HeLa | ATCC | Cat# CCL-2; RRID:CVCL_0030 |
| Patient-derived organoids | This paper | N/A |
| iPSC line WTC-11 | Coriell Institute | RRID:CVCL_Y803 |

**注意：**
- 细胞系 RRID 查询: https://web.expasy.org/cellosaurus/
- 格式: `RRID:CVCL_XXXX`
- 患者来源样本如无 RRID，需在方法中详细描述来源

### Oligonucleotides

| REAGENT or RESOURCE | SOURCE | IDENTIFIER |
|---------------------|--------|------------|
| sgRNA targeting TP53: GAGCGCTGCCCCCACCATGA | This paper | N/A |
| qPCR primer GAPDH-F: GAAGGTGAAGGTCGGAGTC | This paper | N/A |
| siRNA targeting BRCA1 | Dharmacon | Cat# L-003461-00 |

**注意：**
- 序列必须从 5' 到 3' 书写
- sgRNA 需标注靶基因
- 可引用补充表格（"See Table S1 for complete list"）

### Recombinant DNA

| REAGENT or RESOURCE | SOURCE | IDENTIFIER |
|---------------------|--------|------------|
| pLentiCRISPR v2 | Feng Zhang Lab | Addgene Cat# 52961; RRID:Addgene_52961 |
| pcDNA3.1-GFP-TP53 | This paper | N/A |
| pAAV-CAG-GCaMP6f | Bhatt Lab | Addgene Cat# 100836 |

---

## Data and Code Availability 标准模板

### 模板 A（含测序 + 代码）

```
Data and Code Availability

• All sequencing data have been deposited at GEO and are publicly available
  as of the date of publication. Accession numbers are listed in the key
  resources table.

• All original code has been deposited at GitHub and Zenodo and is publicly
  available as of the date of publication. DOIs are listed in the key
  resources table.

• Any additional information required to reanalyze the data reported in
  this paper is available from the lead contact upon request.
```

### 模板 B（含结构数据）

```
Data and Code Availability

• The cryo-EM maps have been deposited at the Electron Microscopy Data Bank
  (EMDB) and atomic coordinates have been deposited at the Protein Data Bank
  (PDB). Accession numbers are listed in the key resources table.

• This paper does not report original code.

• Any additional information required to reanalyze the data reported in
  this paper is available from the lead contact upon request.
```

### 模板 C（无高通量数据）

```
Data and Code Availability

• This paper does not report datasets that have been deposited in public
  repositories.

• This paper does not report original code.

• Any additional information required to reanalyze the data reported in
  this paper is available from the lead contact upon request.
```

---

## 合规检查清单

在提交前确认：

- [ ] KRT 位于 STAR Methods 最开头
- [ ] 所有抗体均有 RRID
- [ ] 所有细胞系均有 RRID (CVCL)
- [ ] 所有测序数据有 accession number
- [ ] 所有结构数据已存入 PDB/EMDB
- [ ] 自写代码有 GitHub URL 和 Zenodo DOI
- [ ] 所有软件标注了版本号
- [ ] Data Availability 三段式完整
- [ ] Lead Contact 信息正确
- [ ] 无 "TBD"/"XXX" 等占位符
- [ ] Accession numbers 已激活（非 private/embargo）
- [ ] 表格中无合并单元格（每个资源单独一行）

---

## 常见错误与修正

| 错误 | 修正 |
|------|------|
| 使用 "Corresponding Author" | 改为 "Lead Contact" |
| 缺少 RRID | 从 scicrunch.org 查找并补充 |
| 代码仅有 GitHub 无 DOI | 用 Zenodo 存档获取 DOI |
| 多个抗体写在一行 | 每个抗体单独一行 |
| 版本号缺失 | 补充具体版本 (如 "v1.40.2") |
| "Data available upon request" | Cell Press 不接受，必须公开存储 |
| 使用英式拼写 | 改为美式 (analysed → analyzed) |

---

## 参考文献

1. Cell Press STAR Methods Guidelines: https://www.cell.com/star-methods
2. RRID Portal: https://scicrunch.org/resources
3. Antibody Registry: https://antibodyregistry.org/
4. Cellosaurus: https://web.expasy.org/cellosaurus/
5. GEO Submission Guide: https://www.ncbi.nlm.nih.gov/geo/info/submission.html
6. Zenodo: https://zenodo.org/
