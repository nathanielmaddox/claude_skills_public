# Error Fixing

Specialized agents for diagnosing and fixing specific types of errors. These activate automatically when relevant errors are encountered.

## Skills

| Skill | Command | Fixes |
|-------|---------|-------|
| API Error Fixer | `api-error-fixer` | Fetch failures, CORS, network request problems in Next.js |
| Build Error Fixer | `build-error-fixer` | Next.js build errors, webpack failures, production build issues |
| Database Error Fixer | `database-error-fixer` | Supabase, Prisma, PostgreSQL connection/query/RLS errors |
| Dependency Error Fixer | `dependency-error-fixer` | npm/pnpm dependency conflicts, peer dependency issues |
| ESLint Error Fixer | `eslint-error-fixer` | ESLint errors, warnings, code style issues (runs auto-fix) |
| Hydration Error Fixer | `hydration-error-fixer` | React hydration mismatches, SSR/CSR inconsistencies |
| Test Failure Fixer | `test-failure-fixer` | Jest, Vitest, Playwright, React Testing Library failures |
| TypeScript Error Fixer | `typescript-error-fixer` | TS compilation errors, type mismatches, inference issues |
| Convex Error Fixer | `convex-error-fixer` | Schema validation, query/mutation types, deployment, auth config |

## Error → Skill Quick Lookup

| Error Pattern | Skill to Use |
|---------------|-------------|
| `fetch failed`, `CORS`, `NetworkError` | `api-error-fixer` |
| `Build failed`, `webpack`, `Module not found` | `build-error-fixer` |
| `connection refused`, `RLS`, `query error` | `database-error-fixer` |
| `peer dep`, `ERESOLVE`, `version conflict` | `dependency-error-fixer` |
| `eslint`, `no-unused-vars`, `prettier` | `eslint-error-fixer` |
| `Hydration failed`, `Text content does not match` | `hydration-error-fixer` |
| `Test failed`, `expect(`, `toEqual` | `test-failure-fixer` |
| `TS2322`, `Type '...' is not assignable` | `typescript-error-fixer` |
| `Convex`, `schema validation`, `deployment` | `convex-error-fixer` |

## Usage Examples

```
Skill({ skill: 'build-error-fixer' })
Skill({ skill: 'typescript-error-fixer' })
Skill({ skill: 'hydration-error-fixer' })
```

## Note
Per feedback rule `feedback_use_skills_on_errors`, ALWAYS invoke the relevant error-fixer skill when encountering errors — don't try to fix manually first.
