# OpenClaw 集成

OpenClaw 智能体以工作区形式安装，每个工作区包含 `SOUL.md`、`AGENTS.md`、`IDENTITY.md`。
安装器会把每个工作区复制到 `~/.openclaw/agency-agents/`，并在本机存在 `openclaw` CLI 时自动注册。

安装前，请先生成 OpenClaw 工作区：

```bash
./scripts/convert.sh --tool openclaw
```

## 安装

```bash
./scripts/install.sh --tool openclaw
```

## 激活智能体

安装完成后，可在 OpenClaw 会话中通过 `agentId` 使用。

如果 OpenClaw 网关已经在运行，安装后请重启：

```bash
openclaw gateway restart
```

## 重新生成

```bash
./scripts/convert.sh --tool openclaw
```
