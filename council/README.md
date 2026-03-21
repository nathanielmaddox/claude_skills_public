# Council

Multi-perspective review system. The Council provides different viewpoints on decisions, designs, and architecture.

## Skills

| Skill | Command | Role | Perspective |
|-------|---------|------|-------------|
| Council Arbiter | `council-arbiter` | The Judge | Spawns all council members, weighs arguments, decides path forward |
| Council Critic | `council-critic` | The Opponent | Adversarial auditor, benchmarks against Airbnb/Stripe/Linear/Notion |
| Council Advocate | `council-advocate` | The Defender | Argues for shipping, defends working code, finds pragmatic paths |
| Council User Voice | `council-user-voice` | The Customer | Simulates first-time user, documents confusion and stuck points |
| Council Architect | `council-architect` | The Long-Game | Evaluates tech debt, scalability, 6-month consequences |

## How It Works

1. **Full Council** — Use `council-arbiter` to spawn all 4 members as a team
2. **Individual** — Use any single council member for focused feedback
3. **Decision Modes** (arbiter): majority, least-resistance, highest-impact, risk-weighted, user-wins, override

## When to Use

| Situation | Use |
|-----------|-----|
| Major architecture decision | `council-arbiter` (full council) |
| "Is this good enough to ship?" | `council-advocate` |
| "What's wrong with this?" | `council-critic` |
| "Would a user understand this?" | `council-user-voice` |
| "What happens at scale?" | `council-architect` |
| Design review, UX audit | `council-critic` or `council-arbiter` |

## Usage Examples

```
Skill({ skill: 'council-arbiter', args: 'Review the booking flow redesign' })
Skill({ skill: 'council-critic', args: 'Audit the pricing page UX' })
Skill({ skill: 'council-user-voice', args: 'Test the onboarding flow as a new user' })
```

## Safeguards (Self-Corrected After Portal Review)

The council's Portal Multi-View review (2026-03-18) produced a flawed verdict because the arbiter pre-digested conclusions instead of letting members research. The council self-corrected, adding 3 safeguards that prevent the same mistakes:

1. **Independent Research** — The arbiter provides questions and file paths, never conclusions. Each council member forms its own opinion from primary sources.
2. **Ecosystem-Wide Scope** — All related projects must be researched (not just the one under review). For Otesse, every member reads otesse-app, otesse_erp, otesse_portal, and er_documentation before forming any opinion.
3. **Debate Over Decree** — The arbiter presents the council's debate to the user, not its own plan. Read each project's CLAUDE.md first to understand scope boundaries.

## How the Council Self-Improves

- Each council member has a `pitfalls.md` that captures mistakes from past reviews.
- The arbiter reads all pitfalls BEFORE every invocation, so known failure modes are actively avoided.
- Failed verdicts become prevention checklists — the worse the failure, the stronger the safeguard.

## Otesse Council History

- Portal Multi-View (2026-03-18) — Triggered the 3 safeguards above. Pitfalls logged across all 5 skills. Re-reviewed successfully as v2.
- Booking Rules: Grade C+, 3-phase plan (see `booking-rules-council-verdict.md`)
- Industry Types: Dynamic feature verdict (see `industry-types-dynamic.md`)
- Pricing UX: Grade D+ (see `pricing-ux-audit.md`)
- Integrations/Workflows UX: Grade C- (see `integrations-workflows-ux-audit.md`)
