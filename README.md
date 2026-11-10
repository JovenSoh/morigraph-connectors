# morigraph connectors

Public installation packages for morigraph, a hosted MCP gateway for enabled AI tools, connected accounts, workspace context, memory, files and reusable skills.

This repository contains installation metadata and public agent instructions. It does not contain the morigraph backend, credentials or reviewer access. Marketplace submissions are being prepared; this repository does not imply marketplace approval or a completed host compatibility certification.

## Connect

Remote MCP URL: https://morigraph.com/mcp
Transport: Streamable HTTP. Authentication: browser OAuth.
Sign in with your morigraph account and choose the intended workspace. Each connected account needs its own explicit authorization. Included AI capabilities consume morigraph credits; connected services may require their own plans.

### Cursor

The root plugin.json and mcp.json use the Agent Plugins format. Follow Cursor's supported local plugin or marketplace installation flow. A marketplace listing is not yet approved. After adding the connection, complete browser OAuth and verify an actual workspace read.

### Gemini CLI

```sh
gemini extensions install https://github.com/JovenSoh/morigraph-connectors
```

Complete the MCP OAuth sign-in in Gemini CLI. Native installation, OAuth and first-task verification are still part of release validation. The root gemini-extension.json configures the same production gateway.

### Claude Code and Codex

The published setup CLI is also available:

```sh
npx @morigraph/cli@0.3.0 setup --client claude-code
npx @morigraph/cli@0.3.0 setup --client codex
```

Use the environment that actually configures your agent. A cloud sandbox does not necessarily configure your desktop app. Existing compatible brainlet server/skill identifiers are retained to avoid duplicates.

## First useful task

Ask your agent to read a document you saved in your morigraph workspace. Missing files are reported as missing. Writes, connected-account operations and paid capabilities require the appropriate user intent, permissions and available credits. This package does not authorize unattended writes or payments.

## Support and data practices

- Website: https://morigraph.com/
- Setup: https://morigraph.com/setup.md
- Support: https://morigraph.com/support.html
- Privacy: https://morigraph.com/privacy.html
- Terms: https://morigraph.com/terms.html

The hosted service remains subject to morigraph's terms. No separate open-source license grant is made by this repository.
