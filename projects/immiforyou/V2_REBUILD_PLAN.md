# IMMIFORYOU V2 REBUILD PLAN

## Rebuild Position

- `v1` stays live.
- `v2` is rebuilt in parallel.
- Cutover happens only after page parity, integration parity, and QA parity are confirmed.
- `v2` should live in a separate private rebuild repository, not inside the production repository.

This is not a visual redesign first.
This is a structural rebuild first.

## Repository Strategy

This rebuild assumes a three-repository model:

- `lbing2181-sudo.github.io`:
  production `v1`
- `immiforyou-v2`:
  rebuild repository for `v2`
- `2026Codex`:
  control layer

See `REPO_STRATEGY.md` for repository roles and boundaries.

## Rebuild Goal

Build a cleaner, modular, maintainable version of `immiforyou.com` without breaking the working infrastructure that already exists.

The new version should preserve:

- the main domain
- the Cloudflare delivery layer
- the existing Supabase subscriber database
- the Worker-based diagnosis backend
- analytics and verification wiring
- current SEO-critical URLs wherever possible

## What V2 Is Fixing

The current live site proves product direction, but the codebase still has `v1` problems:

- homepage is too monolithic
- page templates are inconsistent
- shared styles and scripts are only partially extracted
- diagnosis page logic is tightly packed
- SEO structure is uneven across templates
- maintenance cost rises too quickly as pages grow

So the `v2` task is:

- keep the business logic that works
- remove structural debt
- rebuild the front-end system in a repeatable way

## Content Baseline Shift

The latest production-doc update at commit `a424f15` changes the rebuild baseline in an important way:

- the old slim-content direction is no longer valid for planning
- deep long-form content is now the default product standard

For `v2`, this means the system must be designed around depth, not around compression.

## Architecture Decision

### Core Principle

Keep infrastructure stable.
Replace the site application layer.

### Recommended V2 Stack

- front-end architecture:
  static-first, component-based site architecture
- rendering model:
  pre-rendered public pages with minimal client-side islands for interaction
- data layer:
  reuse current Supabase project where schema remains compatible
- AI/backend layer:
  keep Cloudflare Worker as the protected backend boundary for diagnosis and model calls
- delivery layer:
  keep Cloudflare in front of the site
- analytics layer:
  preserve GA, Baidu analytics, and verification integrations

### Implementation Direction

If I am responsible for the rebuild, I would not keep writing raw one-off HTML pages.
I would rebuild the site as a structured static project with:

- shared layouts
- shared SEO component
- shared content schemas
- shared navigation/footer blocks
- shared country/news page templates
- isolated interactive modules

And those templates must be comfortable with deep editorial density:

- long-form body sections
- richer heading hierarchies
- large data tables
- FAQ blocks
- persona-based interpretation blocks
- stronger official-source citation density

The key point is not the framework brand.
The key point is that `v2` must become template-driven instead of page-by-page hand assembly.

## Target V2 Structure

```text
immiforyou-v2/
  src/
    components/
      layout/
      seo/
      home/
      countries/
      news/
      diagnosis/
      membership/
      common/
    layouts/
      BaseLayout.*
      CountryLayout.*
      NewsLayout.*
    content/
      countries/
      news/
      pages/
    data/
      site.ts
      navigation.ts
      country-meta.ts
    styles/
      tokens.css
      base.css
      components/
      pages/
    lib/
      analytics.ts
      schema.ts
      workers.ts
      supabase.ts
      search.ts
    pages/
      index.*
      about.*
      diagnosis.*
      membership.*
      news/
      countries/
  public/
    robots.txt
    favicon.*
  docs/
    content-model.md
    migration-checklist.md
```

## Public Information Architecture

The rebuilt public structure should keep these core page groups:

- home
- countries index or country discovery layer
- country detail pages
- diagnosis page
- membership page
- news index
- news article pages
- about / trust / method pages

## Reusable Template System

V2 should have these template classes:

### 1. Base Layout

Shared:

- head tags
- canonical logic
- nav
- footer
- analytics hooks
- structured data hooks

### 2. Home Template

Shared blocks:

- hero
- search
- updates ticker
- country cards
- subscribe block

### 3. Country Template

Shared blocks:

- summary
- pathway cards
- requirements
- persona-fit interpretation
- deep comparison tables
- official-source links
- FAQ
- SEO schema block

### 4. News Template

Shared blocks:

- article header
- author/date/source discipline
- summary
- key changes
- deep analysis sections
- persona or use-case framing
- table-capable body content
- official-source references
- related country/topic links

### 5. Diagnosis Template

Shared blocks:

- questionnaire shell
- loading states
- result shell
- paywall shell
- Worker integration boundary

## Integration Boundary

This is the most important engineering rule for the rebuild.

### What Should Stay Outside The Front End

- DeepSeek API key
- model-calling logic
- any paid unlock verification
- any privileged write or read path

These should remain behind Cloudflare Workers or another controlled backend boundary.

### What Can Stay In The Front End

- public analytics IDs
- public verification tags
- public Supabase anon path if RLS remains correctly limited
- public rendering logic

### Current Reusable Integrations

- domain and Cloudflare zone:
  reusable
- Supabase subscriber project:
  reusable
- diagnosis Worker endpoint:
  reusable, but contract should be cleaned and documented
- scheduled publish Worker:
  reusable, but may need repo/build adjustments later
- analytics and verification:
  reusable

## Content Model Rules

V2 should stop treating content as page-specific hardcoded markup.

### Country Content Model

Each country should become structured content with fields like:

- slug
- chinese_name
- english_name
- region
- status
- teaser
- pathways
- budget range
- timeline range
- persona_slices
- faq_items
- comparison_tables
- official links
- last_verified_at
- seo title
- seo description

### News Content Model

Each article should have:

- slug
- title
- publish date
- effective date if different
- country/topic tags
- summary
- why_it_matters
- persona_impact
- faq_items
- table_blocks
- official_sources
- body
- schema fields

## Development Phases

### Phase 0: Freeze And Audit

Goal:
turn the current live site into a frozen reference target.

Deliverables:

- route inventory
- feature inventory
- current integration inventory
- SEO inventory
- content model inventory
- v1 risk list

Acceptance:

- every existing public route is listed
- every external dependency is listed
- every live integration is classified as reusable / refactor / replace

### Phase 1: Foundation Build

Goal:
create the clean project skeleton and system primitives.

Deliverables:

- project scaffold
- base layout
- global style tokens
- navigation/footer
- SEO component
- analytics wrapper

Acceptance:

- empty but running shell for all major page types
- no business logic yet
- styles and layouts centralized

### Phase 2: Template System

Goal:
build the reusable page templates before migrating content.

Deliverables:

- home template
- country template
- news template
- diagnosis shell
- membership shell

Acceptance:

- page types render from shared templates
- no duplicated page-level layout code for the same class of page

### Phase 3: Content Migration

Goal:
migrate high-priority content into structured models.

Deliverables:

- homepage copy and sections
- top-priority country pages
- news index and first migrated articles
- about / trust pages

Acceptance:

- migrated pages preserve current SEO intent
- canonical and metadata are correct
- URLs remain stable where possible

### Phase 4: Interactive Systems Rebuild

Goal:
rebuild interaction layers cleanly.

Deliverables:

- search module
- subscription module
- diagnosis questionnaire module
- diagnosis result rendering module

Acceptance:

- interaction code is modular
- front-end only handles public-safe logic
- Worker and Supabase contracts are isolated in dedicated adapters

### Phase 5: Technical Hardening

Goal:
close the architecture gaps that `v1` left open.

Deliverables:

- security header plan
- anti-abuse plan for subscription path
- accessibility pass
- schema pass
- performance pass

Acceptance:

- no giant monolithic entry page
- template consistency established
- structured data aligned across key page classes

### Phase 6: QA And Parity Review

Goal:
prove `v2` is safe to replace `v1`.

Deliverables:

- route parity checklist
- metadata parity checklist
- integration parity checklist
- visual QA pass
- mobile QA pass

Acceptance:

- all critical public pages work
- diagnosis flow works
- subscription flow works
- analytics hooks are present
- no major SEO regression risk

### Phase 7: Cutover

Goal:
move traffic without breaking the working business surface.

Deliverables:

- cutover checklist
- rollback checklist
- post-launch monitoring checklist

Acceptance:

- domain points to `v2`
- critical paths return `200`
- rollback path is prepared before cutover

## Suggested Execution Order

This is the order I would actually use:

1. Freeze `v1`
2. Build the `v2` shell
3. Build the shared templates
4. Rebuild diagnosis shell and integration adapters
5. Rebuild homepage and country template
6. Migrate key content
7. QA parity
8. Cutover

## Milestone Tracker

### M0: Planning Locked

Status:
in progress

Meaning:
the rebuild direction, architecture, and scope are agreed.

### M1: Foundation Ready

Status:
not started

Meaning:
`v2` has a clean scaffold and reusable base system.

### M2: Template Ready

Status:
not started

Meaning:
main page classes can render from shared templates.

### M3: Integration Ready

Status:
not started

Meaning:
Supabase, Worker, analytics, and public-safe modules are reconnected.

### M4: Content Ready

Status:
not started

Meaning:
priority pages are migrated and reviewable.

### M5: Cutover Ready

Status:
not started

Meaning:
`v2` can replace `v1` with controlled risk.

## Time Estimate

If I own the work and keep the scope disciplined, I would estimate:

- planning lock:
  2 to 3 days
- foundation + templates:
  4 to 7 days
- content + interactions:
  7 to 12 days
- QA + hardening + cutover prep:
  4 to 6 days

Practical total:

- about 3 to 4 working weeks for a clean `v2`

This assumes:

- we are rebuilding structure first
- not adding large new business modules
- not solving payment productization in the same batch

## What Is Explicitly Not In V2 First Batch

- payment gateway productionization
- large new product modules
- major business model expansion
- unnecessary visual experimentation

The first batch is for:

- architecture
- maintainability
- parity
- trustworthiness

## Review Standard

When we discuss this plan, the questions should be:

- is the architecture clean enough
- is the scope disciplined enough
- is the migration risk low enough
- is the order realistic enough
- what should be removed before anything new is added

That is the right conversation before code.
