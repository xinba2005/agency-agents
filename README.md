# 🎭 The Agency：可直接部署的 AI 专家团队

> 一个放在你手边的完整 AI Agency。前端、后端、设计、营销、产品、测试、运维、空间计算等角色齐全，且每个角色都有明确人格、流程和可交付结果。

[![GitHub stars](https://img.shields.io/github/stars/msitarzewski/agency-agents?style=social)](https://github.com/msitarzewski/agency-agents)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg)](https://makeapullrequest.com)

---

## 🚀 这是什么

The Agency 是一套可复用的专业智能体体系，不是通用提示词合集。

每个智能体都具备：

- **专业领域深度**：覆盖工程、设计、营销、销售、产品、项目管理、测试等
- **清晰人格与沟通风格**：输出风格稳定，不是一次性临时模板
- **可交付导向**：强调代码、文档、流程、指标等可验证产出
- **可落地流程**：内置步骤、质量门槛与成功标准

你可以把它理解为：
一个可随时调用、可并行协作、可持续迭代的 AI 专家团队。

---

## ⚡ 快速开始

### 方式 1：用于 Claude Code（推荐）

```bash
# 复制智能体到 Claude 目录
cp -r agency-agents/* ~/.claude/agents/

# 在会话中激活
# 例如：Activate Frontend Developer and help me build a React component.
```

### 方式 2：直接当作角色库参考

每个智能体文件通常包含：

- 身份与行为特征
- 核心任务与工作流
- 技术产出与示例
- 质量标准与成功指标

### 方式 3：接入其他工具（Cursor / Copilot / Aider / Windsurf / Gemini CLI / OpenCode / OpenClaw）

```bash
# 1) 生成各工具需要的集成文件
./scripts/convert.sh

# 2) 交互式安装（自动检测本机工具）
./scripts/install.sh

# 3) 安装指定工具
./scripts/install.sh --tool cursor
./scripts/install.sh --tool copilot
./scripts/install.sh --tool aider
./scripts/install.sh --tool windsurf
./scripts/install.sh --tool gemini-cli
./scripts/install.sh --tool opencode
./scripts/install.sh --tool openclaw
```

---

## 🧩 目录说明

- `engineering/`：工程角色（前端、后端、AI、安全、DevOps、架构等）
- `design/`：设计角色（UI、UX、品牌、视觉叙事、包容性视觉等）
- `marketing/`：营销角色（内容、社媒、SEO、短视频、电商等）
- `paid-media/`：投放角色（PPC、素材、归因、审核等）
- `sales/`：销售角色（外呼、商机、提案、售前、管道分析等）
- `product/`：产品角色（优先级、趋势、反馈、行为设计等）
- `project-management/`：项目管理角色（计划、推进、Jira、实验追踪等）
- `testing/`：测试角色（API、性能、可访问性、证据化验收等）
- `support/`：支持角色（客服、分析、财务、法务、基础设施等）
- `spatial-computing/`：空间计算角色（XR、visionOS、WebXR、Metal 等）
- `specialized/`：专精角色（编排、治理、合规、文档、招聘、供应链等）
- `game-development/`：游戏开发角色（跨引擎 + Unity/Unreal/Godot/Roblox）
- `examples/`：多智能体实战示例
- `integrations/`：各工具集成与安装说明

---

## 🎯 典型使用场景

### 1) 创业 MVP

推荐组合：

1. Frontend Developer
2. Backend Architect
3. Rapid Prototyper
4. Growth Hacker
5. Reality Checker

效果：缩短从想法到首版上线的周期，且质量可控。

### 2) 企业功能开发

推荐组合：

1. Senior Project Manager
2. Senior Developer
3. UI Designer
4. Experiment Tracker
5. Evidence Collector
6. Reality Checker

效果：在复杂协作下维持需求清晰、质量可验收、上线可追踪。

### 3) 广告账户接管

推荐组合：

1. Paid Media Auditor
2. Tracking & Measurement Specialist
3. PPC Campaign Strategist
4. Search Query Analyst
5. Ad Creative Strategist

效果：快速完成账户体检、追踪修正、结构重建和投放提效。

---

## 🔌 多工具集成

支持：

- Claude Code（原生）
- GitHub Copilot（原生）
- Antigravity
- Gemini CLI
- OpenCode
- OpenClaw
- Cursor
- Aider
- Windsurf

查看详细安装与激活方式：

- [integrations/README.md](integrations/README.md)

---

## 📚 示例与工作流

推荐先阅读：

- [examples/README.md](examples/README.md)
- [examples/workflow-startup-mvp.md](examples/workflow-startup-mvp.md)
- [examples/workflow-landing-page.md](examples/workflow-landing-page.md)
- [examples/nexus-spatial-discovery.md](examples/nexus-spatial-discovery.md)

---

## 🤝 贡献方式

欢迎贡献新的智能体或改进现有角色：

1. Fork 本仓库
2. 在合适目录新增/修改智能体文件
3. 保持结构完整（身份、任务、流程、交付、指标）
4. 提交 PR

也欢迎把你的实战案例提交到 `examples/`。

---

## 🧠 设计理念

The Agency 的核心原则：

1. **强角色**：有稳定人格和表达方式
2. **强交付**：输出可执行、可验证、可复用
3. **强流程**：有步骤、有边界、有质量门槛
4. **强协作**：支持多角色并行与交接
5. **强迭代**：可持续优化，不是一次性提示词

---

## 📊 项目概况

- 覆盖十多个业务分组
- 含大量专业智能体定义与流程模板
- 提供多工具转换和安装脚本
- 包含真实多智能体协作示例

---

## 🌐 社区翻译

本项目已有社区维护的中文本地化分支与衍生版本，可根据需要选择使用。

---

## 📜 许可证

MIT License。
可自由用于个人和商业场景。

---

## 🚀 开始使用

1. 先从一个目标任务出发（如落地页上线或MVP 验证）
2. 在对应分组里挑选 2-5 个角色
3. 按工作流并行执行，再由质量角色做验收
4. 将有效流程沉淀为团队标准

<div align="center">

**The Agency：让 AI 从会回答变成能交付**

</div>
