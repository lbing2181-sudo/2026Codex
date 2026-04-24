# IMMIFORYOU M1 TEMPLATE MATRIX

## Purpose

This file translates the approved content model into page-template structure.

It is the second required output of `M1`.

## Principle

- templates exist to carry structured content cleanly
- templates should reduce page-by-page improvisation
- shared blocks should be centralized
- deep content should feel readable, not heavy
- dynamic behavior should be isolated to the few blocks that truly need it

## Global Template Families

| Template Family | Role | Shared Scope |
|---|---|---|
| `BaseLayout` | global shell | head tags, canonical, global nav, footer, analytics hooks, shared scripts |
| `ContentLayout` | long-form reading shell | article rhythm, section spacing, table styling, source styling, FAQ styling |
| `LandingLayout` | conversion-oriented shell | hero framing, CTA rhythm, trust blocks, compact section cadence |
| `UtilityLayout` | tool-oriented shell | step flow, state blocks, result shell, legal / trust framing |

## Template Matrix

| Page Template | Base Family | Required Blocks | Optional Blocks | Dynamic Blocks | Notes |
|---|---|---|---|---|---|
| Home | `LandingLayout` | global nav, hero, value proposition, search, country discovery, fresh news signal, diagnosis entry, trust signal, footer | featured picks, editorial note, soft CTA | featured news feed | system homepage, not a blog index |
| News List | `ContentLayout` | global nav, page intro, article list, tag/topic cues, footer | filters, editorial note | article listing feed | should remain clean even as article depth grows |
| News Article | `ContentLayout` | global nav, article header, author block, summary, sectioned body, tables, FAQ, official sources, related links, footer | sticky TOC, persona block, update note | related links module | default long-form authority template |
| Country Detail | `ContentLayout` | global nav, hero, overview, pathway breakdown, requirements, cost/timeline, comparison tables, persona-fit block, FAQ, official links, disclaimer, footer | quick decision summary, source notes, trust reminder | related-news aggregation block | static-first evergreen template with one living news layer sourced from the site's own original news articles |
| Diagnosis | `UtilityLayout` | global nav, intro, trust framing, questionnaire shell, loading state, result shell, disclaimer, footer | case examples, pre-qualification explainer, payment explanation layer | questionnaire state, result rendering, worker-backed diagnosis | future primary service-entry template |
| Membership | `LandingLayout` | global nav, offer framing, who-it-is-for, benefit blocks, free-vs-paid comparison, FAQ, CTA, footer | testimonials, roadmap note, team note | pricing / offer state if needed later | can remain commercially light in first batch |
| About / Trust | `ContentLayout` | global nav, mission, method, why trust us, source discipline, non-legal-advice boundary, editorial discipline, footer | team note, timeline, principle cards | none by default | trust-supporting template |

## Shared Block Library

### Global Shared Blocks

- `GlobalNav`
- `GlobalFooter`
- `SeoHead`
- `AnalyticsHooks`
- `TrustMicrocopy`

### Long-Form Shared Blocks

- `ArticleHeader`
- `AuthorBlock`
- `SectionRenderer`
- `TableBlock`
- `FaqBlock`
- `OfficialSourcesBlock`
- `RelatedLinksBlock`
- `DisclaimerBlock`

### Landing Shared Blocks

- `HeroBlock`
- `ValueStack`
- `TrustSignals`
- `ComparisonBlock`
- `PrimaryCtaBlock`

### Utility Shared Blocks

- `StepShell`
- `LoadingState`
- `ResultShell`
- `ActionPanel`
- `BoundaryNotice`

## Block Ownership By Template

| Block | Home | News List | News Article | Country Detail | Diagnosis | Membership | About / Trust |
|---|---|---|---|---|---|---|---|
| `GlobalNav` | required | required | required | required | required | required | required |
| `SeoHead` | required | required | required | required | required | required | required |
| `HeroBlock` | required | optional | optional | required | optional | optional | optional |
| `ArticleHeader` | no | no | required | no | no | no | no |
| `AuthorBlock` | no | no | required | no | no | no | no |
| `SectionRenderer` | limited | no | required | required | limited | limited | required |
| `TableBlock` | no | no | required | required | optional | optional | no |
| `FaqBlock` | no | no | required | required | optional | required | optional |
| `OfficialSourcesBlock` | no | no | required | required | optional | no | optional |
| `RelatedLinksBlock` | optional | no | required | optional | no | no | no |
| `RelatedNewsAggregation` | no | no | no | required | no | no | no |
| `StepShell` | no | no | no | no | required | no | no |
| `ResultShell` | no | no | no | no | required | no | no |
| `ComparisonBlock` | optional | no | no | optional | no | required | no |
| `PrimaryCtaBlock` | required | optional | optional | optional | required | required | optional |
| `DisclaimerBlock` | optional | no | required | required | required | optional | required |
| `GlobalFooter` | required | required | required | required | required | required | required |

## Dynamic Boundary Rules

| Block Type | Rule |
|---|---|
| `RelatedNewsAggregation` | may be auto-aggregated or built from structured article relations, but only from the site's own original news corpus |
| `Questionnaire / Result` | stays behind protected adapters and Worker boundaries |
| `FeaturedNewsFeed` | can be dynamic, but should degrade gracefully |
| `Most country-page blocks` | static-first, not tied to constant live rewriting |

## Static-First Rule For Country Pages

Country pages should remain mostly stable.

Only this block is expected to stay meaningfully dynamic by default:

- `RelatedNewsAggregation`

Everything else should be optimized for:

- evergreen trust
- low maintenance burden
- slower editorial refresh cadence

## Readability Rules For Deep Content Templates

Because `D61` depth is now a core rule, long-form templates should assume:

- strong section spacing
- visible hierarchy between H2 and H3
- table overflow handling without visual breakage
- source blocks that do not feel like footnote clutter
- FAQ and persona blocks that read as part of the page, not as appendices

## Visual Continuity Rule

`v2` should not break the user's mental image of `v1`.

This means:

- preserve the calm premium tone
- preserve the reading-first feeling
- avoid a drastic visual reset in the first rebuild batch
- improve structure first, then evolve the design carefully

## Entry To Next Step

After this file is reviewed, the next valid step is not code yet unless needed immediately.

The next preferred outputs are:

1. block-priority order by template
2. implementation scaffold plan inside `immiforyou-v2`
