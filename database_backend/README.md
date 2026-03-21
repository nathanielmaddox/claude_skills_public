# Database & Backend

Skills for database design, backend architecture, and authentication.

## Skills

| Skill | Command | Description |
|-------|---------|-------------|
| Supabase Architect | `supabase-architect` | PostgreSQL schema, RLS, auth, real-time, edge functions, pgvector |
| Convex Architect | `convex-architect` | Reactive DB schema, queries/mutations/actions, real-time sync, Clerk/Auth0 |
| Auth Flow Designer | `auth-flow-designer` | OAuth 2.1/OIDC, passkeys/WebAuthn, session vs JWT, multi-tenant auth |

## When to Use

- **supabase-architect** — PostgreSQL schema design, RLS policies, real-time subscriptions
- **convex-architect** — Convex schema, reactive queries, file storage, scheduled functions
- **auth-flow-designer** — Authentication architecture, OAuth flows, session management

## Otesse Context

**CRITICAL:** Otesse uses Convex, NOT Prisma/Neon.
- All new features MUST use Convex
- Deploy: `npx convex dev --once --typecheck=disable`
- Filenames in `convex/` CANNOT have hyphens — use underscores

## Usage Examples

```
Skill({ skill: 'convex-architect', args: 'Design schema for customer management' })
Skill({ skill: 'auth-flow-designer', args: 'Add multi-tenant auth to the ERP' })
```
