# Deployment & DevOps

Skills for deployment, CI/CD, caching, disaster recovery, and release management.

## Skills

| Skill | Command | Description |
|-------|---------|-------------|
| **Deploy** | `/deploy` | Slash command: commit → push → `npx vercel --prod --scope hello-9162s-projects` |
| **Preflight** | `/preflight` | Standalone lint + type-check + build validation (does NOT deploy) |
| Vercel Deployment | `vercel-deployment` | Next.js config, Edge/Serverless, caching, performance, troubleshooting |
| GitHub Actions Builder | `github-actions-builder` | CI/CD pipelines, test automation, matrix builds, caching, workflows |
| Caching Strategist | `caching-strategist` | Redis, CDN, ISR/SSG/SSR, browser caching, service workers, invalidation |
| Disaster Recovery | `disaster-recovery-planner` | RTO/RPO planning, DR testing, failover (ISO 22301, NIST) |
| Release Manager | `release-manager` | Release trains, feature flags, staged rollouts, change advisory (ITIL, SAFe) |

## When to Use

- **`/deploy`** — Full deploy pipeline: commit → push → Vercel CLI deploy. Does NOT run preflight automatically — run `/preflight` separately if needed
- **`/preflight`** — Standalone pre-deploy validation (lint, types, build). Does NOT deploy
- **vercel-deployment** — Vercel deploy issues, Edge vs Serverless decisions, caching config
- **github-actions-builder** — Setting up CI/CD, optimizing build times, test automation
- **caching-strategist** — Caching strategy decisions, Redis setup, CDN configuration
- **disaster-recovery-planner** — DR planning, backup strategies, failover design
- **release-manager** — Release process, feature flags, staged rollouts

## Deploy Context

- **Vercel scope:** `--scope hello-9162s-projects` (ALWAYS required — without it deploys get BLOCKED)
- **Git author:** `cocoking` / `hello@otesse.com` (wrong author = blocked deploy)
- **Multiple projects:** Deploy sequentially, not in parallel (Hobby plan blocks concurrent builds)
- **DS fallback:** Use prebuilt deploy when remote build fails (see `feedback_ds_deploy_prebuilt`)

## Usage Examples

```
# vercel-deployment
Skill({ skill: 'vercel-deployment', args: 'Deploy otesse_erp to production' })

# github-actions-builder — argument-hint: [workflow-type: ci|cd|release|test]
Skill({ skill: 'github-actions-builder', args: 'ci' })
Skill({ skill: 'github-actions-builder', args: 'release' })
Skill({ skill: 'github-actions-builder', args: 'Set up CI for the monorepo' })

# caching-strategist
Skill({ skill: 'caching-strategist', args: 'Redis caching strategy for API responses' })

# disaster-recovery-planner
Skill({ skill: 'disaster-recovery-planner', args: 'Design DR plan for multi-region SaaS' })

# release-manager
Skill({ skill: 'release-manager', args: 'Set up feature flags for staged rollout' })
```
