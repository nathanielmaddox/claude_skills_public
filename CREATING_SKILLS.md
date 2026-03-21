# Creating a New Skill

A practical guide. Follow these steps and you'll have a working skill in 10 minutes.

---

## Where Skills Live

| Location | Purpose |
|----------|---------|
| `~/.claude/skills/{skill-name}/` | **Executable** -- what Claude actually runs |
| `desktop/vs_code/claude_skills/{category}/` | **Catalog** -- human reference, README per category |

The executable skill is the source of truth. The catalog is documentation.

---

## Required Files

```
~/.claude/skills/my-skill/
  SKILL.md                    # Required: skill definition + runbook
  references/
    checklist.md              # Required: validation gates (Critical/Important/Nice-to-Have)
    pitfalls.md               # Required: starts empty, grows via self-improvement
    shortcuts.md              # Required: starts empty, grows via discovered fast-paths
```

---

## Step-by-Step Process

### 1. Pick a name

- Lowercase, hyphen-separated: `api-designer`, `build-error-fixer`
- Max 64 characters
- No "anthropic" or "claude" in the name

### 2. Create the directory

```bash
mkdir -p ~/.claude/skills/my-skill/references
```

### 3. Write SKILL.md

Use the structure below. Keep the body under 5k tokens -- move detailed content to `references/`.

### 4. Create references/checklist.md

```markdown
# My Skill -- Validation Checklist

Source: [industry tool or standard this is based on]

## Critical (must pass, blocks delivery)
- [ ] [Specific, verifiable item]
- [ ] [Specific, verifiable item]

## Important (should pass, warn if failing)
- [ ] [Specific, verifiable item]

## Nice-to-Have (improve if time allows)
- [ ] [Specific, verifiable item]
```

Every item must be **verifiable** -- no vague "ensure quality" entries. Base items on what real tools check (Lighthouse, axe-core, OWASP ZAP, Ahrefs, etc.).

### 5. Create references/pitfalls.md

```markdown
# My Skill -- Known Pitfalls

Read this FIRST before starting any work. These are mistakes from previous runs.

[Entries will be added as mistakes are discovered]
```

### 6. Create references/shortcuts.md

```markdown
# My Skill -- Efficiency Shortcuts

Check this before starting. If a shortcut applies, use it instead of the full process.

[Entries will be added as shortcuts are discovered]
```

### 7. Update registrations (see "After Creation" below)

---

## SKILL.md Structure

```markdown
---
name: my-skill
description: What this skill does. Include trigger keywords so Claude knows when to activate it. (max 1024 chars)
context: fork
allowed-tools: Read, Glob, Grep, Write, Edit
---

## MANDATORY: Pre-Flight

Before doing ANY work:

1. **Read pitfalls** -- Read `references/pitfalls.md`. Check EVERY item.
2. **Read shortcuts** -- Read `references/shortcuts.md`. Use a fast-path if one applies.
3. **Verify context:**
   - [ ] Clear understanding of what the user wants
   - [ ] Access to files/codebase
   - [ ] Knowledge of project tech stack

---

## Execution Process

### Step 1: [First Major Step]
[What to do]

**Gate 1 -- Verify before proceeding:**
- [ ] [Verification item]

### Step 2: [Second Major Step]
[What to do]

**Gate 2 -- Verify before proceeding:**
- [ ] [Verification item]

[Continue as needed...]

---

## MANDATORY: Post-Flight Checklist

BEFORE delivering ANY output, verify EVERY item in `references/checklist.md`.

Universal checks:
- [ ] Output actually works (build, run, render -- don't assume)
- [ ] No regression introduced
- [ ] Follows project's existing patterns
- [ ] No security vulnerabilities introduced
- [ ] No accessibility violations introduced

**If ANY item fails: fix it before delivering.**

---

## MANDATORY: Self-Improvement Protocol

### On error:
Append to `references/pitfalls.md`:
- **Error:** What went wrong
- **Root cause:** Why it happened
- **Fix:** What to do instead
- **Prevention:** What check would catch this

### On discovered shortcut:
Append to `references/shortcuts.md`:
- **Instead of:** The slow approach
- **Do this:** The fast approach
- **When it applies:** Conditions

---

## Core Knowledge

[Domain-specific expertise. Keep under 3000 tokens here.
Move detailed reference material to references/ files.]

---

## Integration & Escalation

**Works with:** [Related skills]
**Escalate when:** [When this skill can't solve the problem alone]
```

### Frontmatter Fields

| Field | Rules |
|-------|-------|
| `name` | Required. Max 64 chars, lowercase + hyphens + numbers only |
| `description` | Required. Max 1024 chars, no XML tags. Include trigger keywords |
| `context` | Use `fork` for skills that should run in isolated context |
| `allowed-tools` | List tools the skill can use |

### Progressive Disclosure

| Level | When Loaded | Token Cost |
|-------|-------------|------------|
| Metadata (name + description) | Always at startup | ~100 tokens |
| SKILL.md body | When triggered | Under 5k tokens |
| references/ files | As needed | Unlimited |

This is why you keep SKILL.md lean and put details in `references/`.

---

## After Creation

Three things to update:

### 1. CLAUDE.md skills list

Add the new skill name to the appropriate category in `~/.claude/CLAUDE.md` under "Available Skills."

### 2. TABLE_OF_CONTENTS.md

Update the skill count and add to the relevant category row in `desktop/vs_code/claude_skills/TABLE_OF_CONTENTS.md`.

### 3. Category README

Add the skill entry to the appropriate `desktop/vs_code/claude_skills/{category}/README.md`.

---

## Common Mistakes

These are the top failure patterns across all skills. Avoid them.

| Mistake | Fix |
|---------|-----|
| **Assuming instead of verifying** | Always run the build, check the output, load the page. Never say "it works" without proof. |
| **Not reading existing code first** | Read relevant files before writing. Use Grep/Glob to find existing patterns. |
| **Ignoring project tech stack** | Check package.json and existing imports first. Don't use Prisma when the project uses Convex. |
| **Building only the happy path** | Every UI must handle: loading, empty, error, success, and edge cases. |
| **Delivering untested code** | Build and run before delivering. If you can't verify, say so explicitly. |
| **Over-engineering** | Read shortcuts.md first. Check for known fast paths before starting the full process. |
| **Leaving debug artifacts** | No console.logs, TODOs, hardcoded test values, or placeholder text in delivered output. |
| **Not communicating limitations** | State what was verified, what wasn't, and what assumptions were made. |
| **Skipping industry standards** | Checklists must be based on real tools (Lighthouse, OWASP ZAP, axe-core, Ahrefs). |

---

## Quick Checklist: Is My Skill Ready?

- [ ] `SKILL.md` has valid frontmatter (name + description)
- [ ] SKILL.md body is under 5k tokens
- [ ] Pre-Flight section reads pitfalls and shortcuts first
- [ ] Execution has numbered steps with verification gates
- [ ] Post-Flight verifies `references/checklist.md`
- [ ] Self-Improvement Protocol appends errors to pitfalls.md
- [ ] `references/checklist.md` exists with Critical/Important/Nice-to-Have tiers
- [ ] `references/pitfalls.md` exists (can be empty initially)
- [ ] `references/shortcuts.md` exists (can be empty initially)
- [ ] Checklist items are specific and verifiable, not vague
- [ ] CLAUDE.md updated with new skill name
- [ ] TABLE_OF_CONTENTS.md updated
- [ ] Category README updated
