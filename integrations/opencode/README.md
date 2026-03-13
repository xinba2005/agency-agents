# OpenCode 集成

OpenCode 智能体是带 YAML frontmatter 的 `.md` 文件，存放在 `.opencode/agents/`。
转换器会把命名颜色转为十六进制颜色，并添加 `mode: subagent`，让智能体通过 `@agent-name` 按需调用。

## 安装

```bash
# 在你的项目根目录执行
cd /your/project
/path/to/agency-agents/scripts/install.sh --tool opencode
```

该命令会在项目目录创建 `.opencode/agents/<slug>.md`。

## 激活智能体

在 OpenCode 中，用 `@` 前缀调用子智能体：

```
@frontend-developer 帮我实现这个组件。
```

```
@reality-checker 审查这个 PR。
```

你也可以在 OpenCode 的智能体选择器中手动选择。

## 智能体文件格式

生成文件示例：

```yaml
---
name: Frontend Developer
description: 专业前端开发智能体，擅长现代 Web 技术...
mode: subagent
color: "#00FFFF"
---
```

- **mode: subagent**：按需调用，不占用主代理轮询列表
- **color**：十六进制颜色值（源文件命名颜色会自动转换）

## 项目级与全局安装

`.opencode/agents/` 为**项目级**。若要全局可用，请复制到 OpenCode 配置目录：

```bash
mkdir -p ~/.config/opencode/agents
cp integrations/opencode/agents/*.md ~/.config/opencode/agents/
```

## 重新生成

```bash
./scripts/convert.sh --tool opencode
```
