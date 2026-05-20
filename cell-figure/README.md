# cell-figure

> Cell Press 出版级图表制作技能 | Publication-Quality Figures for Cell Press

## 功能 | Features

本技能帮助你制作符合 Cell Press 期刊投稿标准的出版级图表，涵盖：

- 📐 严格的尺寸规范（最大宽度 17.4cm，分辨率 ≥300 DPI）
- 🔤 字体标准（Arial/Helvetica，≥6pt）
- 🎨 色盲友好配色方案
- 📊 统计标注规范（误差线、显著性标记、样本量）
- 🏷️ 面板标签格式（大写粗体 A, B, C...）
- 📝 Figure Legend 结构化撰写
- 🐍 Python/R 代码模板

This skill helps you create publication-quality figures that strictly conform to Cell Press journal submission standards.

## 适用场景 | Use Cases

- 从数据生成符合 Cell Press 规范的统计图表
- 排版多面板复合图（multi-panel composite figures）
- 撰写结构化的 Figure Legend
- 检查图表是否满足投稿要求（清单式验证）
- 微观图像处理（scale bar、magnification 标注）

## 使用方法 | Usage

在 AI 对话中说：
- "帮我按 Cell Press 标准制作一个图表"
- "Generate a Cell Press compliant multi-panel figure"
- "Check my figure against Cell Press submission requirements"
- "Write a figure legend for my Western blot panel"

## 文件结构 | File Structure

```
cell-figure/
├── SKILL.md              # 核心技能文件
├── README.md             # 本文件
└── references/
    └── figure-specs.md   # Cell Press 图表规范详细参考
```

## 关键规范速查 | Quick Reference

| 参数 | 规范 |
|------|------|
| 最大宽度 | 17.4 cm (全页) / 8.5 cm (单栏) |
| 分辨率 | ≥300 DPI (照片) / ≥600 DPI (线条) |
| 字体 | Arial 或 Helvetica |
| 最小字号 | 6 pt |
| 面板标签 | 大写粗体 (A, B, C...) |
| 文件格式 | PDF/EPS (矢量) 或 TIFF (位图) |
| 配色 | 色盲友好 |
