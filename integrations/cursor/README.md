# Cursor 集成

把 61 个 Agency 智能体转换为 Cursor `.mdc` 规则文件。
规则是**项目级**的，请在目标项目根目录安装。

## 安装

```bash
# 在你的项目根目录执行
cd /your/project
/path/to/agency-agents/scripts/install.sh --tool cursor
```

该命令会在项目中生成 `.cursor/rules/<agent-slug>.mdc`。

## 激活规则

在 Cursor 提示词中引用智能体：

```
@frontend-developer 审查这个 React 组件的性能问题。
```

也可编辑 frontmatter，让规则始终生效：

```yaml
---
description: 专业前端开发智能体...
globs: "**/*.tsx,**/*.ts"
alwaysApply: true
---
```

## 重新生成

```bash
./scripts/convert.sh --tool cursor
```
