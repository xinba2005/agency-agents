# MCP Memory 集成

> 通过 Model Context Protocol（MCP）为任意智能体提供跨会话持久记忆。

## 作用

默认情况下，The Agency 的智能体每次会话都从零开始，需要手动在会话或智能体间复制上下文。
接入 MCP 记忆服务后可以实现：

- **跨会话记忆**：记住历史决策、交付物与上下文
- **交接连续性**：一个智能体交接给另一个时，可直接回忆先前工作
- **失败回滚**：当 QA 失败或架构方向错误时，回退到已知正确状态

## 配置

你需要一个提供 `remember`、`recall`、`rollback`、`search` 工具的 MCP 服务。
在 MCP 客户端（Claude Code、Cursor 等）中配置：

```json
{
  "mcpServers": {
    "memory": {
      "command": "your-mcp-memory-server",
      "args": []
    }
  }
}
```

任何暴露上述 4 个工具的 MCP 服务都可使用。可参考 [MCP 生态](https://modelcontextprotocol.io)。

## 如何给任意智能体加入记忆能力

在智能体提示词中增加一个 **Memory Integration** 章节，指导其在关键时刻使用记忆工具。

### 推荐模式

```markdown
## Memory Integration

When you start a session:
- Recall relevant context from previous sessions using your role and the current project as search terms
- Review any memories tagged with your agent name to pick up where you left off

When you make key decisions or complete deliverables:
- Remember the decision or deliverable with descriptive tags (your agent name, the project, the topic)
- Include enough context that a future session  or a different agent  can understand what was done and why

When handing off to another agent:
- Remember your deliverables tagged for the receiving agent
- Include the handoff metadata: what you completed, what's pending, and what the next agent needs to know

When something fails and you need to recover:
- Search for the last known-good state
- Use rollback to restore to that point rather than rebuilding from scratch
```

### 这会带来什么

给出以上指引后，LLM 会在流程中自动使用 MCP 工具：

- `remember`：保存决策、交付物或上下文快照
- `recall`：按关键词、标签、语义召回历史记忆
- `rollback`：出现问题时回退到历史状态
- `search`：跨会话、跨智能体检索指定信息

无需改智能体代码，也不需要手写 API 调用。

## 示例：增强 Backend Architect

完整示例见 [backend-architect-with-memory.md](backend-architect-with-memory.md)。

## 示例：记忆驱动工作流

见 [../../examples/workflow-with-memory.md](../../examples/workflow-with-memory.md)，展示如何用记忆替代人工复制粘贴进行跨智能体上下文传递。

## 建议

- **统一标签**：每条记忆都加上智能体名和项目名
- **让模型判断关键点**：规则是指导，不必僵化执行
- **优先使用回滚**：当质量检查失败时，优先回到最近稳定检查点
