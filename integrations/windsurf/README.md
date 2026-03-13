# Windsurf 集成

全部 61 个 Agency 智能体会合并为单个 `.windsurfrules` 文件。
规则是**项目级**的，请在目标项目根目录安装。

## 安装

```bash
# 在你的项目根目录执行
cd /your/project
/path/to/agency-agents/scripts/install.sh --tool windsurf
```

## 激活智能体

在 Windsurf 中，用提示词按名称引用智能体：

```
使用 Frontend Developer 智能体实现这个组件。
```

## 重新生成

```bash
./scripts/convert.sh --tool windsurf
```
