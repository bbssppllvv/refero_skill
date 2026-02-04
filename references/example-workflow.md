# Example Workflow: Fintech Onboarding

A complete walkthrough showing how to apply the Research-First Design methodology.

---

## Phase 0: Discovery

**Questions answered:**

| Question | Answer |
|----------|--------|
| WHAT are we building? | Onboarding flow, iOS, 5-7 screens |
| WHO is this for? | Millennials, first-time investors, moderate tech-savvy |
| WHAT should users accomplish? | Set up account, complete KYC, fund account |
| WHAT feeling should it evoke? | Trustworthy yet modern, approachable |
| WHAT JOB is the user hiring this? | "Get me started without friction" + "Convince me to trust you" |
| WHAT objections might they have? | "Is my money safe?", "Why do you need my SSN?", "How long will this take?" |
| WHAT should they remember tomorrow? | "That was surprisingly easy and I felt safe" |
| ANY constraints? | iOS-first, must include KYC, brand colors exist |

**Design Brief:**
> "Onboarding flow for millennial first-time investors that helps them set up and fund their account while feeling trustworthy yet modern. The user's job: get started without friction while building trust. Main objection: 'Is my money safe?' and 'Why do you need my personal info?'. They should remember: 'That was surprisingly easy.' Constraints: iOS-first, must include KYC."

---

## Phase 1: Research

### Focus Identified

**By Challenge:** Building trust (fintech) + Reducing friction (onboarding)
→ Focus on: security signals, credentials, progressive disclosure, smart defaults

**By Goal:** UX/Flow optimization
→ Focus on: step count, friction points, error handling, save states

### Search Loop Executed

```
1. BROAD: "onboarding fintech" → 45 results, see patterns
2. SPECIFIC: "KYC verification flow" → 28 results, identity patterns
3. COMPANY: "Revolut onboarding" → 12 results, best-in-class
4. COMPANY: "Wise signup" → 15 results, trust patterns
5. ELEMENT: "progress indicator onboarding" → 32 results
6. CROSS-PLATFORM: "fintech onboarding web" → 18 results, fresh ideas
7. ADJACENT: "healthcare onboarding" → 22 results (also needs trust!)
```

**Queries executed:**
- `search_flows("onboarding fintech", platform="ios", limit=25)` → 45 results
- `search_flows("kyc verification", limit=25)` → 28 results
- `search_screens("Revolut", platform="ios", limit=15)` → 12 results
- `search_screens("Wise signup", limit=15)` → 15 results
- `search_screens("progress indicator onboarding", limit=20)` → 32 results
- `search_screens("fintech onboarding", platform="web", limit=20)` → 18 results
- `search_flows("healthcare onboarding", limit=20)` → 22 results

**Total: 172 screens/flows reviewed**

### Deep Dive (get_screen calls)

Called `get_screen` with `include_similar: true` for 8 best finds:
1. Revolut - Welcome sequence (clean, single focus)
2. Wise - KYC explanation screen (trust-building copy)
3. Robinhood - Progress steps (gamified)
4. Mercury - Form design (spacious, professional)
5. Cash App - Verification (casual, fast)
6. Monzo - Security explanation (transparent)
7. One Medical - Document upload (healthcare, trust patterns)
8. Plaid - Bank connection (third-party trust)

### Three Lenses Applied

**Lens A: Structure**
- All use single focus per screen
- Progress indication: 60% use subtle bar, 30% numbered steps, 10% hidden
- KYC typically 3-5 screens: info → document → selfie → processing
- Average total flow: 6-8 screens before funded

**Lens B: Visual Craft**
- Typography: Large headlines (28-32pt), generous line height
- Color: Muted backgrounds, accent for CTAs only
- Spacing: Very generous (24-32px between elements)
- Details: Soft shadows, large radii (12-16px), subtle gradients
- Vibe: Clean, spacious, confidence-inspiring

**Lens C: Conversion & Soul**
- Hook: "Invest in minutes" / "Start with $1" / "No hidden fees"
- Objections: Explain WHY before asking sensitive info (Wise does brilliantly)
- Trust: Security badges, encryption mentions, "Bank-level security"
- Unique: Revolut's minimal aesthetic, Cash App's casual tone
- Microcopy: "This helps us protect your account" > "Required by law"

**For Flows:**
- Step count: 6-8 screens average
- Decision points: Plan selection, funding amount
- Friction reducers: Camera for documents, autofill, skip options
- Save states: All allow resume if interrupted
- Error handling: Inline validation, clear retry paths

### Research Summary

```
📊 RESEARCH SUMMARY
────────────────────────────────────────
Queries executed: 7 (172 total results)
Screens analyzed: 52 total (8 full with get_screen, 44 search descriptions)

STRUCTURE PATTERNS:
  • Single focus per screen (universal)
  • Progress bar at top, subtle (60% of references)
  • KYC: explain benefit before asking
  • 6-8 screens total before funded

🎨 VISUAL INSPIRATION:
  • Typography: Large headlines (28-32pt), generous leading
  • Color: Muted backgrounds, single accent for CTAs
  • Spacing: Very generous (24-32px gaps)
  • Details: Soft shadows, 12-16px radii
  • Vibe: Clean, spacious, confidence-inspiring

✨ CLEVER FINDS (things to steal):
  • Wise — "This helps protect your account" before SSN (reframes requirement as benefit)
  • Revolut — Single word per screen for key moments ("Welcome", "Almost there")
  • Cash App — "$1 to start" removes mental barrier
  • Monzo — "Your money is protected up to £85,000" specific = trustworthy
  • One Medical — Document upload with camera guides (reduces retakes)
  • Mercury — "Takes about 3 minutes" sets expectation upfront

🧠 CONVERSION TACTICS:
  • Trust: Specific numbers ("256-bit encryption", "FDIC insured up to $250K")
  • Friction: Explain time upfront, show progress, allow skip where possible
  • Social proof: "Join 2M+ investors" early in flow

❓ STILL NEED: Nothing critical — good coverage
────────────────────────────────────────
```

---

## Phase 2: Analyze

### Pattern Table

| Aspect | Revolut | Wise | Robinhood | Mercury | **Our Choice** |
|--------|---------|------|-----------|---------|----------------|
| Progress | Hidden | Subtle bar | Numbered | Dots | **Subtle bar** (clean, non-intrusive) |
| Tone | Minimal | Friendly | Gamified | Professional | **Friendly** (trust + approachable) |
| Forms | Dense | Spacious | Minimal | Spacious | **Spacious** (premium, less anxiety) |
| KYC framing | Required | Beneficial | Quick | Legal | **Beneficial** (Wise's approach) |
| CTA style | Primary | Primary | Bold | Subtle | **Primary** (clear action) |
| Time indication | None | Upfront | None | Upfront | **Upfront** (Mercury's "3 minutes") |

### Steal List (Required)

| Source | What | Why It Works | How I'll Use It |
|--------|------|--------------|-----------------|
| Wise | "This helps protect your account" before SSN | Reframes requirement as benefit, reduces resistance | Same placement before sensitive fields |
| Mercury | "Takes about 3 minutes" on first screen | Sets expectation, reduces anxiety about unknown | Opening screen, honest time estimate |
| Revolut | Single-word hero screens ("Welcome") | Creates breathing room, feels premium | Key transition moments |
| Monzo | "Protected up to £85,000" | Specific number = credible, not vague "secure" | Footer during KYC, with actual FDIC amount |
| Cash App | "$1 to start" | Removes mental barrier to funding | Funding screen, lowest possible amount shown |
| One Medical | Camera guides for document | Reduces failed uploads, feels helpful | Document capture with alignment overlay |

**Categories covered:**
- ✅ Trust signal (Monzo's specific protection amount)
- ✅ Objection killer (Wise's "helps protect" framing)
- ✅ Friction reducer (Mercury's time estimate, Cash App's low barrier)
- ✅ Visual treatment (Revolut's breathing room)
- ✅ Micro-detail (One Medical's camera guides)
- ✅ Memorable element (Single-word hero moments)

---

## Phase 3: Design

### Persuasion Layer (Filled Before Code)

| Element | Our Answer | Implementation |
|---------|------------|----------------|
| **Hook** (first 3 sec) | "Start investing in 3 minutes" | Hero headline + time indicator |
| **Story arc** | Welcome → Trust → Setup → Verify → Fund → Success | Screen sequence |
| **Objection killers** | 1. "Why SSN?" → "Protects your account" 2. "Is it safe?" → "FDIC $250K" 3. "How long?" → "3 minutes" | Inline copy at friction points |
| **Trust signals** | FDIC insurance specific, encryption mention, "2M+ users" | KYC screens + footer |
| **Urgency/Scarcity** | N/A — not appropriate for trust-focused fintech | Skip |
| **The memorable thing** | Single-word breathing moments + surprisingly easy completion | "Welcome" / "Almost there" / "You're in" screens |

### Typography System

- Display: SF Pro Display, 32px, -0.02em tracking
- H1: SF Pro, 24px, -0.01em tracking
- Body: SF Pro, 17px (iOS default)
- Caption: SF Pro, 13px, +0.01em tracking
- Leading: 1.2 for headlines, 1.5 for body

### Color Palette

- Background: #FAFAFA (warm white, not stark)
- Text primary: #1A1A1A
- Text secondary: #666666
- Accent: Brand green (not default blue!)
- Success: #22C55E
- Error: #EF4444

### Spacing System

- Base: 8px
- Scale: 8, 16, 24, 32, 48, 64
- Section gap: 48px
- Element gap: 16px
- Form field gap: 24px

### The Soul (20%)

- **Bold visual choice:** Brand green accent, never blue
- **Voice:** Second person, benefit-focused ("Your account is protected" not "We protect accounts")
- **Memorable detail:** Single-word hero screens at transitions
- **Micro-interaction:** Subtle scale on CTA tap (0.98, 90ms)

---

## Phase 4: Implement

### Build Checklist

- [x] Semantic HTML/SwiftUI structure
- [x] Design tokens for all values
- [x] Progress bar component (subtle, top)
- [x] Form fields with inline validation
- [x] Camera overlay for document capture
- [x] Loading states with copy ("Verifying...")
- [x] Error states with clear recovery
- [x] Save state (can resume if interrupted)

### Quality Gate

| Category | Check | Status |
|----------|-------|--------|
| **Functional** | Primary action obvious? Error states? Works on all iOS sizes? | ✅ |
| **Visual** | Squint test passes? Spacing rhythm? Typography intentional? | ✅ |
| **Persuasion** | Hook in 3 sec? 2+ trust signals? Objections addressed? | ✅ |
| **Polish** | No orphaned words? Icons aligned? CTAs consistent? Something memorable? | ✅ |

### Side-by-Side Test

Compared against Revolut, Wise, Mercury:

| Criteria | Score |
|----------|-------|
| Polish (details, alignment) | ✅ Match |
| Clarity (hierarchy, readability) | ✅ Match |
| Uniqueness (memorable elements) | ✅ Exceed (breathing screens + specific trust copy) |
| Usability (obvious actions) | ✅ Match |

**Result:** 4/4 criteria met or exceeded.

---

## Key Takeaways

1. **Research depth matters:** 172 results reviewed, 8 deep dives — found tactics like Wise's objection framing that wouldn't appear in first 10 results

2. **Adjacent industries help:** Healthcare onboarding (One Medical) gave us camera guide idea for documents

3. **Steal List drives decisions:** Every unique element traces back to a specific reference and reason

4. **Specificity builds trust:** "FDIC insured up to $250,000" > "Your money is safe"

5. **The soul is small:** Three things make it memorable — breathing screens, honest time estimate, benefit-framed copy. Not a complete redesign.
