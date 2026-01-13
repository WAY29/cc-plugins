# SuperBrain

Claude Code 插件：`super-brain`。提供 `SuperBrain` 输出风格、配套 Agents 与 Skills。

## 包含内容

### Output Styles

| 名称 | 文件 | 说明 |
|------|------|------|
| `SuperBrain` | `output-styles/superbrain.md` | RIPER-5 工作流 + 严格三层探索协议（Verification-First） |

### Agents

| 名称 | 文件 | 说明 |
|------|------|------|
| `code-explorer` | `agents/code-explorer.md` | 代码库探索与调用链追踪 |
| `code-writer` | `agents/code-writer.md` | 聚焦文件读写的代码编写 |

### Skills

| 名称 | 文件 | 说明 |
|------|------|------|
| `brainstorming` | `skills/brainstorming/brainstorming.md` | 创意工作前的头脑风暴，探索需求与设计 |

## 安装

### 1. 安装插件

在 Claude Code 中输入：

```bash
/plugin marketplace add way29/cc-plugins
/plugin install super-brains@way29/cc-plugins
```

### 2. 配置环境变量

插件依赖以下 MCP 服务器（已集成，无需手动安装），只需设置对应的环境变量：

#### Auggie (代码库语义检索)

```bash
export AUGGIE_API_TOKEN="your_token_here"
export AUGGIE_API_URL="your_url_here"
```

#### Context7 (库文档查询)

```bash
export CONTEXT7_API_KEY="your_api_key_here"
```

## 许可证

MIT
