# Aider 集成

所有 61 个 Agency 智能体会被合并为一个 `CONVENTIONS.md` 文件。
当该文件位于项目根目录时，Aider 会自动读取。

## 安装

```bash
# 在你的项目根目录执行
cd /your/project
/path/to/agency-agents/scripts/install.sh --tool aider
```

## 激活智能体

在 Aider 会话中，直接按名称引用智能体：

```
使用 Frontend Developer 智能体重构这个组件。
```

```
使用 Reality Checker 智能体验证这个功能是否可用于生产。
```

## 手动使用

你也可以显式传入约定文件：

```bash
aider --read CONVENTIONS.md
```

## 重新生成

```bash
./scripts/convert.sh --tool aider
```
