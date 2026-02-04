# Refero Design Skill

Research-First design methodology using [Refero MCP](https://refero.design). 

This skill teaches AI agents to create professional UI/UX by researching real products first, extracting patterns, and applying craft principles — avoiding generic "AI slop" designs.

## Installation

```bash
npx skills add https://github.com/bbssppllvv/refero_skill
```

<details>
<summary>Troubleshooting & manual install</summary>

If skill is not recognized, specify your agent explicitly:
```bash
npx skills add https://github.com/bbssppllvv/refero_skill --agent cursor
```

Or clone directly:
```bash
git clone https://github.com/bbssppllvv/refero_skill.git .cursor/skills/refero-design
```

</details>

## What's Inside

- **SKILL.md** — Core methodology: Discovery → Research → Analyze → Design → Implement
- **references/** — Deep-dive guides:
  - `typography.md` — Type scale, pairing, letter-spacing
  - `color.md` — Palettes, tokens, dark mode
  - `motion.md` — Micro-interactions, timing, easing
  - `icons.md` — Sizing, optical corrections, libraries
  - `craft-details.md` — Focus states, forms, accessibility
  - `anti-ai-slop.md` — How to avoid generic AI-generated look
  - `mcp-tools.md` — Refero MCP tools reference
  - `example-workflow.md` — Complete SaaS churn example

## Usage

Once installed, the skill activates when you ask to design, build, or create UI. The agent will:

1. Ask discovery questions (what, who, goals)
2. Research with Refero MCP (search_screens, search_flows, get_screen)
3. Analyze patterns and extract tactics
4. Apply craft principles (typography, color, spacing, motion)
5. Implement with quality checks

---

<details>
<summary>Don't have Refero MCP yet? Setup instructions</summary>

This skill requires **Refero MCP** — a design research tool with 150K+ screens and flows from real products.

### 1. Get your token

Go to [refero.design](https://refero.design) and sign up for API access.

### 2. Add MCP to your tool

**Claude Code** (terminal):
```bash
claude mcp add --transport http refero https://api.refero.design/v1/mcp --header "Authorization: <token>"
```

**Cursor**: [One-click install](https://cursor.com/docs/context/mcp/install-links)

**Gemini CLI** (terminal):
```bash
gemini mcp add --transport http refero https://api.refero.design/v1/mcp --header "Authorization: <token>"
```

**Lovable**:
1. Settings → Connectors → Personal connectors
2. Click "New MCP server"
3. Server name: `Refero`
4. Server URL: `https://api.refero.design/v1/mcp`
5. Select "Authorization with Bearer token" and enter your token

**Other tools** — use these settings:
- HTTP URL: `https://api.refero.design/v1/mcp`
- Bearer token: `<token>`

</details>

## License

MIT
