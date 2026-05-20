# Cell-Skills 🧬

> Academic Writing & Submission Skills for Cell Press Journal Family

[![License: MIT](https://img.shields.io/badge/License-MIT-green.svg)](./LICENSE)
[![Skills](https://img.shields.io/badge/Skills-9-blue.svg)]()
[![Cell Press](https://img.shields.io/badge/Journals-Cell%20Press-red.svg)]()

---

## Introduction

**Cell-Skills** is a comprehensive AI-assisted academic writing skill pack designed specifically for the [Cell Press](https://www.cell.com/) journal family, covering Cell, Molecular Cell, Cell Stem Cell, Cell Reports, Cell Systems, Cell Chemical Biology, Cell Host & Microbe, Immunity, Neuron, Developmental Cell, Current Biology, and more.

This skill pack strictly adheres to Cell Press submission guidelines, including:
- **Summary** (not Abstract): ≤150 words, no citations
- **STAR Methods** (Structured, Transparent, Accessible Reporting)
- **Key Resources Table** (mandatory)
- **Graphical Abstract** (required for all Cell Press articles)
- **Highlights**: 3–4 bullet points, ≤85 characters each
- **eTOC Blurb**: ~50-word plain-language summary
- **Lead Contact** (not Corresponding Author)
- **Declaration of Interests**
- American English throughout
- Cell's distinctive narrative-driven, hypothesis-oriented writing style

---

## Skill Index

| # | Skill | Description |
|---|-------|-------------|
| 1 | [cell-figure](./cell-figure/) | Publication-quality figures for Cell Press |
| 2 | [cell-polishing](./cell-polishing/) | Academic prose polishing in Cell style |
| 3 | [cell-writing](./cell-writing/) | Manuscript section drafting in Cell format |
| 4 | [cell-citation](./cell-citation/) | Citation & reference management |
| 5 | [cell-data](./cell-data/) | Data availability & Key Resources Table |
| 6 | [cell-reader](./cell-reader/) | Bilingual full-paper Markdown reader |
| 7 | [cell-response](./cell-response/) | Reviewer response letters |
| 8 | [cell-paper2ppt](./cell-paper2ppt/) | Paper to presentation conversion |
| 9 | [cell-graphical-abstract](./cell-graphical-abstract/) | Graphical abstract design |

---

## Installation

### For Codex

```bash
git clone https://github.com/yanwenjie-666/skills.git cell-skills
cd cell-skills
# In Codex: Settings → Skills → Add Skill Directory → select the skill folder
```

### For Claude Code

```bash
# Option 1: Install via URL
claude skill add --url https://github.com/yanwenjie-666/skills/tree/main/cell-figure
claude skill add --url https://github.com/yanwenjie-666/skills/tree/main/cell-polishing
claude skill add --url https://github.com/yanwenjie-666/skills/tree/main/cell-writing
claude skill add --url https://github.com/yanwenjie-666/skills/tree/main/cell-citation
claude skill add --url https://github.com/yanwenjie-666/skills/tree/main/cell-data
claude skill add --url https://github.com/yanwenjie-666/skills/tree/main/cell-reader
claude skill add --url https://github.com/yanwenjie-666/skills/tree/main/cell-response
claude skill add --url https://github.com/yanwenjie-666/skills/tree/main/cell-paper2ppt
claude skill add --url https://github.com/yanwenjie-666/skills/tree/main/cell-graphical-abstract

# Option 2: Local installation
git clone https://github.com/yanwenjie-666/skills.git cell-skills
cd cell-skills
claude skill add --local ./cell-figure
claude skill add --local ./cell-polishing
# ... and so on
```

### Manual Installation

Copy the `SKILL.md` content from the desired skill folder into your AI tool's prompt.

---

## Target Journals

| Journal | IF (2025) | Focus |
|---------|-----------|-------|
| Cell | ~64 | Flagship, all life sciences |
| Molecular Cell | ~18 | Molecular biology |
| Cell Stem Cell | ~24 | Stem cell biology |
| Cell Reports | ~8 | Broad life sciences |
| Cell Systems | ~10 | Systems biology |
| Cell Chemical Biology | ~8 | Chemical biology |
| Cell Host & Microbe | ~21 | Microbiology & host interactions |
| Immunity | ~32 | Immunology |
| Neuron | ~17 | Neuroscience |
| Developmental Cell | ~12 | Developmental biology |
| Current Biology | ~10 | Broad biology |

---

## Key Differences: Cell Press vs Nature

| Feature | Cell Press | Nature |
|---------|-----------|--------|
| Abstract | Summary (≤150 words, no citations) | Abstract (≤150 words) |
| Methods | STAR Methods | Methods |
| Resources | Key Resources Table (mandatory) | None |
| Graphical Abstract | Required | Optional |
| Highlights | 3-4 bullets, ≤85 chars each | None |
| Plain Summary | eTOC Blurb (~50 words) | None |
| Corresponding Author | Lead Contact | Corresponding Author |
| Language | American English | British English |
| Writing Style | Narrative-driven, hypothesis-oriented | Concise, data-focused |
| Conflict Statement | Declaration of Interests | Competing Interests |
| Figure Width | ≤17.4 cm | Single 89mm / Double 183mm |

---

## Contributing

Issues and Pull Requests are welcome!

---

## License

[MIT License](./LICENSE)

---

## Acknowledgments

Inspired by [Yuan1z0825/nature-skills](https://github.com/Yuan1z0825/nature-skills).

This project is independently maintained and has no official affiliation with Cell Press / Elsevier.
