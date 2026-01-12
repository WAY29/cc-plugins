# SuperBrain

Claude Code 插件：`super-brain`。提供 `SuperBrain` 输出风格与配套 Agents。

## 包含内容

### Output Styles

| 名称 | 文件 | 说明 |
|------|------|------|
| `SuperBrain` | `plugins/output-styles/superbrain.md` | RIPER-5 工作流 + 严格三层探索协议（Verification-First） |

### Agents

| 名称 | 文件 | 说明 |
|------|------|------|
| `code-explorer` | `plugins/agents/code-explorer.md` | 代码库探索与调用链追踪 |
| `code-writer` | `plugins/agents/code-writer.md` | 聚焦文件读写的代码编写 |

## 安装

### 1. 安装插件
在claude-code中输入
```bash
/plugin marketplace add way29/cc-plugins
```

### 2. 安装依赖 MCP 服务器

插件依赖以下 MCP 服务器以发挥完整功能：

#### Auggie (代码库语义检索)

```bash
npm install -g @augmentcode/auggie@latest

claude mcp add-json auggie -s user '{
  "command": "auggie",
  "args": ["--mcp"],
  "env": {
    "AUGMENT_API_TOKEN": "your_token_here",
    "AUGMENT_API_URL": "your_url_here"
  }
}'
```

#### Context7 (库文档查询)

```bash
claude mcp add-json context7 -s user '{
  "type": "http",
  "url": "https://mcp.context7.com/mcp",
  "headers": {
    "CONTEXT7_API_KEY": "your_api_key_here"
  }
}'
```

## 许可证

MIT
