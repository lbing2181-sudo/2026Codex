# Immiforyou

## Role In 2026Codex

This folder is the control-layer project entry for the immigration content product currently represented by:

- repository:
  `https://github.com/lbing2181-sudo/lbing2181-sudo.github.io`
- live site:
  `https://immiforyou.com`

This is not the full source mirror.
It is the operating entry inside `2026Codex`.

## Current Status

- Connected to the master control repository
- Active for `v2` rebuild planning
- `v1` remains live and unchanged during planning
- `v2` rebuild repository now exists:
  `https://github.com/lbing2181-sudo/immiforyou-v2`
- Reserved for strategy, operating memory, architecture, and project decisions

## Required Boot Path

Before starting work in a new thread, read in this order:

1. root `START_HERE.md`
2. root `PROJECT_OS.md`
3. root `WORKING_MEMORY.md`
4. this `README.md`
5. `DECISIONS.md`
6. `WORKING_MEMORY.md`
7. `M0_V1_FREEZE_CHECKLIST.md` while `v1` freeze and `v2` planning remain active
8. `V2_REBUILD_PLAN.md` before any `v2` implementation decision

## Source Of Truth

- GitHub repository first
- Live site second
- Local copies only as fallback context

## What Lives Here

- `OFFER.md`:
  what this project sells
- `PIPELINE.md`:
  how the rebuild and migration should operate
- `DECISIONS.md`:
  project-level decisions
- `WORKING_MEMORY.md`:
  current project state
- `V2_REBUILD_PLAN.md`:
  architecture, phases, milestones, and acceptance for the parallel rebuild
- `REPO_STRATEGY.md`:
  repository names, boundaries, and ownership for `v1`, `v2`, and `2026Codex`
- `M0_V1_FREEZE_CHECKLIST.md`:
  the current phase-control file that freezes `v1` before `v2` implementation

## Operating Rule

- Do not start implementation from stale assumptions.
- When this project is activated, policy and process claims must be checked against official government sources first.
- Treat this as a content product and information-service system, not as legal advice.
- Before formal takeover, reread the latest GitHub repository content and live site state first.
- Update the control-layer understanding to the newest repository state before starting work in `2026Codex`.
- Keep `v1` running while `v2` is rebuilt in parallel.
- Reuse stable infrastructure where possible:
  domain, Cloudflare layer, Supabase project, analytics, and Worker-backed integrations.
- Obey document hierarchy strictly:
  root control files override this project folder,
  and this project folder overrides phase plans and execution notes.
- Backtest project documents when direction changes:
  remove or revise stale lower-level expressions
  so future threads do not inherit reversed instructions by accident.
