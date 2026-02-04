# Refero Design Skill

[Refero](https://refero.design) is a design inspiration platform — 150K+ screens and 6K+ flows from the best products.

AI agents have generic design knowledge. This skill gives them **specific knowledge** — real patterns, real flows, real solutions from companies like Stripe, Linear, Notion, and thousands more.

**What changes:**
- Agent researches 150K+ screens before designing, not guessing from training data
- Decisions grounded in how top products actually solve problems
- User flows based on real onboarding, checkout, settings patterns
- Visual craft informed by industry standards, not AI defaults

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
