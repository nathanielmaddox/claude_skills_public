# Workflow & Utilities

Meta-skills for Claude Code configuration, workflow automation, and session management.

## Skills

| Skill | Command | Description |
|-------|---------|-------------|
| Simplify | `simplify` | Review changed code for reuse, quality, and efficiency — then fix issues found |
| Loop | `loop` | Run a prompt or slash command on a recurring interval (e.g., `/loop 5m /foo`, defaults to 10m) |
| Frontend Monitor | `frontend-monitor` | Frontend monitoring |
| Save Progress | `save-progress` | Persist all progress so nothing is lost if the session ends unexpectedly |
| Deploy | `deploy` | Commit all changes, push to main, and deploy to Vercel using the CLI |
| Team | `team` | Execute a task using an agent team with coordinated agents |
| Update Config | `update-config` | Configure Claude Code settings, hooks, permissions, env vars |
| Keybindings Help | `keybindings-help` | Customize keyboard shortcuts, rebind keys, chord bindings |

## When to Use

- **simplify** — After writing code, review for quality and simplification opportunities
- **loop** — Polling a deploy status, recurring checks, babysitting PRs (`/loop 5m /foo`)
- **frontend-monitor** — Monitoring frontend behavior
- **save-progress** — Before context gets high, or at logical stopping points to prevent work loss
- **deploy** — Ready to ship: commits, pushes, and deploys to Vercel in one command
- **team** — Complex tasks that benefit from multiple coordinated agents working together
- **update-config** — Setting up hooks ("when X happens, do Y"), adding permissions, env vars
- **keybindings-help** — Rebinding keys, adding chord shortcuts, customizing submit key

## Usage Examples

```
Skill({ skill: 'simplify' })
Skill({ skill: 'loop', args: '5m check deploy status' })
Skill({ skill: 'frontend-monitor' })
Skill({ skill: 'save-progress' })
Skill({ skill: 'deploy' })
Skill({ skill: 'team', args: 'Build the customer management module' })
Skill({ skill: 'update-config', args: 'Add a hook to run lint on save' })
Skill({ skill: 'keybindings-help', args: 'Rebind ctrl+s to save and format' })
```

## Notes

- **deploy** uses Vercel account `hello@otesse.com` — git email must match
- **team** is preferred over parallel background agents (per `feedback_use_agent_teams`)
- **save-progress** should be used proactively at 60%+ context usage
