# Refero Design Skill

**Design with data, not defaults.**

Every AI agent has the same problem: it draws UI from training data averages. The result? Generic layouts, safe color choices, patterns you've seen a thousand times. Design that looks "AI-generated."

This skill changes that.

Before creating anything, your agent researches [Refero](https://refero.design) — a library of 150,000+ screens and 6,000+ flows from the world's best products. Stripe's checkout. Linear's onboarding. Notion's settings. The patterns that actually convert, retain, and delight.

**The shift:**
- From guessing → to researching
- From "best practices" → to specific solutions that shipped
- From generic → to grounded in what top products actually do

Your agent stops generating. It starts designing with evidence.

## Install

```bash
npx skills add https://github.com/bbssppllvv/refero_skill
```

Requires Refero MCP to connect your agent to the design library.

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
