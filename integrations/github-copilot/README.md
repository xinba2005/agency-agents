# GitHub Copilot 集成

The Agency 与 GitHub Copilot 原生兼容。
无需转换，现有 `.md` + YAML frontmatter 可直接使用。

## 安装

```bash
# 安装全部智能体到 GitHub Copilot 目录
./scripts/install.sh --tool copilot

# 或手动复制某一类
cp engineering/*.md ~/.github/agents/
```

## 激活智能体

在任意 GitHub Copilot 会话中，按名称引用：

```
激活 Frontend Developer，并帮我实现一个 React 组件。
```

```
使用 Reality Checker 智能体，验证这个功能是否达到生产可用。
```

## 智能体目录

智能体按分组组织。完整清单见主 README。
