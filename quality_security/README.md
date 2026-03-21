# Quality & Security

Skills for testing, security, compliance, and code quality.

## Skills

| Skill | Command | Description |
|-------|---------|-------------|
| Test Engineer | `test-engineer` | Test strategies, coverage, comprehensive test writing |
| Security Auditor | `security-auditor` | OWASP Top 10, vulnerability identification, secure coding |
| API Security Specialist | `api-security-specialist` | OWASP API Security 2023, OAuth 2.1, rate limiting, GraphQL security |
| Compliance Officer | `compliance-officer` | SOC2, HIPAA, GDPR, PCI-DSS, ISO 27001 |
| Incident Response | `incident-response-specialist` | Security incidents, breach protocols, forensics, NIST CSF |
| Code Reviewer | `code-reviewer` | Quality, consistency, security vulnerabilities, pattern adherence |
| QA Enforcer | `qa-enforcer` | Ruthless database-agnostic QA: discovers backend, executes real CRUD, hunts edge cases, audits workflows, audits env vars (.env + deployment platform), grades modules |
| QA Enforcer All | `/qa-enforcer-all` | Full sweep — tests every module in priority order using parallel agent teams, produces master report |

## When to Use

- **test-engineer** — Writing tests, planning test strategy, improving coverage
- **security-auditor** — Security review of code, checking for vulnerabilities
- **api-security-specialist** — API auth design, rate limiting, webhook security, CORS
- **compliance-officer** — Regulatory compliance questions, data handling, privacy
- **incident-response-specialist** — Security breach, incident playbook, forensics
- **code-reviewer** — PR review, code quality feedback, pattern consistency
- **qa-enforcer** — Verify everything actually works via execution, not just code reading. Find bugs, test CRUD, audit workflow docs vs code, audit env vars and deployment config

## Usage Examples

```
# test-engineer — argument-hint: [component] [test-type: unit|integration|e2e]
Skill({ skill: 'test-engineer', args: 'auth unit' })
Skill({ skill: 'test-engineer', args: 'booking-flow e2e' })
Skill({ skill: 'test-engineer', args: 'Plan test strategy for the booking module' })

# security-auditor
Skill({ skill: 'security-auditor', args: 'Audit the auth middleware' })

# api-security-specialist
Skill({ skill: 'api-security-specialist', args: 'Review webhook signature verification' })

# compliance-officer
Skill({ skill: 'compliance-officer', args: 'GDPR audit for user data handling' })

# incident-response-specialist
Skill({ skill: 'incident-response-specialist', args: 'API keys exposed in git history' })

# code-reviewer
Skill({ skill: 'code-reviewer', args: 'Review the pricing resolver changes' })

# qa-enforcer — argument-hint: [module-or-path] [--crud-only|--schema-only|--workflow-only]
Skill({ skill: 'qa-enforcer', args: 'auth' })
Skill({ skill: 'qa-enforcer', args: 'billing --crud-only' })
Skill({ skill: 'qa-enforcer', args: 'projects --workflow-only' })
/qa-enforcer billing
/qa-enforcer C:/Users/nmadd/desktop/vs_code/cojo
/qa-enforcer auth --env-only
/qa-enforcer-all  # full sweep across all modules
```
