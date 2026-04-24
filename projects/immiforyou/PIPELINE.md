# PIPELINE

## Current Mode

Active for `v2` rebuild planning.
`v1` stays live during planning and later implementation.

## Rebuild Workflow

1. reread latest GitHub repository and live site state
2. freeze `v1` routes, features, and integrations
3. define `v2` architecture and template system
4. rebuild the application layer in parallel
5. reconnect stable infrastructure
6. run parity QA
7. cut over only after acceptance is passed

## Current Rule

- Do not patch `v1` into a pseudo-`v2`.
- Do not rebuild from memory when the repository has newer truth.
- Preserve domain, Worker boundaries, analytics, and reusable data systems where possible.
- Replace structure before adding new business complexity.

## Active Planning Artifact

- `V2_REBUILD_PLAN.md` is the primary rebuild document.
