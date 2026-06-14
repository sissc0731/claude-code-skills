<p align="center">
  <img src="https://img.shields.io/github/stars/sissc0731/claude-code-skills?style=for-the-badge&color=f59e0b" alt="Stars">
  <img src="https://img.shields.io/github/license/sissc0731/claude-code-skills?style=for-the-badge&color=10b981" alt="License">
  <img src="https://img.shields.io/badge/Skills-12-blue?style=for-the-badge" alt="Skills">
</p>

<h1 align="center">🚀 Claude Code Skills</h1>
<h3 align="center">12 个开箱即用的 Claude Code 技能，提升开发效率</h3>

---

## 📦 安装

克隆到项目的 `.claude/skills/` 目录：

```bash
git clone https://github.com/sissc0731/claude-code-skills.git
cp -r claude-code-skills/.claude/skills/* .claude/skills/
cp claude-code-skills/CLAUDE.md .claude/CLAUDE.md
```

或者直接复制需要的单个 Skill 目录到 `.claude/skills/<skill-name>/SKILL.md`。

---

## 🛠 技能列表

| Skill | 触发词 | 说明 |
|-------|--------|------|
| 📝 **commit** | "生成 commit 信息"、"写个提交" | Conventional Commit 格式提交信息 |
| 🔍 **explain** | "解释这段代码"、"这段代码在干嘛" | 逐行分析代码逻辑 |
| 📖 **docstring** | "加注释"、"生成文档注释" | JSDoc/Python docstring/JavaDoc |
| 🧪 **test-gen** | "写测试"、"生成单元测试" | 自动生成测试用例 |
| ♻️ **refactor** | "重构"、"优化这段代码" | 代码坏味道分析和改进 |
| 🌐 **translate** | "翻译文档"、"中译英" | Markdown 翻译（中/英） |
| 🚀 **release-notes** | "生成 Release Notes" | 从 commit 历史生成发版说明 |
| 📋 **pr-desc** | "写 PR 描述"、"生成 PR 摘要" | 从 diff 生成 Pull Request 描述 |
| 📘 **readme-gen** | "生成 README"、"写项目文档" | 扫描项目生成 README |
| 🗄 **sql-format** | "格式化 SQL"、"优化查询" | SQL 格式化和优化建议 |
| 🔑 **env-gen** | "生成 .env 模板" | 扫描代码生成 .env.example |
| 📄 **changelog** | "更新 Changelog" | 从 git 历史生成 CHANGELOG |

---

## 📂 目录结构

```
.claude/skills/
├── commit/SKILL.md        # 提交信息生成
├── explain/SKILL.md       # 代码解释
├── docstring/SKILL.md     # 文档注释
├── test-gen/SKILL.md      # 测试生成
├── refactor/SKILL.md      # 代码重构
├── translate/SKILL.md     # 文档翻译
├── release-notes/SKILL.md # 发版说明
├── pr-desc/SKILL.md       # PR 描述
├── readme-gen/SKILL.md    # README 生成
├── sql-format/SKILL.md    # SQL 格式化
├── env-gen/SKILL.md       # 环境变量模板
└── changelog/SKILL.md     # 变更日志
```

---

## ⚡ 使用示例

```
# 生成提交信息
"帮我生成 commit 信息"

# 解释选中的代码
"解释一下这个函数"

# 生成测试
"给这个模块写单元测试"

# 重构代码
"重构一下这个文件"

# 翻译 README
"把 README 翻译成中文"
```

---

## 🤝 贡献

欢迎贡献新的 Skill！请参考 [CLAUDE.md](CLAUDE.md) 中的格式。

---

## ⭐ Star History

[![Star History Chart](https://api.star-history.com/svg?repos=sissc0731/claude-code-skills&type=Date)](https://star-history.com/#sissc0731/claude-code-skills&Date)

---

<p align="center">
  <sub>Made with ❤️ by <a href="https://github.com/sissc0731">sissc0731</a></sub>
</p>
