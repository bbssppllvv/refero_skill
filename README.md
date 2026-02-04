# Refero Design Skill

Research-First design methodology using [Refero MCP](https://refero.design). 

This skill teaches AI agents to create professional UI/UX by researching real products first, extracting patterns, and applying craft principles — avoiding generic "AI slop" designs.

## Installation

### Option 1: Using npx skills (recommended)

```bash
# For specific agent (Claude Code)
npx skills add https://github.com/bbssppllvv/refero_skill --agent claude-code

# For Cursor
npx skills add https://github.com/bbssppllvv/refero_skill --agent cursor

# For Codex
npx skills add https://github.com/bbssppllvv/refero_skill --agent codex
```

### Option 2: Manual installation

```bash
# Claude Code
git clone https://github.com/bbssppllvv/refero_skill.git .claude/skills/refero-design

# Cursor
git clone https://github.com/bbssppllvv/refero_skill.git .cursor/skills/refero-design

# Codex
git clone https://github.com/bbssppllvv/refero_skill.git .codex/skills/refero-design
```

### Troubleshooting

If skill is not recognized after `npx skills add -y`, it may have installed to `.agents/skills/` instead of agent-specific folder. Fix:

```bash
# For Claude Code
cp -r .agents/skills/refero-design .claude/skills/
```

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
