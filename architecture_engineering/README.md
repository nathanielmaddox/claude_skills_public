# Architecture & Engineering

Skills for system design, API design, and engineering best practices.

## Skills

| Skill | Command | Description |
|-------|---------|-------------|
| System Architect | `system-architect` | Scalable distributed systems (Martin Fowler patterns) |
| API Designer | `api-designer` | REST/GraphQL/tRPC, versioning, documentation, DX |
| Mobile Architect | `mobile-architect` | iOS, Android, React Native, Flutter platform selection |
| DevOps Engineer | `devops-engineer` | Infrastructure, deployment, monitoring (Google SRE) |
| Performance Engineer | `performance-engineer` | Core Web Vitals, frontend/backend optimization |
| Cloud Architect | `cloud-architect` | Multi-cloud, hybrid, FinOps, landing zones (Well-Architected) |
| Enterprise Integration | `enterprise-integration-architect` | ERP integration, B2B protocols, SAP/Oracle/Salesforce (TOGAF) |
| Next.js Specialist | `nextjs-specialist` | App Router, Server/Client Components, caching, middleware |
| TypeScript Specialist | `typescript-specialist` | Advanced types, generics, conditional types, inference |
| Monorepo Manager | `monorepo-manager` | Turborepo, pnpm workspaces, shared packages, build optimization |
| Error Handler Architect | `error-handler-architect` | Error boundaries, global handling, structured logging, graceful degradation |

## When to Use

- **system-architect** — Designing a new system, evaluating trade-offs, scalability concerns
- **api-designer** — Designing REST/GraphQL APIs, versioning strategy, documentation
- **performance-engineer** — Page load slow, Core Web Vitals failing, bundle size issues
- **nextjs-specialist** — App Router questions, Server vs Client component decisions, caching
- **typescript-specialist** — Complex type issues, generic patterns, type inference problems
- **monorepo-manager** — Setting up or optimizing a monorepo, shared package issues

## Usage Examples

```
# system-architect
Skill({ skill: 'system-architect', args: 'Design the notification delivery system' })

# api-designer
Skill({ skill: 'api-designer', args: 'Design REST API for customer management' })

# mobile-architect
Skill({ skill: 'mobile-architect', args: 'Evaluate React Native vs Flutter for field service app' })

# devops-engineer
Skill({ skill: 'devops-engineer', args: 'Set up monitoring and alerting for production' })

# performance-engineer
Skill({ skill: 'performance-engineer', args: 'The dashboard loads in 8 seconds' })

# cloud-architect
Skill({ skill: 'cloud-architect', args: 'Multi-region failover strategy for AWS' })

# enterprise-integration-architect
Skill({ skill: 'enterprise-integration-architect', args: 'Connect Salesforce CRM to our booking system' })

# nextjs-specialist
Skill({ skill: 'nextjs-specialist', args: 'Should this be a Server or Client component?' })

# typescript-specialist
Skill({ skill: 'typescript-specialist', args: 'Fix complex generic inference in useForm hook' })

# monorepo-manager
Skill({ skill: 'monorepo-manager', args: 'Optimize Turborepo build pipeline for shared packages' })

# error-handler-architect
Skill({ skill: 'error-handler-architect', args: 'Design error boundary strategy for the dashboard' })
```
