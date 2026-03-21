# Debugging

Systematic debugging for complex, hard-to-trace bugs.

## Skills

| Skill | Command | Description |
|-------|---------|-------------|
| Bug Debugger | `bug-debugger` | Structured debugging process: traces root causes, identifies fixes, prevents regressions |

## When to Use

- Bug with unclear root cause
- Issue that spans multiple files/modules
- Intermittent or hard-to-reproduce problems
- When error-fixers don't cover the specific issue

## Usage Examples

```
Skill({ skill: 'bug-debugger', args: 'Drawer opens but shows stale data after switching tabs' })
Skill({ skill: 'bug-debugger', args: 'Form submits twice on slow network connections' })
Skill({ skill: 'bug-debugger', args: 'Kanban drag-drop loses card position intermittently' })
```

## Debugging vs Error Fixing

| Situation | Use |
|-----------|-----|
| Clear error message (TS, build, etc.) | Error Fixer skill |
| Behavior bug, no clear error | `bug-debugger` |
| Performance issue | `performance-engineer` |
