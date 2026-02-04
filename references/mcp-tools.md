# Refero MCP Tools Reference

Refero has 5 tools. This document covers detailed usage for each.

## `search_screens` — Visual Exploration

**Best for:** Single screens, specific UI patterns, visual inspiration.

**Parameters:**
- `query` — semantic search (required)
- `platform` — `"ios"` | `"web"` | `"all"` (default: all)
- `limit` — results per page, up to 50 (default: 20)
- `offset` — for pagination

**Query examples (simple):**
```
"pricing page"
"forgot password"  
"skeleton loading"
"data table with filters"
"headspace subscription"
```

**Query examples (complex — combine freely):**
```
"iOS paywall modal with annual/monthly toggle and dark mode"
"onboarding welcome screen with illustration and progress indicator"
"error state for email input with inline validation message"
"product analytics dashboard with activity heatmap"
```

**Pro tips:**
- Use `platform: "ios"` or `platform: "web"` for focused results
- Start broad, then narrow: `"onboarding"` → `"fintech onboarding"` → `"KYC verification"`
- Mix query types: screen type + company + style = `"Notion settings dark mode"`

---

## `search_flows` — Journey Understanding

**Best for:** Multi-step processes, user journeys, flow logic.

**Query examples:**
```
"signing up"
"onboarding airbnb"
"canceling subscription"
"checkout flow with promo code"
"password reset flow with 2FA"
```

**When to use flows vs screens:**
- **Screens** when you need visual inspiration for a single screen
- **Flows** when you need to understand the full journey (onboarding, checkout, etc.)

---

## `get_screen` — Deep Dive on Specific Screen

**Best for:** Detailed analysis after finding promising examples in search.

**Key parameters:**

**`image_size`** — choose wisely:
| Value | When to use | Size |
|-------|-------------|------|
| `"none"` | Default. Text descriptions are usually enough | 0 KB |
| `"thumbnail"` | Need to visually evaluate layout | ~30-100 KB |
| `"full"` | Need fine UI details (icons, typography, exact spacing) | ~400KB-2MB |

**`include_similar: true`** — get similar screens from other apps. Excellent for expanding research and seeing alternative approaches.

**`similar_limit`** — how many similar screens (default: 4, max: 20)

**Batch requests:** Use `screen_ids: [...]` to fetch multiple screens at once.

---

## `get_flow` — Complete Journey Analysis

**Best for:** Understanding end-to-end user experience after finding a flow in search.

Returns:
- All screens with full descriptions
- For each step: goal, action, system response
- User problem description
- Related search queries

**Batch requests:** Use `flow_ids: [...]` for multiple flows.

---

## `get_design_guidance` — AI-Powered Best Practices

**Best for:** When you're stuck, starting fresh, or need a "second opinion." Takes ~15-30 seconds.

**How it works:**
1. You give context (queries) and ask a question.
2. The server analyzes hundreds of screens.
3. It returns a structured guide: what's standard, what's unique, and what to avoid.

**Example:**
```
queries: [
  "paywall",
  "subscription pricing screen", 
  "premium upgrade modal",
  "free trial"
]
question: "How to create a converting paywall for a photo app?"
```

**Response includes:**
- **must_do** — required elements (conventions, requirements)
- **consider** — ideas for uniqueness (who does it, why it works)
- **avoid** — anti-patterns (what to avoid and why)
- **examples** — specific screens to study

---

## Tips for Better Results

**Query formulation:**
- If 0 results → broaden query, remove specific words
- Too many irrelevant results → add context (platform, company, style)
- Combine multiple aspects: `"fintech onboarding ios"` vs just `"onboarding"`

**Efficiency:**
- Use batch requests (`screen_ids`, `flow_ids`) when fetching multiple items
- Start with `image_size: "none"` — descriptions are usually sufficient
- Use `include_similar: true` to discover related approaches

**Platform filter:**
- Use `platform: "ios"` for mobile app patterns
- Use `platform: "web"` for web app/site patterns
- Use `platform: "all"` when exploring broadly
