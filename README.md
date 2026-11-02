# Phaze MCP

Things your AI agent can do on your other computers with [Phaze](https://phaze.app).

There is nothing to install here beyond Phaze and your AI agent. Each playbook is a prompt you can copy, plus what helps it go well.

## Set up once

1. Download [Phaze](https://phaze.app) and sign in on both computers.
2. On the computer you're sitting at, open Phaze's client settings and turn on the experimental **MCP server** feature. Keep the app open.
3. Add it to your agent. In Claude Code:

   ```bash
   claude mcp add --transport http phaze http://127.0.0.1:41010/mcp
   ```

   Claude Desktop, ChatGPT and Codex are covered in [The Phaze MCP Server](https://help.phaze.app/articles/6522930271-the-phaze-mcp-server).
4. Start a new chat and try: `List my Phaze computers, connect to one, and tell me what's on its screen.`

Phaze connects Windows computers for now, and the MCP server is experimental, so let us know what you find.

## Playbooks

| Playbook | What it does |
|---|---|
| [Watch a long job](playbooks/watch-a-long-job.md) | Watches a build, render or export on another PC, tries to fix a failure, and lets you know what happened |
| [Watch a render](playbooks/watch-a-render.md) | Runs a Blender render on another PC, restarts it if it stops, and tells you what happened |
| [Watch an Unreal build](playbooks/watch-an-unreal-build.md) | Packages an Unreal project on another PC, tries to fix a failure, and lets you know what happened |

## Learnings for any job

[LEARNINGS.md](LEARNINGS.md) works for every playbook. Paste it into your agent's instructions, or ask your agent to read it first.
