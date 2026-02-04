# Refero Design Skill

Research-First design methodology. Teaches AI to create professional UI/UX by researching real products first — avoiding generic "AI slop" designs.

## Install

```bash
npx skills add https://github.com/bbssppllvv/refero_skill
```

Requires [Refero MCP](https://refero.design) — 150K+ screens and flows from real products.

---

<details>
<summary>Setup Refero MCP</summary>

### Get token

Sign up at [refero.design](https://refero.design)

### Add to your tool

**Claude Code / Gemini CLI:**
```bash
claude mcp add --transport http refero https://api.refero.design/v1/mcp --header "Authorization: <token>"
```

**Cursor:** [One-click install](https://cursor.com/docs/context/mcp/install-links)

**Lovable:** Settings → Connectors → New MCP server → URL: `https://api.refero.design/v1/mcp` → Bearer token

**Other tools:**
```
URL: https://api.refero.design/v1/mcp
Auth: Bearer <token>
```

</details>

<details>
<summary>Skill installation troubleshooting</summary>

Specify agent explicitly:
```bash
npx skills add https://github.com/bbssppllvv/refero_skill --agent cursor
```

Or clone directly:
```bash
git clone https://github.com/bbssppllvv/refero_skill.git .cursor/skills/refero-design
```

</details>

<details>
<summary>What's inside</summary>

- **SKILL.md** — Methodology: Discovery → Research → Analyze → Design → Implement
- **references/**
  - `typography.md` — Type scale, pairing, letter-spacing
  - `color.md` — Palettes, tokens, dark mode
  - `motion.md` — Micro-interactions, timing, easing
  - `icons.md` — Sizing, optical corrections
  - `craft-details.md` — Focus states, forms, accessibility
  - `anti-ai-slop.md` — Avoiding generic AI look
  - `mcp-tools.md` — Refero tools reference
  - `example-workflow.md` — SaaS churn example

</details>

## License

MIT
