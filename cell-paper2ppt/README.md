# cell-paper2ppt 📊

> Cell Press 论文转中文学术报告 PPT | Convert Cell Press Papers to Chinese Academic Presentations

---

## 功能简介 | Overview

**cell-paper2ppt** 将 Cell Press 期刊论文转换为结构化的中文学术演示文稿（PPT），适用于组会、读书会、学术会议和答辩等场景。

**cell-paper2ppt** converts Cell Press journal papers into structured Chinese-language academic presentations (PPT/PPTX), suitable for lab meetings, journal clubs, academic conferences, and thesis defenses.

---

## 核心特性 | Key Features

### 🎯 Cell Press 叙事风格保留
- 保持 Cell 独特的假说驱动叙事弧线
- Highlights 作为幻灯片结构骨架
- Graphical Abstract 作为开篇概览

### 🇨🇳 专业中文学术表达
- 符合中国学术界演示规范
- 标准生物医学术语（全国科技名词委标准）
- 首次出现中英对照，后续使用中文

### 📐 出版级设计规范
- Cell Press 红 (#C9302C) 配色体系
- 16:9 宽屏比例
- 思源黑体/微软雅黑 + Arial 字体方案
- 最小 14pt 字号保证可读性

### 🔄 多场景适配
- 组会版（含方法细节）
- 读书会版（含批判分析）
- 答辩版（关联自身研究）
- 会议版（精炼高效）

---

## 使用方法 | Usage

### 基本用法

```
请将这篇 Cell 论文转换为组会 PPT（标准版，约 20 张幻灯片）：
[粘贴论文内容或提供 PDF]
```

### 指定长度

```
将这篇论文做成简短版 PPT（12-15张），用于 10 分钟 journal club 展示。
```

### 指定输出格式

```
将这篇论文转为 PPT，输出为 python-pptx 代码，我需要可执行的脚本。
```

---

## 幻灯片结构 | Slide Architecture

| 序号 | 内容 | 幻灯片数 |
|------|------|----------|
| 1 | 标题页 | 1 |
| 2 | Graphical Abstract 概览 | 1 |
| 3 | 研究背景 | 1–3 |
| 4 | Highlights 导览 | 1 |
| 5 | 主体结果（按 Highlight 分组） | 6–16 |
| 6 | STAR Methods 概述 | 1–2 |
| 7 | 讨论与意义 | 1–2 |
| 8 | 总结与展望 | 1 |
| 9 | 参考文献 | 1 |

---

## 输出格式 | Output Formats

| 格式 | 说明 | 适用场景 |
|------|------|----------|
| Markdown Outline | 结构化文本 | 手动制作 PPT |
| Python-pptx Script | 可执行 Python 代码 | 自动生成 .pptx |
| PPTX File | 直接生成文件 | 即用型演示文稿 |

---

## 设计规范 | Design Specs

- **配色**: 白底 + Cell Red (#C9302C) + 深灰 (#333333)
- **中文字体**: 思源黑体 / 微软雅黑
- **英文字体**: Arial / Helvetica
- **标题**: 28–36pt
- **正文**: 18–24pt
- **最小字号**: 14pt
- **每页要点**: ≤6 条
- **图片占比**: ≤60% 幻灯片面积

---

## 与其他技能的关系 | Related Skills

| 技能 | 关系 |
|------|------|
| cell-reader | 提供论文全文解析 |
| cell-figure | 图表规范参考 |
| cell-graphical-abstract | GA 理解与展示 |
| cell-citation | 参考文献格式 |

---

## 示例 | Examples

### 输入
> 请将这篇发表在 Cell 上的单细胞测序论文转换为 20 分钟组会 PPT

### 输出（节选）
```
Slide 1: 标题页
- 论文标题（中英）
- 作者、期刊、年份

Slide 2: Graphical Abstract 概览
- [Graphical Abstract 图片]
- 一句话总结：本研究通过...揭示了...

Slide 3: 研究背景
- 领域现状
- 知识缺口
- 核心问题
```

---

## 安装 | Installation

```bash
# Claude Code
claude skill add --url https://github.com/yanwenjie-666/skills/tree/main/cell-paper2ppt

# 本地安装
claude skill add --local ./cell-paper2ppt
```

---

## 注意事项 | Notes

1. 图片版权：所有引用图片需标注来源
2. 术语规范：遵循全国科技名词审定委员会标准
3. 基因/蛋白命名：保持英文格式（基因斜体，蛋白正体）
4. 建议配合 cell-reader 使用以获得最佳解析效果

---

## License

[MIT](../LICENSE)
