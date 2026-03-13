# Antigravity 集成

将全部 61 个 Agency 智能体安装为 Antigravity 技能。
每个技能都会加上 `agency-` 前缀，避免和已有技能冲突。

## 安装

```bash
./scripts/install.sh --tool antigravity
```

该命令会把 `integrations/antigravity/` 中的文件复制到：
`~/.gemini/antigravity/skills/`

## 激活技能

在 Antigravity 中，用技能 slug 调用：

```
使用 agency-frontend-developer 技能审查这个组件。
```

可用 slug 统一遵循 `agency-<agent-name>`，例如：

- `agency-frontend-developer`
- `agency-backend-architect`
- `agency-reality-checker`
- `agency-growth-hacker`

## 重新生成

修改智能体后，执行：

```bash
./scripts/convert.sh --tool antigravity
```

## 文件格式

每个技能是一个 `SKILL.md`，包含 Antigravity 兼容 frontmatter：

```yaml
---
name: agency-frontend-developer
description: 专业前端开发智能体，擅长...
risk: low
source: community
date_added: '2026-03-08'
---
```
