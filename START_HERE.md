# START HERE

This repository is the control tower for long-term AI projects.
Do not start from chat memory.

## Default Boot Order

1. Read `START_HERE.md`
2. Read `PROJECT_OS.md`
3. Read root `DECISIONS.md`
4. Read root `WORKING_MEMORY.md`
5. Enter the relevant project folder under `projects/`
6. Read the project's `README.md`
7. Read the project's `DECISIONS.md`
8. Read the project's `WORKING_MEMORY.md`

## Phase-Specific Rule

If a project is in a defined phase, read that phase file before doing work.

Examples:

- `projects/immiforyou/M0_V1_FREEZE_CHECKLIST.md`
- `projects/immiforyou/V2_REBUILD_PLAN.md`

## Source Of Truth Rule

- GitHub repository first
- Live product second
- Local copies only as fallback

## Handoff Rule

- Do not assume the last chat is complete.
- Refresh the newest repository state first.
- Write key conclusions back into repository files before ending a work block.

## Document Hierarchy Rule

- Upper-level documents override lower-level documents.
- Root control documents override all project documents.
- Project control documents override phase files, planning files, and execution notes.
- Lower-level files may expand detail, but may not reverse upper-level rules.

## Document Backtesting Rule

- When a new decision changes direction, reread affected files and clean old expressions.
- Do not leave invalidated rules alive just because they are historical.
- Treat stale or reversed documentation as a bug to be fixed.
