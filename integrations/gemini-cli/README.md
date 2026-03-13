# Gemini CLI 集成

将 61 个 Agency 智能体打包为 Gemini CLI 扩展。
扩展安装路径：`~/.gemini/extensions/agency-agents/`。

## 安装

```bash
# 先生成 Gemini CLI 集成文件
./scripts/convert.sh --tool gemini-cli

# 再安装扩展
./scripts/install.sh --tool gemini-cli
```

## 激活技能

在 Gemini CLI 中按名称引用智能体：

```
使用 frontend-developer 技能帮我实现这个 UI。
```

## 扩展结构

```
~/.gemini/extensions/agency-agents/
  gemini-extension.json
  skills/
    frontend-developer/SKILL.md
    backend-architect/SKILL.md
    reality-checker/SKILL.md
    ...
```

## 重新生成

```bash
./scripts/convert.sh --tool gemini-cli
```
