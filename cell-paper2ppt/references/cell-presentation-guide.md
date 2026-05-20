# Cell Press Paper Presentation Guide

## Reference: Converting Cell Press Papers to Academic Presentations

### Cell Press Paper Structure (for presentation mapping)

A typical Cell Press paper follows this structure, which maps directly to presentation slides:

```
Paper Section          →  Presentation Section
─────────────────────────────────────────────────
Graphical Abstract     →  Slide 2: Overview
Highlights (3-4)       →  Slide 4: Roadmap → Result group structure
Summary (≤150 words)   →  Background + Overview narration
Introduction           →  Slides 3: Background (1-3 slides)
Results                →  Slides 5+: Main Results (grouped by Highlight)
Discussion             →  Discussion & Significance slides
STAR Methods           →  Methods summary (1-2 slides)
Key Resources Table    →  Key tools/resources callout
```

### Cell Press Highlights Format

Highlights are the **structural spine** of the presentation:
- Exactly 3–4 bullet points
- Each ≤85 characters
- Written as complete findings (not questions)
- Each highlight = one story unit in the presentation

**Example Highlights** (from a Cell paper):
1. "Single-cell profiling reveals seven distinct tumor-infiltrating T cell states"
2. "Exhausted T cells show a continuous differentiation trajectory"
3. "TCF1+ progenitor cells fuel the anti-tumor immune response"
4. "Checkpoint blockade expands the progenitor-to-effector transition"

**Mapped to slides**:
- Highlight 1 → Slides 5-7 (scRNA-seq results, UMAP, marker genes)
- Highlight 2 → Slides 8-10 (trajectory analysis, pseudotime)
- Highlight 3 → Slides 11-13 (functional validation, in vivo)
- Highlight 4 → Slides 14-16 (therapeutic implications, patient data)

### STAR Methods Categories

STAR Methods use a structured format. Summarize for presentation as:

| STAR Category | Slide Content |
|---------------|---------------|
| KEY RESOURCES TABLE | Icon-based tool/resource summary |
| RESOURCE AVAILABILITY | Data access information |
| EXPERIMENTAL MODEL AND STUDY PARTICIPANT DETAILS | Sample/model overview |
| METHOD DETAILS | Flowchart of experimental pipeline |
| QUANTIFICATION AND STATISTICAL ANALYSIS | Statistical approach summary |

### Visual Design Reference

#### Cell Press Brand Colors
- **Primary Red**: #C9302C (Cell Press signature)
- **Dark Text**: #333333
- **Light Gray**: #F5F5F5 (backgrounds)
- **Accent Blue**: #2E86AB (methods/tools)
- **Accent Green**: #28A745 (positive results)

#### Recommended Slide Layouts

**Layout A: Figure-focused (60% image)**
```
┌─────────────────────────────────┐
│  标题 (Title)                    │
├──────────────────┬──────────────┤
│                  │ • 要点1       │
│   [Figure]       │ • 要点2       │
│                  │ • 要点3       │
├──────────────────┴──────────────┤
│  图注 / Caption                  │
└─────────────────────────────────┘
```

**Layout B: Data-focused (split)**
```
┌─────────────────────────────────┐
│  标题 (Title)                    │
├────────────────┬────────────────┤
│  [Figure A]    │  [Figure B]    │
├────────────────┴────────────────┤
│  • 关键发现 1                    │
│  • 关键发现 2                    │
└─────────────────────────────────┘
```

**Layout C: Text-focused (conclusions)**
```
┌─────────────────────────────────┐
│  标题 (Title)                    │
├─────────────────────────────────┤
│                                 │
│  ① 核心结论一                    │
│  ② 核心结论二                    │
│  ③ 核心结论三                    │
│                                 │
│         [Small icon/graphic]    │
└─────────────────────────────────┘
```

### Chinese Academic Terminology Reference

#### Common Biology Terms (中英对照)

| English | Chinese | Abbreviation |
|---------|---------|-------------|
| Transcription factor | 转录因子 | TF |
| Chromatin accessibility | 染色质可及性 | — |
| Single-cell RNA sequencing | 单细胞RNA测序 | scRNA-seq |
| Spatial transcriptomics | 空间转录组学 | ST |
| CRISPR screen | CRISPR筛选 | — |
| Lineage tracing | 谱系追踪 | — |
| Tumor microenvironment | 肿瘤微环境 | TME |
| Immune checkpoint | 免疫检查点 | — |
| Organoid | 类器官 | — |
| Epithelial-mesenchymal transition | 上皮-间充质转化 | EMT |
| Metabolic reprogramming | 代谢重编程 | — |
| Epigenetic modification | 表观遗传修饰 | — |
| Protein-protein interaction | 蛋白质-蛋白质相互作用 | PPI |
| Gene regulatory network | 基因调控网络 | GRN |
| Phase separation | 相分离 | — |

#### Presentation Transition Phrases (过渡语)

| Position | Chinese Phrase |
|----------|---------------|
| Opening | "今天我来分享一篇发表在 Cell 上的最新研究..." |
| Background→Results | "在此背景下，研究者提出了以下假说..." |
| Between results | "基于以上发现，研究者进一步探究了..." |
| Results→Discussion | "综合以上实验结果，我们可以得出..." |
| Closing | "总结来说，这项研究为我们理解...提供了新的视角" |

### Time Allocation Guide

| Version | Total Time | Slides | Per Slide |
|---------|-----------|--------|-----------|
| Short (组会快速) | 10 min | 12-15 | ~45 sec |
| Standard (读书会) | 20 min | 18-25 | ~50-60 sec |
| Detailed (答辩) | 30+ min | 30-40 | ~50-60 sec |

### Quality Checklist

- [ ] Graphical Abstract included as overview slide
- [ ] All 3-4 Highlights addressed in results section
- [ ] STAR Methods summarized visually
- [ ] Chinese terminology consistent throughout
- [ ] All figures attributed with source
- [ ] Speaker notes complete for every slide
- [ ] Transitions between sections smooth
- [ ] Font sizes ≥ 14pt throughout
- [ ] Color coding consistent with Cell Press palette
- [ ] Total slide count matches requested version
