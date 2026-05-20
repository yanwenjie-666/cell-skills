# cell-graphical-abstract 🎨

> Cell Press Graphical Abstract 设计技能 | Graphical Abstract Design for Cell Press Journals

⚠️ **Graphical Abstract 是所有 Cell Press 投稿的必需组件** | **Graphical Abstracts are REQUIRED for ALL Cell Press submissions**

---

## 功能简介 | Overview

**cell-graphical-abstract** 帮助你设计符合 Cell Press 严格规范的 Graphical Abstract（图形摘要），确保在一张图中传达论文的核心发现。

**cell-graphical-abstract** helps you design publication-ready Graphical Abstracts that comply with Cell Press's strict formatting guidelines, conveying your paper's main finding in a single compelling image.

---

## Cell Press 强制规范 | Mandatory Requirements

| 规范 Requirement | 标准 Standard |
|-----------------|---------------|
| 格式 Format | 正方形 1:1 比例 |
| 最低分辨率 Min Resolution | 1200 × 1200 像素 |
| 背景 Background | 白色优先 (#FFFFFF) |
| 最大面板数 Max Panels | 4 个（推荐单面板） |
| 最小字号 Min Font | 5pt（推荐 ≥8pt） |
| 风格 Style | 简洁、大胆、概念化 |
| 版权 Copyright | 不得包含受版权保护的材料 |
| 色彩 Colors | 与论文主图保持一致配色 |
| 核心要求 Core Rule | 不读论文也能理解核心发现 |

---

## 核心特性 | Key Features

### 🎯 3秒测试法则
- 第1秒：识别生物学系统/背景
- 第2秒：理解干预/方法
- 第3秒：明白关键发现/结论

### 🎨 专业配色方案
- Cell Press 经典配色（红灰绿蓝金）
- 色盲友好配色方案
- 极简双色方案

### 📐 标准化布局模板
- 线性流程型（左→右）
- 对比型（前/后、对照/处理）
- 中心发现型（汇聚式）
- 多面板型（≤4面板）

### 🔬 生物场景覆盖
- 基因调控/信号通路
- 药物靶向机制
- 单细胞异质性
- 结构生物学发现
- 进化比较研究

---

## 使用方法 | Usage

### 基本用法

```
请为我的 Cell 论文设计 Graphical Abstract。
核心发现：[描述你的主要发现]
研究系统：[细胞/动物/临床]
```

### 从论文提取

```
请根据以下论文的 Highlights 和 Summary 设计 Graphical Abstract：
[粘贴 Highlights 和 Summary]
```

### 指定输出格式

```
请生成 SVG 格式的 Graphical Abstract 代码，我需要在 Illustrator 中编辑。
```

---

## 输出格式 | Output Formats

| 格式 Format | 说明 Description | 适用场景 Use Case |
|-------------|-----------------|-------------------|
| SVG 代码 | 矢量图代码 | Illustrator/Inkscape 编辑 |
| Python 脚本 | matplotlib/PIL 代码 | 编程自动化生成 |
| 设计规格书 | 详细设计说明 | 交给设计师执行 |
| BioRender 指南 | 工具操作步骤 | BioRender 在线制作 |

---

## 设计流程 | Design Workflow

```
1. 提炼核心信息  →  将论文浓缩为一句话
       ↓
2. 选择视觉策略  →  机制/对比/工具/系统/治疗
       ↓
3. 确定布局模板  →  线性/对比/中心/多面板
       ↓
4. 选择配色方案  →  与主图一致 + 色盲友好
       ↓
5. 生成 GA      →  代码/规格书/指南
       ↓
6. 质量验证     →  Cell Press 清单逐项检查
```

---

## 常见错误 | Common Mistakes to Avoid

| ❌ 错误 | ✅ 正确做法 |
|---------|-----------|
| 太复杂，像补充图 | 简化为3个关键步骤 |
| 字太小看不清 | 所有文字 ≥5pt |
| 不是正方形 | 严格 1:1 比例 |
| 复制其他论文的图 | 原创设计所有元素 |
| 需要读标题才懂 | 图本身就讲完故事 |
| 超过4个面板 | 精简为1-2面板 |
| 红绿色区分 | 使用色盲友好方案 |

---

## 与其他技能的关系 | Related Skills

| 技能 Skill | 关系 Relationship |
|-----------|-------------------|
| cell-writing | GA 信息与 Summary/Highlights 对齐 |
| cell-figure | GA 与主图使用相同配色方案 |
| cell-paper2ppt | GA 作为 PPT 开篇概览幻灯片 |
| cell-reader | 从全文提取 GA 设计所需信息 |

---

## 示例 | Example

### 输入
> 论文核心发现：转录因子 FOXO3 通过调控自噬相关基因的表达，维持造血干细胞的静息状态，其功能丧失导致干细胞耗竭和白血病易感性增加。

### 输出（概念描述）
```
视觉叙事：左→右流程
- 左面板：正常造血干细胞（蓝色静息状态）+ FOXO3（绿色光环）
- 中面板：FOXO3 激活自噬基因转录（箭头+DNA元素）
- 右面板上：维持静息态（蓝色健康干细胞）
- 右面板下：FOXO3缺失→干细胞耗竭→白血病（红色异常细胞）

配色：蓝(正常)→绿(FOXO3)→红(疾病)
布局：1200×1200px, 白色背景, Arial 8pt标签
```

---

## 安装 | Installation

```bash
# Claude Code
claude skill add --url https://github.com/yanwenjie-666/skills/tree/main/cell-graphical-abstract

# 本地安装
claude skill add --local ./cell-graphical-abstract
```

---

## 参考资源 | References

- [Cell Press Graphical Abstract Guidelines](https://www.cell.com/pb/assets/raw/shared/figureguidelines/GA_guide.pdf)
- [Cell Press Figure Guidelines](https://www.cell.com/figure-guidelines)
- references/ 文件夹中包含详细设计规范参考

---

## License

[MIT](../LICENSE)
