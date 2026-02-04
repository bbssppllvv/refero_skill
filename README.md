# Refero Design Skill

Design with data, not defaults.

AI generates UI from training data averages. This skill connects your agent to [Refero](https://refero.design) — 150K screens and 6K flows from products like Stripe, Linear, and Notion. Before designing, your agent researches what actually ships.

## Install

```bash
npx skills add https://github.com/bbssppllvv/refero_skill
```

Requires Refero MCP.

---

<details>
<summary>Setup Refero MCP</summary>

### 1. Get your token

[refero.design](https://refero.design)

### 2. Connect

**Claude Code:**
```bash
claude mcp add --transport http refero https://api.refero.design/v1/mcp --header "Authorization: <token>"
```

**Gemini CLI:**
```bash
gemini mcp add --transport http refero https://api.refero.design/v1/mcp --header "Authorization: <token>"
```

**Cursor** — add to `.cursor/mcp.json`:
```json
{
  "mcpServers": {
    "refero": {
      "url": "https://api.refero.design/v1/mcp",
      "headers": { "Authorization": "<token>" }
    }
  }
}
```

**Lovable:** Settings → Connectors → New MCP server → `https://api.refero.design/v1/mcp` → Bearer token

**Other tools:**
```
URL: https://api.refero.design/v1/mcp
Auth: Bearer <token>
```

</details>

<details>
<summary>Troubleshooting</summary>

```bash
npx skills add https://github.com/bbssppllvv/refero_skill --agent cursor
```

Or clone:
```bash
git clone https://github.com/bbssppllvv/refero_skill.git .cursor/skills/refero-design
```

</details>

## License

MIT
