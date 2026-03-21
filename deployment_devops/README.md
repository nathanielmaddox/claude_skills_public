# Deployment & DevOps

Skills for deployment, CI/CD, caching, disaster recovery, and release management.

## Skills

| Skill | Command | Description |
|-------|---------|-------------|
| Vercel Deployment | `vercel-deployment` | Next.js config, Edge/Serverless, caching, performance, troubleshooting |
| GitHub Actions Builder | `github-actions-builder` | CI/CD pipelines, test automation, matrix builds, caching, workflows |
| Caching Strategist | `caching-strategist` | Redis, CDN, ISR/SSG/SSR, browser caching, service workers, invalidation |
| Disaster Recovery | `disaster-recovery-planner` | RTO/RPO planning, DR testing, failover (ISO 22301, NIST) |
| Release Manager | `release-manager` | Release trains, feature flags, staged rollouts, change advisory (ITIL, SAFe) |

## When to Use

- **vercel-deployment** — Vercel deploy issues, Edge vs Serverless decisions, caching config
- **github-actions-builder** — Setting up CI/CD, optimizing build times, test automation
- **caching-strategist** — Caching strategy decisions, Redis setup, CDN configuration
- **disaster-recovery-planner** — DR planning, backup strategies, failover design
- **release-manager** — Release process, feature flags, staged rollouts

## Otesse Deploy Context

- **Vercel account:** hello@otesse.com
- **Git email must match:** `git config user.email "hello@otesse.com"`
- **Always explicit:** `npx vercel --prod` (no auto-deploy assumed)
- **DS fallback:** Use prebuilt deploy when remote build fails (see `feedback_ds_deploy_prebuilt`)

## Usage Examples

```
Skill({ skill: 'vercel-deployment', args: 'Deploy otesse_erp to production' })
Skill({ skill: 'github-actions-builder', args: 'Set up CI for the monorepo' })
```
