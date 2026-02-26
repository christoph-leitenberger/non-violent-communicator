# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## What This Is

An **MCP (Model Context Protocol) server** that provides Nonviolent Communication (NVC) tools and knowledge to any MCP-compatible LLM client (Claude Desktop, Claude Code, etc.).

### Architecture

- **`index.js`** — Single-file MCP server using `@modelcontextprotocol/sdk`. All NVC knowledge is embedded inline as template literals. Exposes 4 tools and 7 browsable resources. Communicates via stdio transport.
- **`PROMPT.md`** — Standalone copy-paste prompt for non-MCP users (any LLM chat).
- **No API keys, no network calls, no disk writes** — the server assembles knowledge + instructions and returns them to the host LLM for processing.

### How It Works

Each tool (e.g. `thought_clarifier`) does NOT call an external API. It:
1. Takes the user's input
2. Assembles a structured prompt containing the embedded NVC knowledge base + analysis instructions + the user's text
3. Returns this to the host LLM, which performs the actual NVC analysis

### Key Commands

```bash
npm install          # Install dependencies
node index.js        # Run the MCP server
```

## Tools

1. **Thought Clarifier** — free-form text → NVC analysis (feelings, needs, request)
2. **Message Transformer** — rewrite any message using NVC principles
3. **NVC Trainer** — interactive NVC practice exercises
4. **Political Discourse** — analyze political citations through the NVC lens

## Greeting

When starting a new conversation, greet the user with a warm welcome that covers the following — in your own words, conversationally, not as a raw list:

1. **What this is**: This project provides NVC (Nonviolent Communication) tools that help surface the feelings and needs behind everyday thoughts and messages.
2. **The four tools and what you can do with them**:
   - **Thought Clarifier** — paste any raw thought, rant, or journal entry to get a structured NVC breakdown. *Example: "I'm so frustrated that my colleague keeps interrupting me in meetings."*
   - **Message Transformer** — rewrite a difficult email, chat message, or piece of feedback using NVC principles. *Example: "Can you rewrite this message to my manager in NVC?"*
   - **NVC Trainer** — practice identifying observations, feelings, needs, and requests with interactive exercises at three difficulty levels. *Example: "Give me a beginner exercise on feelings."*
   - **Political Discourse** — analyze political quotes through the NVC lens, surfacing the human needs behind the rhetoric. *Example: "Analyze this quote from last night's debate."*
3. **Browsable knowledge base**: The user can explore NVC concepts directly — feelings catalog (~120 feelings), needs catalog (9 categories), the four components of NVC, core principles, and worked examples.
4. **Invitation**: End with a friendly nudge like *"Tell me what's on your mind and I'll find the feelings and needs underneath — or ask me for a practice exercise to sharpen your NVC skills."*

---

## Working Style

- **Always use plan mode** before implementing any non-trivial task. Explore the codebase, design an approach, and get user approval before writing code.
- **Always ask for clarification** when anything is unclear. Do not make assumptions about ambiguous requirements.
- **Before starting any task**, ask the user for:
  - **Goal**: What is the desired outcome?
  - **Constraints**: Any limitations (tech stack, performance, compatibility, scope)?
  - **Format**: Expected output format (file, function, API, UI, etc.)?
  - **Failure conditions**: What would make this implementation wrong or unacceptable?
- **Always present three possible solutions** before implementing, ranked by probability of being the right fit, with a brief rationale for each. Then ask the user which to proceed with.
- **Security warnings**: At each implementation step, explicitly call out any security issues the user might encounter — including secrets management, injection risks, dependency vulnerabilities, exposed endpoints, or insecure defaults. Do this proactively, not only when asked.
