# 安装指南 | Installation Guide

## 系统要求 | Requirements

- Git
- AI 编程工具（Codex / Claude Code / Cursor / 其他支持 skill 的工具）

---

## 安装方式 | Installation Methods

### 方式一：Codex

1. 克隆仓库：
```bash
git clone https://github.com/yanwenjie-666/skills.git cell-skills
cd cell-skills
```

2. 在 Codex 设置中添加技能：
   - 打开 Settings → Skills
   - 点击 "Add Skill Directory"
   - 选择需要的技能文件夹（如 `cell-writing/`）
   - Codex 会自动读取该目录下的 `SKILL.md`

3. 验证安装：
   - 在对话中询问："请用 Cell 格式帮我写一个 Summary"
   - AI 应当遵循 Cell Press 的 150 词限制、无引用等规范

### 方式二：Claude Code

```bash
# 逐个添加
claude skill add --url https://github.com/yanwenjie-666/skills/tree/main/cell-writing
claude skill add --url https://github.com/yanwenjie-666/skills/tree/main/cell-figure
claude skill add --url https://github.com/yanwenjie-666/skills/tree/main/cell-polishing

# 或本地批量添加
git clone https://github.com/yanwenjie-666/skills.git cell-skills
for skill in cell-skills/cell-*/; do
  claude skill add --local "$skill"
done
```

### 方式三：Cursor / Windsurf

1. 克隆仓库到本地
2. 在项目根目录创建 `.cursorrules` 或 `.windsurfrules` 文件
3. 将所需 SKILL.md 内容粘贴到规则文件中

### 方式四：手动添加到任意 AI 工具

将 `SKILL.md` 的内容复制到 AI 工具的系统提示词（System Prompt）中即可。

---

## 技能组合建议 | Recommended Combinations

### 写作全流程
- `cell-writing` + `cell-polishing` + `cell-citation` + `cell-data`

### 图表制作
- `cell-figure` + `cell-graphical-abstract`

### 投稿准备
- `cell-writing` + `cell-data` + `cell-graphical-abstract` + `cell-citation`

### 修稿回复
- `cell-response` + `cell-reader`

### 学术报告
- `cell-reader` + `cell-paper2ppt`

---

## 更新 | Updates

```bash
cd cell-skills
git pull origin main
```

---

## 故障排除 | Troubleshooting

**Q: AI 没有遵循 Cell Press 格式？**
A: 确认 SKILL.md 已正确加载。在对话开头明确提及目标期刊（如 "I'm submitting to Cell"）。

**Q: 如何选择正确的子刊？**
A: 在使用技能时指定目标期刊名称。不同子刊有细微差异（如 Cell Reports 的字数限制不同于 Cell）。

**Q: 如何与其他技能包配合？**
A: Cell-Skills 可与通用写作辅助工具并行使用。当指定 Cell Press 投稿时，本技能包的规则优先。
