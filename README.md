![Refero Design Skill](assets/banner.png)

# Refero Design Skill

**Design with data, not defaults.**

AI agents design from training data averages — generic layouts, safe colors, patterns you've seen a thousand times. You've seen the result: design that looks "AI-generated." This skill fixes that.

**Your agent gets access to real design research.** Before creating anything, it searches [Refero](https://refero.design) — the largest curated library of product design: 150,000+ screens and 6,000+ complete user flows from Stripe, Linear, Notion, Figma, Vercel, and thousands of the best products ever built.

**Not just screenshots — structured data.** Every screen has rich metadata: UI components, design patterns, typography choices, color palettes, layout structures. Your agent doesn't just see designs — it understands them.

**Semantic search that actually works.** Looking for a pricing page with annual/monthly toggle? An onboarding flow for fintech? A dark mode dashboard with data tables? A cancellation flow that reduces churn? If the pattern exists in the wild, your agent will find it. This is the kind of research that takes designers hours — done in seconds.

**Problems regular AI can't solve.** Without real-world data, AI agents guess. They produce "safe" designs that look like everything else. With Refero, your agent researches first, then designs with confidence. The difference is visible.

**Craft knowledge built in.** The skill includes deep guides on typography, color systems, spacing, motion, and icons — the details that separate polished products from rough prototypes. Letter-spacing rules. Color token architecture. Animation timing curves. The stuff AI usually gets wrong.

**Anti-slop by design.** Explicit rules to avoid the generic AI look: no default indigo, no blob backgrounds, no hero-features-pricing-FAQ templates. Your agent learns what makes design feel human and intentional — and what screams "generated."

**A complete methodology.** From discovery questions through research, analysis, design, and implementation — with quality gates and side-by-side validation against real products. Not just tools — a way of working.

## Install

```bash
npx skills add https://github.com/bbssppllvv/refero_skill
```

Requires [Refero MCP](#setup-refero-mcp) to connect your agent to the design library.

---

<details id="setup-refero-mcp">
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

<details>
<summary>What's inside</summary>

**SKILL.md** — Research-First methodology
- Discovery questions before designing
- Research strategies and query patterns  
- Analysis frameworks and steal lists
- Design craft summaries
- Quality gates and validation

**Reference guides:**
- `typography.md` — Scale, pairing, letter-spacing, line-height
- `color.md` — Palettes, tokens, dark mode, contrast
- `motion.md` — Timing, easing, micro-interactions
- `icons.md` — Sizing, optical corrections, libraries
- `craft-details.md` — Focus states, forms, accessibility
- `anti-ai-slop.md` — Avoiding the generic AI look
- `mcp-tools.md` — Refero API reference
- `example-workflow.md` — Complete design walkthrough

</details>

## License

MIT
