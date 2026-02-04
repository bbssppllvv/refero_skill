# Refero Design Skill

**Give your AI agent access to the world's best UX/UI.**

[Refero](https://refero.design) — 150K+ screens and 6K+ flows from top products. This skill teaches AI to research before designing, replacing generic output with patterns from Stripe, Linear, Notion, and thousands more.

- 🔍 **Research, don't guess** — agent explores real products before every design decision
- 🎯 **Specific, not generic** — actual solutions from companies that nailed it
- ✨ **Craft that ships** — typography, color, spacing based on industry standards

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
