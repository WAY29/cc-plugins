# CC-Plugins

Claude Code 插件集合，提供增强的输出风格和专用 Agent。

## 插件列表

| 插件 | 说明 |
|------|------|
| `full stack engineer` | Full Stack Engineer 风格 - 严格的 RIPER-5 工作流与三层探索协议 |
| `agents/code-writer` | 专注代码编写的轻量 Agent (Haiku) |

## 安装

### 1. 安装插件

```bash
claude plugins:add github:way29/cc-plugins/plugins
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
