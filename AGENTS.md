# AGENTS.md

Guidance for AI coding agents working in this repository.

## What this is

`@three-ws/assistant-mcp` v0.1.2. Generate a paste-ready three.ws assistant widget from any AI agent. build_assistant_widget turns a config into an embeddable <script> tag, a frame URL, and a ThreeAssistant.init() snippet for a floating 3D avatar chatbot on any website; list_assistant_options enumerates every avatar, background, mode and data-* attribute you can set. Pure, offline, deterministic, no key, no signer, no payment.

A Model Context Protocol server. Run it over stdio from any MCP client.

## Use it

```bash
npx -y @three-ws/assistant-mcp
```

Full usage, tool list and configuration are in [README.md](README.md). Machine-readable summaries: [llms.txt](llms.txt) and [llms-full.txt](llms-full.txt).

## Develop

```bash
npm install
npm test
```

Scripts:
- `npm run start`: `node src/index.js`
- `npm run test`: `node --test "test/**/*.test.mjs"`
- `npm run inspect`: `npx -y @modelcontextprotocol/inspector node src/index.js`

## Conventions

- ES modules, Node >=20.
- Read-only by default. Anything that signs, spends or sends must be an explicit, separately named tool or option, and must never be inferred from untrusted text (token names, memos, listings).
- Never commit credentials. Configuration comes from environment variables documented in the README.
- Keep changes small and covered by a test next to the code they change.

## Source of truth

This repository is a generated mirror of `packages` in https://github.com/nirholas/three.ws. Open issues here; send substantial changes as a pull request here or upstream.
