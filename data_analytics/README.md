# Data & Analytics

Skills for data modeling, analytics implementation, and observability.

## Skills

| Skill | Command | Description |
|-------|---------|-------------|
| Data Strategist | `data-strategist` | Kimball dimensional modeling, dbt, modern data stack, semantic layers |
| Analytics Engineer | `analytics-engineer` | Event tracking, PostHog/Mixpanel/Amplitude/GA4, dashboards, funnels |
| Observability Architect | `observability-architect` | Enterprise monitoring, SLO dashboards, alerting, OpenTelemetry (Google SRE) |

## When to Use

- **data-strategist** — Data warehouse design, dbt transformations, data modeling
- **analytics-engineer** — Setting up event tracking, product analytics, cohort/funnel analysis
- **observability-architect** — Monitoring setup, alerting strategy, SLOs, distributed tracing

## Usage Examples

```
Skill({ skill: 'analytics-engineer', args: 'Design event tracking for the booking flow' })
Skill({ skill: 'analytics-engineer', args: 'Set up funnel analysis for signup-to-activation' })
Skill({ skill: 'data-strategist', args: 'Model the pricing data for analytics queries' })
Skill({ skill: 'data-strategist', args: 'Design a star schema for the invoicing domain' })
Skill({ skill: 'observability-architect', args: 'Set up alerting for API latency' })
Skill({ skill: 'observability-architect', args: 'Define SLOs for the booking service' })
```

## Otesse Context
- Analytics module: 9 views + PostHog integration (see `analytics-reporting-modules.md`)
- Reports module: 21 views + Convex backend
