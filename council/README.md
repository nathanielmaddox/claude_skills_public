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

## Critical Rules (Learned from Failures)

1. **NO ASSUMPTIONS** — Council members research independently. The arbiter provides the QUESTION and FILE PATHS, never pre-digested conclusions.
2. **ECOSYSTEM-WIDE RESEARCH** — For Otesse, every member must read ALL related projects (otesse-app, otesse_erp, otesse_portal, er_documentation). Evaluating one project without understanding the others produces garbage.
3. **READ CLAUDE.md FIRST** — Every project has a CLAUDE.md that defines its scope and boundaries. Read it before forming any opinion. Don't critique a project for missing features that belong to another project.
4. **DEBATE, DON'T RUBBER-STAMP** — The arbiter presents the council's debate to the user. The arbiter does NOT present its own opinion disguised as a verdict.

## Otesse Council History
- Portal Multi-View: INVALID (2026-03-18) — arbiter fed assumptions, council didn't research independently. Pitfalls logged across all 5 skills.
- Booking Rules: Grade C+, 3-phase plan (see `booking-rules-council-verdict.md`)
- Industry Types: Dynamic feature verdict (see `industry-types-dynamic.md`)
- Pricing UX: Grade D+ (see `pricing-ux-audit.md`)
- Integrations/Workflows UX: Grade C- (see `integrations-workflows-ux-audit.md`)
