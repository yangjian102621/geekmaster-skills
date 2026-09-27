# geekmaster-skills

个人开源的 Agent Skills 仓库。这里收录我日常使用并持续打磨的可复用 AI 助手技能，全部遵循开放的 [Agent Skills](https://agentskills.io) 格式（`SKILL.md`），可安装到 Claude Code、ZCode、Codex CLI、Gemini CLI、Cursor 等支持该格式的工具中使用。

My personal collection of open-source Agent Skills for AI coding agents (Claude Code, ZCode, Codex CLI, Gemini CLI, Cursor, and any tool that supports the SKILL.md format).

## Skills 一览

| Skill | 简介 |
|---|---|
| [get-style-notes](./get-style-notes/) | 把网页链接 / 文章 / 长文本整理成「得到 GET 笔记」风格的结构化中文阅读笔记 |

## 安装某个 Skill

### 方式一：skills CLI（推荐）

```bash
npx skills add yangjian102621/geekmaster-skills@get-style-notes
```

### 方式二：手动安装

```bash
git clone https://github.com/yangjian102621/geekmaster-skills.git
cp -r geekmaster-skills/get-style-notes ~/.agents/skills/
```

不同工具的技能目录可能不同，按所用工具的文档放置。

## License

[MIT](./LICENSE)
