# IMMIFORYOU REPOSITORY STRATEGY

## Core Decision

`immiforyou` should run as a three-repository system.

Do not rebuild `v2` directly inside the live production repository.

## Repository Topology

### 1. Production Repository

Recommended identity:

- repository:
  `lbing2181-sudo/lbing2181-sudo.github.io`
- role:
  current `v1` live production system

What it owns:

- current live site code
- current content publishing flow
- current GitHub Pages deployment
- current Cloudflare-facing production behavior
- current Worker references already wired into `v1`
- current SEO-visible public routes

What it should not own:

- large-scale `v2` restructuring work
- unstable template experiments
- architectural rewrite branches that put `v1` stability at risk

### 2. Rebuild Repository

Actual identity:

- repository:
  `lbing2181-sudo/immiforyou-v2`
- visibility:
  private
- role:
  parallel rebuild repository for `v2`

What it owns:

- the new front-end architecture
- template system
- structured content model
- modular diagnosis shell
- shared SEO system
- migration-ready application layer

What it should not own:

- direct production content publishing for `v1`
- legacy one-off page maintenance
- unrelated experiments

### 3. Control Repository

Current identity:

- repository:
  `lbing2181-sudo/2026Codex`
- role:
  control tower and long-term memory

What it owns:

- strategy
- rebuild planning
- project decisions
- operating memory
- migration checklists
- repository responsibilities

What it should not own:

- full source mirror of `v1`
- full source mirror of `v2`
- direct production deployment logic

## Why This Topology Is Correct

It separates three different kinds of work:

- live production stability
- parallel rebuilding
- strategic control and memory

Without this separation, the same repository starts carrying:

- revenue risk
- rewrite risk
- memory and planning burden

That becomes noisy very quickly.

## Recommended Naming

Use these names unless there is a strong branding reason not to.

- `lbing2181-sudo.github.io`
  current live production repository
- `immiforyou-v2`
  clean rebuild repository
- `2026Codex`
  control repository

This naming is plain, stable, and easy to understand later.

## Ownership Boundary

### `lbing2181-sudo.github.io`

Default work allowed:

- urgent production fixes
- content updates
- SEO maintenance
- current-route maintenance
- live incident handling

Default work blocked:

- major re-architecture
- large template rewrite
- moving page classes into a new framework

### `immiforyou-v2`

Default work allowed:

- architecture rebuild
- component and layout system
- content model design
- route reconstruction
- migration preparation
- parity testing

Default work blocked:

- direct replacement of production before QA acceptance

### `2026Codex`

Default work allowed:

- decisions
- planning
- repo strategy
- migration logic
- handoff memory

## Migration Rule

The migration direction should always be:

`v1 production repo` -> reference target
`v2 rebuild repo` -> implementation target
`2026Codex` -> control layer

Never invert this relationship.

## Infrastructure Rule

The future cutover should reuse infrastructure where possible:

- same domain
- same Cloudflare zone
- same Supabase project where schema remains compatible
- same Worker boundary where contract remains valid
- same analytics and verification layers

This means:

the rebuild repository changes the application layer,
not the business foundation.

## Working Rule Before V2 Starts

Before `v2` implementation starts:

1. reread the latest production repository documentation
2. reread the latest live site state
3. confirm repo boundaries
4. create the new private rebuild repository
5. only then start scaffold work

## Immediate Next Step

The rebuild repository has now been created.

Next:

1. connect it inside `2026Codex`
2. add the first scaffold files
3. start the `v2` implementation only after the rebuild scope is reviewed
