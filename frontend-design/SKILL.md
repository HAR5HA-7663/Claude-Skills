---
name: frontend-design
description: Master orchestrator for premium frontend design. Combines 29 specialized design skills (Impeccable, Emil Kowalski, Taste Skill) into a unified system for building, reviewing, and refining production-grade UIs. Use when the user asks to build web components, pages, dashboards, landing pages, portfolios, or any frontend interface. Also triggers for design reviews, redesigns, UI audits, animation work, responsive fixes, typography improvements, color refinement, layout adjustments, performance optimization, or any request to make a UI look better, more polished, or more professional. Invocable as /frontend-design with optional arguments: "build", "review", "refine", or a specific sub-skill name.
user-invocable: true
argument-hint: "[build|review|refine|<sub-skill>] [target]"
---

# Frontend Design — Master Orchestrator

Unified design system combining **Impeccable** (21 commands), **Emil Kowalski's Design Engineering**, and **Taste Skill** (7 variants) into a single intelligent workflow.

For the complete skill map with all 29 sub-skills: see [references/skill-map.md](references/skill-map.md).

---

## How This Skill Works

This skill does NOT replace the 29 sub-skills — it **orchestrates** them. Analyze the user's request and invoke the right combination in the right order.

### Decision Matrix

| User Intent | Skills to Invoke (in order) |
|---|---|
| **Build new UI** | `/impeccable` (context) → `design-taste-frontend` (architecture) → `high-end-visual-design` (aesthetics) → `emil-design-eng` (animation) → `/polish` |
| **Review existing UI** | `/audit` (technical) → `/critique` (UX) → report findings |
| **Redesign existing UI** | `/critique` → `redesign-existing-projects` → `/polish` |
| **Fix animations** | `emil-design-eng` (decision framework) → `/animate` |
| **Improve typography** | `/typeset` |
| **Fix colors** | `/colorize` |
| **Fix layout/spacing** | `/arrange` |
| **Make it bolder** | `/bolder` |
| **Tone it down** | `/quieter` |
| **Simplify** | `/distill` |
| **Add delight** | `/delight` → `emil-design-eng` (spring physics) |
| **Go all-out** | `/overdrive` → `high-end-visual-design` |
| **Make responsive** | `/adapt` |
| **Production-ready** | `/harden` → `/optimize` → `/polish` |
| **Pre-launch review** | `/audit` → `/critique` → `/polish` |
| **Plan before building** | `/shape` (discovery interview → design brief) |
| **Fix UX copy** | `/clarify` |
| **Extract components** | `/extract` |
| **Consistency pass** | `/normalize` |
| **Onboarding flow** | `/onboard` |

### Aesthetic Presets

When the project calls for a specific style, load the matching preset:

| Style | Skill |
|---|---|
| Clean editorial (Notion/Linear) | `minimalist-ui` |
| Raw mechanical (Swiss/terminal) | `industrial-brutalist-ui` |
| Premium agency ($150k+) | `high-end-visual-design` |
| Google Stitch compatible | `stitch-design-taste` |

---

## Core Design Principles (Always Active)

These principles from all three skill systems apply to EVERY frontend task:

### Anti-AI-Slop Rules
- **No gradient text** (`background-clip: text` + gradient = banned)
- **No side-stripe borders** (`border-left: 3px+` on cards/alerts = banned)
- **No Inter/Roboto/Arial/Syne** — use distinctive fonts per project
- **No purple/blue AI glow aesthetic** — no neon gradients on dark backgrounds
- **No 3-column identical card grids** — use asymmetric layouts
- **No cards-in-cards** — flatten hierarchy
- **No centered-everything** — left-align with asymmetry
- **No bounce/elastic easing** — use exponential ease-out
- **No `h-screen`** — use `min-h-[100dvh]`
- **No `#000000` or `#ffffff`** — always tint neutrals

### Typography
- Modular type scale with `clamp()` for headings on marketing pages, fixed `rem` for app UIs
- Pair a distinctive display font with a refined body font — never same family for both
- Line length capped at 65-75ch
- Before picking a font: write 3 brand words, reject reflex choices, browse font catalogs, cross-check

### Color
- Use OKLCH, not HSL — perceptually uniform
- Tint neutrals toward brand hue (even 0.005 chroma)
- 60-30-10 rule by visual weight: 60% neutral, 30% secondary, 10% accent
- Theme (light/dark) derived from audience and viewing context, not defaults

### Layout
- 4pt spacing scale with semantic tokens
- `gap` over margins for sibling spacing
- Self-adjusting grid: `repeat(auto-fit, minmax(280px, 1fr))`
- Container queries for components, viewport queries for page layout

### Motion (Emil Kowalski Framework)
1. **Should it animate?** Frequency-based: 100+/day = no animation; occasional = standard; rare = add delight
2. **Purpose?** Spatial consistency, state indication, explanation, feedback, preventing jarring changes
3. **Easing?** Entering/exiting = ease-out; moving = ease-in-out; hover = ease; constant = linear. Always use custom curves.
4. **Speed?** Button press: 100-160ms. Tooltips: 125-200ms. Dropdowns: 150-250ms. Modals: 200-500ms. UI stays under 300ms.
- Never animate from `scale(0)` — start from `scale(0.95)` + `opacity: 0`
- Never use `ease-in` for UI — feels sluggish
- Springs for drag, momentum, interruptible gestures
- Only animate `transform` and `opacity` — never layout properties

### Performance
- Hardware acceleration: animate via `transform`/`opacity` only
- Framer Motion `x`/`y` props are NOT hardware-accelerated — use full `transform` strings
- CSS animations beat JS under load (off main thread)
- Grain/noise filters on fixed `pointer-events-none` pseudo-elements only
- Isolate perpetual animations in their own Client Components (React.memo)

### Technical (React/Next.js)
- Server Components by default; `'use client'` only for interactive leaves
- Check `package.json` before importing ANY 3rd party library
- Tailwind version lock — check v3 vs v4 before writing config
- `min-h-[100dvh]` not `h-screen` for full-height sections
- CSS Grid over flexbox percentage math
- `@phosphor-icons/react` or `@radix-ui/react-icons` — never emoji in code

---

## Invocation Modes

### `/frontend-design build [description]`
Full build flow:
1. Check for `.impeccable.md` design context — if missing, run `/impeccable teach`
2. Load `design-taste-frontend` for architecture decisions
3. Load `high-end-visual-design` for aesthetic direction
4. Apply `emil-design-eng` for animation decisions
5. Apply `full-output-enforcement` for complete code output
6. Run `/polish` before delivering

### `/frontend-design review [target]`
Full review flow:
1. Run `/audit` for technical quality (a11y, performance, responsive, anti-patterns)
2. Run `/critique` for UX quality (hierarchy, cognitive load, emotional resonance)
3. Combine into unified report with prioritized action items

### `/frontend-design refine [target]`
Iterative refinement flow:
1. Identify what's weak (typography? color? layout? motion? copy?)
2. Invoke the specific sub-skill(s) for that weakness
3. Finish with `/polish`

### `/frontend-design [sub-skill] [target]`
Direct pass-through to any sub-skill: `/frontend-design animate hero`, `/frontend-design colorize dashboard`, etc.
