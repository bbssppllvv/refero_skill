# Refero Design Skill

[Refero](https://refero.design) is a design inspiration platform — 150K+ screens and flows from the best products. This skill + MCP server bring Refero's library to AI agents, enabling research-driven design based on real industry patterns.

**Why use it:**
- **Grounded in reality** — designs based on proven patterns from Stripe, Linear, Notion, and 1000s more
- **No more "AI slop"** — specific references replace generic solutions
- **Professional craft** — typography, color, spacing, motion done right
- **Faster research** — AI finds relevant examples in seconds, not hours

## Install

```bash
npx skills add https://github.com/bbssppllvv/refero_skill
```

Requires Refero MCP server.

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
