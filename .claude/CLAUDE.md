# Manual Shell — Container Routing

**This is a container-level routing file.** The actual git repo lives at `manual-app/`. Worktrees live at `worktrees/`.

Cascade position:
```
~/.claude/CLAUDE.md
  └─ Documents/.claude/CLAUDE.md
     └─ GitHub/.claude/CLAUDE.md
        └─ manual-shell/.claude/CLAUDE.md    ← you are here
           └─ manual-shell/manual-app/.claude/CLAUDE.md  ← project rules
```

---

## Structure

```
manual-shell/
├── manual-app/       ← git repo root (main branch)
└── worktrees/
    ├── staging/
    ├── develop/
    ├── ws-a/
    ├── ws-b/
    └── ws-c/
```

## Branch Hierarchy

```
ws-a, ws-b, ws-c  →  develop  →  staging  →  main
```

Changes promote UP, sync DOWN — same pattern as `interface-shell`.

## Rules

- Always `cd` into `manual-app/` or the target worktree before making changes
- Read `manual-app/.claude/CLAUDE.md` for project-specific rules before any work
- `src-tauri/target/` is in `.gitignore` — never commit build artifacts
