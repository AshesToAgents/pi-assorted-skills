# pi-assorted-skills

A [pi](https://github.com/mariozechner/pi-coding-agent) package of process skills for planning, debugging, testing, and review — a trimmed fork of [obra/superpowers](https://github.com/obra/superpowers) v7.0.1.

## Install

```bash
# Global (user-level)
pi install ssh://git@github.com/AshesToAgents/pi-assorted-skills.git

# Project-level (shared with team via .pi/settings.json)
pi install -l ssh://git@github.com/AshesToAgents/pi-assorted-skills.git

# Try without installing
pi -e ssh://git@github.com/AshesToAgents/pi-assorted-skills.git
```

## What's Included

| Type | Name | Description |
|------|------|-------------|
| Skills | `brainstorming` | Question-driven design conversations before building; design docs only for project-sized work |
| Skills | `writing-plans` | Implementation plans for work that will be dispatched to subagents |
| Skills | `executing-plans` | Inline plan execution with ledger and per-task verification |
| Skills | `subagent-driven-development` | Fresh implementer/reviewer subagents per task, driven by a plan |
| Skills | `writing-skills` | Creating and editing skills |
| Skills | `systematic-debugging` | Root-cause discipline for bugs and unexpected behavior |
| Skills | `test-driven-development` | RED-GREEN-REFRACTOR cycle for features and fixes |
| Skills | `verification-before-completion` | Evidence before any "done" claim |
| Skills | `using-git-worktrees` | Isolated workspaces for feature work |
| Skills | `finishing-a-development-branch` | Land or discard a branch once its work is done |
| Skills | `requesting-code-review` | Dispatch a fresh-context reviewer over a diff |
| Skills | `receiving-code-review` | Evaluate review feedback with rigor before acting |

## Differences from upstream

Derived from obra/superpowers v7.0.1 (MIT, Jesse Vincent — thank you). Trimmed for a leaner workflow:

- 12 of 15 skills kept; `using-superpowers`, `dispatching-parallel-agents`, and `diagnosing-superpowers` dropped — native pi skill routing replaces the bootstrap
- No aggressive session bootstrap; skills are invoked by routing or `/skill:<name>`
- `brainstorming`: no mandatory design doc for small changes; the visual-companion browser server is removed
- `writing-plans`: plans are written only when work will be dispatched to subagents
- Graph rendering removed from `writing-skills`; skill self-test files removed from `systematic-debugging`
- Forge-neutral wording throughout (GitHub PRs are not assumed)
- Plan artifacts default to the project's `.pi/plans/`, SDD workspace to `.pi/sdd/`

## License

MIT — see [LICENSE](LICENSE). Upstream © Jesse Vincent.
