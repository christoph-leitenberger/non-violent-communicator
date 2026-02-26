# NVC MCP Server

Nonviolent Communication tools for any LLM — via MCP or a copy-paste prompt.

## Pick Your Path

### MCP users (Claude Desktop, Cursor, etc.)

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

No API keys, no network calls. You get 4 tools — thought clarifier, message transformer, NVC trainer, and political discourse analyzer — plus a browsable NVC knowledge base.

### Claude Code users

This repo includes `.claude/settings.json` — clone it and the NVC MCP server is configured automatically. Or add it manually to your project or global settings:

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

### Any LLM (ChatGPT, Gemini, Copilot, etc.) — no install needed

Open **[PROMPT.md](PROMPT.md)**, click the **copy raw file** button (clipboard icon, top-right), and paste it as the first message in any LLM chat. Done — your LLM is now an NVC assistant with all four capabilities.

> **Direct link:** [Copy the raw prompt](https://raw.githubusercontent.com/christoph-leitenberger/non-violent-communicator/master/PROMPT.md) — select all, copy, paste into your chat.

## What You Get

| Tool | What it does |
|---|---|
| **Thought Clarifier** | Paste any raw thought, rant, or journal entry — get a structured NVC breakdown (observations, feelings, needs, request) |
| **Message Transformer** | Rewrite a difficult email, chat message, or feedback using NVC principles |
| **NVC Trainer** | Practice identifying observations, feelings, needs, and requests with interactive exercises (3 difficulty levels) |
| **Political Discourse** | Analyze political quotes through the NVC lens — surface life-alienating patterns and the human needs behind the rhetoric |

## Local development

```bash
git clone https://github.com/christoph-leitenberger/non-violent-communicator.git
cd non-violent-communicator
npm install
node index.js
```

## License

MIT
