# cell-citation 📚

> Cell Press 引用与参考文献管理 | Citation & Reference Management for Cell Press Journals

---

## 功能简介 | Overview

**cell-citation** 专门处理 Cell Press 期刊的引用格式化、参考文献列表编排和引用合规检查。支持 Cell 全部期刊家族的统一引用规范。

**cell-citation** handles citation formatting, reference list compilation, and citation compliance checking for all Cell Press journals. Supports the unified citation style across the entire Cell Press journal family.

---

## 核心特性 | Key Features

### 📝 文内引用格式化
- Author-Year 系统：(Smith et al., 2023)
- 自动处理 1/2/3+ 作者格式
- 多引用按时间排序，分号分隔
- 同作者同年份自动添加 a/b/c 后缀

### 📋 参考文献列表
- 字母顺序排列（首作者姓氏）
- 完整格式：作者. (年份). 标题. 期刊 卷, 页码.
- DOI 必须包含
- 支持预印本、网站、数据库等特殊类型

### ✅ 合规检查
- 验证引用-参考文献一致性
- 检查格式正确性
- 标记缺失 DOI
- 检测常见错误

---

## 使用方法 | Usage

### 格式化引用

```
请将以下参考文献格式化为 Cell Press 格式：
[粘贴参考文献列表]
```

### 检查引用合规性

```
请检查以下手稿的引用是否符合 Cell Press 规范：
[粘贴手稿片段]
```

### 添加引用

```
请为以下段落添加合适的引用（基于提供的参考文献）：
[粘贴段落 + 参考文献列表]
```

---

## Cell Press 引用格式速查 | Quick Reference

### 文内引用 (In-Text)

| 情况 | 格式 |
|------|------|
| 1 位作者 | (Smith, 2023) |
| 2 位作者 | (Smith and Jones, 2023) |
| 3+ 位作者 | (Smith et al., 2023) |
| 多篇引用 | (Smith, 2019; Jones et al., 2021) |
| 同作者同年 | (Smith et al., 2023a, 2023b) |
| 融入句中 | Smith et al. (2023) showed... |

### 参考文献列表 (Reference List)

```
期刊论文:
Author, A.B., Author, C.D., and Author, E.F. (2023). Article title.
Journal Name Volume, Pages. DOI.

预印本:
Author, A.B. (2023). Preprint title. bioRxiv. DOI. (Preprint).

书籍章节:
Author, A.B. (2023). Chapter title. In Book Title, E.D. Editor, ed.
(Publisher), pp. Pages.
```

---

## 安装 | Installation

```bash
# Claude Code
claude skill add --url https://github.com/yanwenjie-666/skills/tree/main/cell-citation

# 本地安装
claude skill add --local ./cell-citation
```

---

## 与其他技能的关系 | Related Skills

| 技能 | 关系 |
|------|------|
| cell-writing | 写作时正确插入引用 |
| cell-polishing | 润色时检查引用格式 |
| cell-response | 回复信中引用新文献 |
| cell-reader | 从论文中提取引用信息 |

---

## License

[MIT](../LICENSE)
