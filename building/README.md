# Building

Skills for building forms and UI components with project-specific patterns.

## Skills

| Skill | Command | Description |
|-------|---------|-------------|
| Form Builder | `form-builder` | ERP forms with validation, error handling, accessibility, multi-step wizards |
| UI Component Builder | `ui-component-builder` | Storybook components with TypeScript, all variants/states, showcase pages, registry |

## When to Use

- **form-builder** — Any new form in the ERP: simple inputs, complex multi-step wizards, connected forms
- **ui-component-builder** — Any new component for the design system (otesse_ds)

## Otesse Context

- **Forms** follow the connected form architecture (see `erp-connected-forms-architecture.md`)
- **Components** go in `otesse_ds` first, then sync to ERP (see DS sync rule)
- DS has 400+ components already — check before building duplicates

## Usage Examples

```
Skill({ skill: 'form-builder', args: 'Build customer edit form with address fields' })
Skill({ skill: 'ui-component-builder', args: 'Build a StatusBadge component' })
```
