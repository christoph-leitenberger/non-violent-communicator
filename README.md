# NVC MCP Server

Nonviolent Communication tools for any LLM — via MCP or a copy-paste prompt.

## Pick Your Path

### MCP users (Claude Desktop, Claude Code, Cursor, etc.)

Run as MCP server — no API keys, no network calls:

```bash
npx non-violent-communicator
```

Add to your MCP client config (e.g. `claude_desktop_config.json`):

```json
{
  "mcpServers": {
    "nvc": {
      "command": "npx",
      "args": ["non-violent-communicator"]
    }
  }
}
```

You get 4 tools — thought clarifier, message transformer, NVC trainer, and political discourse analyzer — plus a browsable NVC knowledge base.

### Everyone else

Copy **[PROMPT.md](PROMPT.md)** into any LLM chat (ChatGPT, Gemini, Copilot, etc.) for the full NVC assistant experience — zero installs.

## Local development

```bash
git clone <repo-url>
cd non-violent-communicator
npm install
node index.js
```

## License

MIT
