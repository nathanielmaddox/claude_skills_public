# Claude Skills — Table of Contents

**Total Skills:** 91
**Categories:** 19
**Location:** `C:\Users\nmadd\desktop\vs_code\claude_skills`

## How to Use

Invoke any skill in Claude Code:
```
Skill({ skill: 'skill-name' })
Skill({ skill: 'skill-name', args: 'optional context' })
```

## Quick Reference — All Skills by Category

| # | Category | Folder | Skills | Key Use Cases |
|---|----------|--------|--------|---------------|
| 1 | [Strategic & Planning](strategic_planning/README.md) | `strategic_planning/` | 3 | Feature breakdown, product strategy, project kickoff |
| 2 | [Design & UX](design_ux/README.md) | `design_ux/` | 9 | UI reviews, accessibility, landing pages, dashboards, mobile, booking flows |
| 3 | [Architecture & Engineering](architecture_engineering/README.md) | `architecture_engineering/` | 11 | System design, APIs, performance, cloud, monorepos, error handling |
| 4 | [AI & Agents](ai_agents/README.md) | `ai_agents/` | 4 | Agent building, LLM ops, prompt engineering, Claude API |
| 5 | [Quality & Security](quality_security/README.md) | `quality_security/` | 9 | Testing, security audits, compliance, code review, QA, frontend checks |
| 6 | [Error Fixing](error_fixing/README.md) | `error_fixing/` | 10 | API, build, Convex, DB, dependency, ESLint, hydration, test, TS errors |
| 7 | [Debugging](debugging/README.md) | `debugging/` | 1 | Systematic root-cause analysis |
| 8 | [Data & Analytics](data_analytics/README.md) | `data_analytics/` | 3 | Data modeling, event tracking, observability |
| 9 | [Business & Growth](business_growth/README.md) | `business_growth/` | 5 | Growth, CRO, sales, customer success, finance |
| 10 | [SEO & Content](seo_content/README.md) | `seo_content/` | 3 | Content strategy, link building, technical SEO |
| 11 | [Marketing](marketing/README.md) | `marketing/` | 1 | Email campaigns, automation, deliverability |
| 12 | [Deployment & DevOps](deployment_devops/README.md) | `deployment_devops/` | 7 | Deploy, preflight, Vercel, GitHub Actions, caching, DR, releases |
| 13 | [Database & Backend](database_backend/README.md) | `database_backend/` | 3 | Supabase, Convex architecture, auth flows |
| 14 | [Internationalization](internationalization/README.md) | `internationalization/` | 1 | RTL, CLDR, locale management |
| 15 | [Documentation](documentation/README.md) | `documentation/` | 1 | Technical writing, SOPs, docs-as-code |
| 16 | [Format Compatibility](format_compatibility/README.md) | `format_compatibility/` | 4 | Audio, font, image, video format issues |
| 17 | [Building](building/README.md) | `building/` | 2 | Form builder, UI component builder |
| 18 | [Council](council/README.md) | `council/` | 5 | Multi-perspective review system |
| 19 | [Workflow & Utilities](workflow_utilities/README.md) | `workflow_utilities/` | 14 | Deploy, preflight, simplify, loop, save progress, team, autonomous-cycle, config |

## Skill Activation Cheat Sheet

| You Want To... | Use This Skill |
|----------------|---------------|
| Plan a feature | `product-manager` |
| Start a new project | `project-inception` |
| Review UI/UX | `ui-ux-designer` |
| Audit accessibility | `accessibility-auditor` |
| Design an API | `api-designer` |
| Fix a build error | `build-error-fixer` |
| Fix TypeScript errors | `typescript-error-fixer` |
| Fix hydration mismatch | `hydration-error-fixer` |
| Debug a tricky bug | `bug-debugger` |
| Security audit | `security-auditor` |
| Write tests | `test-engineer` |
| Ruthlessly verify everything works | `qa-enforcer` |
| Review code | `code-reviewer` |
| Optimize performance | `performance-engineer` |
| Deploy to Vercel | `vercel-deployment` |
| Set up CI/CD | `github-actions-builder` |
| Design a database | `supabase-architect` or `convex-architect` |
| Build a form | `form-builder` |
| Build a UI component | `ui-component-builder` |
| Get multi-perspective review | `council-arbiter` |
| Write copy/microcopy | `copywriter` |
| Optimize conversions | `conversion-rate-optimizer` |
| Set up analytics | `analytics-engineer` |
| Build an AI agent | `ai-agent-builder` |
| Design auth flow | `auth-flow-designer` |
| Design a booking/quote flow | `booking-flow-designer` |
| Fix Convex errors | `convex-error-fixer` |
| Check frontend before deploy | `check-frontend` |
| Monitor frontend health | `frontend-monitor` |
| Pre-flight checks | `preflight` |
| Pre-flight build validation | `preflight-build` |
| Refactor/clean up code | `refactor-editor` |
| Simplify/clean up code | `simplify` |
| Deploy to production | `deploy` |
| Save work before context limit | `save-progress` |
| Run task with agent team | `team` |
| Poll/check something repeatedly | `loop` |
| Configure Claude Code settings | `update-config` |
| Customize keybindings | `keybindings-help` |

## Decision Tree

```
New Task Received
        │
        ▼
  Can a SKILL help? ──YES──▶ Skill({ skill: 'name' })
        │
        NO
        │
        ▼
  Can an AGENT help? ──YES──▶ Agent tool (Explore, Plan, etc.)
        │
        NO
        │
        ▼
  Do it directly
```

## Agents (Task Executors)

**Location:** `agents/`
**Total:** 29 specialized agents

| # | Agent | File | Purpose |
|---|-------|------|---------|
| 1 | Accessibility Auditor | `accessibility-auditor.md` | WCAG compliance checks |
| 2 | API Endpoint Builder | `api-endpoint-builder.md` | Build API routes |
| 3 | Bug Debugger | `bug-debugger.md` | Systematic debugging |
| 4 | Code Reviewer | `code-reviewer.md` | Code quality review |
| 5 | Database Schema Designer | `database-schema-designer.md` | Schema design |
| 6 | Documentation Writer | `documentation-writer.md` | Write docs |
| 7 | Form Builder | `form-builder.md` | Build forms |
| 8 | Git Workflow Manager | `git-workflow-manager.md` | Git operations |
| 9 | Master Orchestrator | `master-orchestrator.md` | Multi-agent coordination |
| 10 | Migration Specialist | `migration-specialist.md` | Data/schema migrations |
| 11 | Performance Optimizer | `performance-optimizer.md` | Performance tuning |
| 12 | QA Coverage Analyzer | `qa-coverage-analyzer.md` | Test coverage analysis |
| 13 | QA Feature Validator | `qa-feature-validator.md` | Feature validation |
| 14 | ReactFlow Specialist | `reactflow-specialist.md` | Node-based UIs |
| 15 | Refactoring Specialist | `refactoring-specialist.md` | Code refactoring |
| 16 | SEO Specialist | `seo-specialist.md` | SEO optimization |
| 17 | State Management Expert | `state-management-expert.md` | State architecture |
| 18 | Styling Expert | `styling-expert.md` | CSS/Tailwind styling |
| 19 | Supabase Auth Integrator | `supabase-auth-integrator.md` | Supabase auth setup |
| 20 | Supabase Migration Manager | `supabase-migration-manager.md` | Supabase migrations |
| 21 | Supabase Realtime Builder | `supabase-realtime-builder.md` | Realtime subscriptions |
| 22 | Supabase RLS Designer | `supabase-rls-designer.md` | Row-level security |
| 23 | Test Data Generator | `test-data-generator.md` | Generate test fixtures |
| 24 | Test E2E Writer | `test-e2e-writer.md` | End-to-end tests |
| 25 | Test Integration Writer | `test-integration-writer.md` | Integration tests |
| 26 | Test Unit Writer | `test-unit-writer.md` | Unit tests |
| 27 | Type Generator | `type-generator.md` | TypeScript types |
| 28 | UI Component Builder | `ui-component-builder.md` | Build UI components |
| 29 | Vercel Specialist | `vercel-specialist.md` | Vercel deployment |

## Slash Commands

| Command | Description |
|---------|-------------|
| `/qa-enforcer [module]` | Run QA on a specific module |
| `/qa-enforcer-all` | Full sweep across all modules |
| `/deploy` | Commit, push, deploy to Vercel |
| `/save-progress` | Persist work before context limit |
| `/team [task]` | Run task with coordinated agent team |
