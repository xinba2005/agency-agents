# 🔌 集成说明

本目录包含 The Agency 针对多种智能体编程工具的集成产物与转换格式。

## 已支持工具

- **[Claude Code](#claude-code)**：原生 `.md` 智能体，可直接使用仓库内容
- **[GitHub Copilot](#github-copilot)**：原生 `.md` 智能体，可直接使用仓库内容
- **[Antigravity](#antigravity)**：每个智能体生成一个 `SKILL.md`
- **[Gemini CLI](#gemini-cli)**：扩展包 + `SKILL.md`
- **[OpenCode](#opencode)**：`.md` 智能体文件
- **[OpenClaw](#openclaw)**：`SOUL.md` + `AGENTS.md` + `IDENTITY.md` 工作区
- **[Cursor](#cursor)**：`.mdc` 规则文件
- **[Aider](#aider)**：`CONVENTIONS.md`
- **[Windsurf](#windsurf)**：`.windsurfrules`

## 快速安装

```bash
# 自动安装到系统中已检测到的工具
./scripts/install.sh

# 安装指定的全局工具
./scripts/install.sh --tool antigravity
./scripts/install.sh --tool copilot
./scripts/install.sh --tool openclaw
./scripts/install.sh --tool claude-code

# Gemini CLI 在全新 clone 后需要先生成集成文件
./scripts/convert.sh --tool gemini-cli
./scripts/install.sh --tool gemini-cli
```

对于 OpenCode、Cursor、Aider、Windsurf 这类项目级工具，请在目标项目根目录执行安装命令。

## 重新生成集成文件

当你新增或修改智能体后，执行：

```bash
./scripts/convert.sh
```

---

## Claude Code

The Agency 最初就是为 Claude Code 设计，原生可用，无需转换。

```bash
cp -r <category>/*.md ~/.claude/agents/
# 或一键安装：
./scripts/install.sh --tool claude-code
```

详见 [claude-code/README.md](claude-code/README.md)。

---

## GitHub Copilot

同样支持原生 `.md` + YAML frontmatter，无需转换。

```bash
./scripts/install.sh --tool copilot
```

详见 [github-copilot/README.md](github-copilot/README.md)。

---

## Antigravity

技能安装到 `~/.gemini/antigravity/skills/`，每个智能体会加 `agency-` 前缀避免冲突。

```bash
./scripts/install.sh --tool antigravity
```

详见 [antigravity/README.md](antigravity/README.md)。

---

## Gemini CLI

智能体会打包为 Gemini CLI 扩展，安装到 `~/.gemini/extensions/agency-agents/`。
首次克隆后请先执行转换。

```bash
./scripts/convert.sh --tool gemini-cli
./scripts/install.sh --tool gemini-cli
```

详见 [gemini-cli/README.md](gemini-cli/README.md)。

---

## OpenCode

每个智能体会生成项目级 `.md` 文件到 `.opencode/agents/`。

```bash
cd /your/project && /path/to/agency-agents/scripts/install.sh --tool opencode
```

详见 [opencode/README.md](opencode/README.md)。

---

## OpenClaw

每个智能体会变成包含 `SOUL.md`、`AGENTS.md`、`IDENTITY.md` 的工作区。

安装前先生成：

```bash
./scripts/convert.sh --tool openclaw
```

然后安装：

```bash
./scripts/install.sh --tool openclaw
```

详见 [openclaw/README.md](openclaw/README.md)。

---

## Cursor

每个智能体会生成一个 `.mdc` 规则文件。该规则是项目级的，请在项目根目录运行安装。

```bash
cd /your/project && /path/to/agency-agents/scripts/install.sh --tool cursor
```

详见 [cursor/README.md](cursor/README.md)。

---

## Aider

所有智能体会合并为单个 `CONVENTIONS.md`，Aider 在项目根目录会自动读取。

```bash
cd /your/project && /path/to/agency-agents/scripts/install.sh --tool aider
```

详见 [aider/README.md](aider/README.md)。

---

## Windsurf

所有智能体会合并为单个 `.windsurfrules` 文件。

```bash
cd /your/project && /path/to/agency-agents/scripts/install.sh --tool windsurf
```

详见 [windsurf/README.md](windsurf/README.md)。
