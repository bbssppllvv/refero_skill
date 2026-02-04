# Refero Design Skill

**Make your AI agent design like a senior product designer.**

When AI creates UI, it draws from generic training data — the result looks "AI-generated". This skill changes that: before designing anything, your agent researches [Refero](https://refero.design)'s library of 150K+ screens and 6K+ flows from Stripe, Linear, Notion, and thousands of top products.

**The difference:**
- Without skill: AI guesses based on generic patterns → forgettable UI
- With skill: AI researches real products first → designs grounded in what actually works

Works with Claude Code, Cursor, Gemini, Lovable, and other AI tools that support MCP.

## Install

```bash
npx skills add https://github.com/bbssppllvv/refero_skill
```

Requires Refero MCP server (connects your AI to Refero's design library).

---

<details>
<summary>Setup Refero MCP</summary>

### 1. Get token

Sign up at [refero.design](https://refero.design)

### 2. Add MCP

**Claude Code** (terminal):
```bash
claude mcp add --transport http refero https://api.refero.design/v1/mcp --header "Authorization: <token>"
```

**Gemini CLI** (terminal):
```bash
gemini mcp add --transport http refero https://api.refero.design/v1/mcp --header "Authorization: <token>"
```

**Cursor:** Add to `.cursor/mcp.json`:
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

**Lovable:** Settings → Connectors → New MCP server → URL: `https://api.refero.design/v1/mcp` → Bearer token

**Other tools:**
```
URL: https://api.refero.design/v1/mcp
Auth: Bearer <token>
```

</details>

<details>
<summary>Skill troubleshooting</summary>

Specify agent:
```bash
npx skills add https://github.com/bbssppllvv/refero_skill --agent cursor
```

Or clone:
```bash
git clone https://github.com/bbssppllvv/refero_skill.git .cursor/skills/refero-design
```

</details>

<details>
<summary>What's inside</summary>

- **SKILL.md** — Research-First methodology: Discovery → Research → Analyze → Design → Implement
- **references/** — typography, color, motion, icons, craft-details, anti-ai-slop, mcp-tools, example-workflow

</details>

## License

MIT
