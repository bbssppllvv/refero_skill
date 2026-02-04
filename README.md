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
  - `example-workflow.md` — Complete fintech onboarding example

## Requirements

- [Refero MCP server](https://refero.design) for design research tools

## Usage

Once installed, the skill activates when you ask to design, build, or create UI. The agent will:

1. Ask discovery questions (what, who, goals)
2. Research with Refero MCP (search_screens, search_flows, get_screen)
3. Analyze patterns and extract tactics
4. Apply craft principles (typography, color, spacing, motion)
5. Implement with quality checks

## License

MIT
