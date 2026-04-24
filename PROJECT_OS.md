# PROJECT_OS

## Project Identity

- This workspace is the long-term operating system for commercial, taste-driven AI projects.
- The core goal is to use AI to create high-value work for real clients first, then decide whether tooling or productization is necessary.
- Revenue comes before SaaS. Results come before tools.

## Aesthetic Standard

- Every output should feel calm, precise, expensive, and necessary.
- Avoid noisy novelty, generic "AI style", and low-grade trend chasing.
- Prefer clear visual worlds, controlled restraint, and strong product presence.
- Commercial taste is part of the product, not decoration.

## Business Standard

- Focus on markets with large demand, clear value, and low delivery cost.
- Prefer high-margin creative services built on repeatable systems.
- Do not expand into software productization until the service model has repeated proof.
- Choose clients, offers, and categories that reward quality, not volume.

## Collaboration Rules

- Chat is for movement, not memory.
- Long-term memory must be written back into repository files.
- Important decisions go into `DECISIONS.md`.
- Current priorities and active context go into `WORKING_MEMORY.md`.
- Each project gets its own folder under `projects/`.
- Before formally taking over any project, reread the latest GitHub repository state and live product state first.
- Do not start execution work from stale local context when newer repository content may exist.
- Sync understanding to the newest source-of-truth state before making changes in the control repository.

## Document Governance

- Documentation must not grow as an unmanaged archive.
- When a newer decision overturns an older rule, the older expression should be revised or removed as soon as practical.
- Avoid leaving invalidated instructions alive in lower-level files where they can mislead a future thread or another AI.
- Document maintenance must include periodic backtesting:
  reread current upper-level rules,
  scan lower-level files,
  and clean or rewrite expressions that no longer match the active direction.
- Hierarchy is mandatory:
  top-level control documents override project-level documents,
  and project-level control documents override phase files, planning files, and execution notes.
- Lower-level documents may add detail, but may not contradict upper-level documents.
- If an upper-level rule changes, affected lower-level files must be updated before new execution continues.
- If a lower-level file contains reversed or stale language, treat it as a documentation bug and fix it.

## Memory Defense

- Every active project must have a clear boot path for new threads and future handoff.
- The default startup order is:
  `START_HERE.md` -> `PROJECT_OS.md` -> root `DECISIONS.md` -> root `WORKING_MEMORY.md` -> project `README.md` -> project `DECISIONS.md` -> project `WORKING_MEMORY.md`.
- If a project has a phase-specific control file such as `M0_V1_FREEZE_CHECKLIST.md` or `V2_REBUILD_PLAN.md`, that file becomes part of the required startup path for that phase.
- When a thread ends with important conclusions, write them back before moving on.
- The repository must remain readable by another AI or another future thread without private chat dependence.

## Structure

- Top level: strategy, collaboration memory, cross-project standards.
- `projects/<project-name>/`: offer, pipeline, project decisions, project working state.

## Operating Principle

- Build small, elegant systems that can produce real money.
- Keep the language simple.
- Keep the standards high.
- Keep the work executable.
