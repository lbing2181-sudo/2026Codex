# IMMIFORYOU M0 V1 FREEZE CHECKLIST

## Purpose

This file freezes the current `v1` system before `v2` implementation begins.

It exists to stop uncontrolled scope growth, stale-memory execution, and accidental rebuild drift.

## Current Status

`M0` has now reached review-ready status.

This means:

- the `v1` surface is frozen enough to discuss structurally
- `v2` can be planned from a stable reference target
- implementation still remains blocked until review is explicitly accepted

## Phase Rule

While `M0` is active:

- `v1` stays live
- `v1` code changes are limited to content publishing and urgent production fixes
- subscription and payment remain off as business priorities
- `v2` planning may continue
- `v2` implementation does not start until this freeze is reviewed

## Source Of Truth

| Priority | Source | Role |
|---|---|---|
| 1 | `lbing2181-sudo/lbing2181-sudo.github.io` | production repository truth |
| 2 | `https://immiforyou.com` | live behavior truth |
| 3 | `2026Codex/projects/immiforyou/` | control-layer interpretation |

## Startup Path For Any New Thread

| Order | File | Why |
|---|---|---|
| 1 | root `START_HERE.md` | initializes the control-tower rule set |
| 2 | root `PROJECT_OS.md` | restores collaboration and memory rules |
| 3 | root `WORKING_MEMORY.md` | restores top-level active state |
| 4 | `projects/immiforyou/README.md` | restores project role and source-of-truth rules |
| 5 | `projects/immiforyou/DECISIONS.md` | restores locked decisions |
| 6 | `projects/immiforyou/WORKING_MEMORY.md` | restores current phase state |
| 7 | this file | restores `M0` boundaries before any planning or build work |
| 8 | `V2_REBUILD_PLAN.md` | only after the freeze context is reloaded |

## V1 Freeze Summary

| Item | Current Freeze Decision |
|---|---|
| Site status | online and functioning |
| Development status | paused for rebuild planning |
| Content publishing | allowed to continue |
| Subscription | not a current `v1` focus |
| Payment / monetization | deferred to `v2` |
| Diagnosis capability | preserved as a core future monetization entry |
| Rebuild mode | parallel `v2`, separate repository |
| Core risk rule | do not let `v1` keep growing structurally while `v2` is being designed |
| Content baseline | follow latest production-doc standard at commit `a424f15` |

## Public Route Classes

Based on the live sitemap observed on `2026-04-22`, `v1` currently exposes these route groups:

| Route Class | Current Surface |
|---|---|
| Home | `/` |
| News hub | `/news/` |
| News articles | 5 published article routes currently visible in sitemap |
| Core utility pages | `/diagnosis.html`, `/membership.html`, `/about.html` |
| Country pages | 62 country and regional routes under `/countries/` |
| Discovery / guide class | includes at least one guide-style route under `/countries/` such as `caribbean-guide.html` |
| Crawl surface | `robots.txt` and `sitemap.xml` are public and active |

## Route Inventory Snapshot

| Class | Count | Notes |
|---|---|---|
| Home | 1 | canonical root route |
| News hub | 1 | `/news/` |
| News articles | 5 | includes `digital-nomad-6-alternatives-2026` as the newest article in sitemap on `2026-04-22` |
| Core utility pages | 3 | `diagnosis.html`, `membership.html`, `about.html` |
| Country and regional pages | 62 | core destination inventory under `/countries/` |
| Total public HTML routes in sitemap | 72 | excluding `robots.txt` and `sitemap.xml` utility files |

## Home Page Snapshot

Observed from the live homepage on `2026-04-22`:

| Item | Current State |
|---|---|
| Page title | `全球移民目的地 2026 | 主流国家移民政策查询与解读` |
| Canonical | `https://immiforyou.com/` |
| Schema | `WebSite` plus `ItemList` visible in page source |
| Search mode | on-page country search map |
| Main navigation role | home, news, diagnosis, membership, about |
| Subscription shell | present in homepage code but not a current business priority |
| Analytics traces | homepage still contains Google and Baidu-oriented traces in source structure |

## V1 Template Class Snapshot

Observed from live pages on `2026-04-22`:

| Template Class | Sample Route | Current Traits |
|---|---|---|
| Home | `/` | hero, country search, discovery navigation, homepage schema, subscription shell |
| News list | `/news/` | list layout, article cards, metadata tags, canonical, analytics hooks |
| Country detail | `/countries/usa.html` | long-form policy guide, official links, structured sections, multiple tables, disclaimer block |
| Diagnosis | `/diagnosis.html` | tool-style interaction shell, diagnosis-specific script, analytics hooks |
| Membership | `/membership.html` | long-form offer/value page, conversion shell, canonical, analytics hooks |
| News article | `/news/{slug}/` | article-detail class assumed from live route structure and news hub links |

## Current Shared Front-End Asset Pattern

| Pattern | Evidence |
|---|---|
| Shared country script | live news page and country page both reference `country.js` |
| Shared news styling | `/news/` references `/css/news-article.css` |
| Page-specific diagnosis script | `/diagnosis.html` references `js/diagnosis.js` |
| Page-level inline styles still exist | homepage and country pages still carry substantial inline styling or page-local structure |

## External Integration Boundary Snapshot

Observed from live sitemap and sampled live pages on `2026-04-22`:

| Integration | Current Status | V2 Direction |
|---|---|---|
| Google Analytics | present on homepage, news, country, diagnosis, membership surfaces | preserve and centralize |
| Baidu Analytics | present on sampled pages | keep only as low-priority compatibility |
| Canonical tags | present on sampled core pages | preserve and standardize |
| JSON-LD / schema | clearly visible on homepage | standardize across key page classes |
| Supabase subscriber path | present in homepage code | preserve boundary but harden abuse control later |
| Diagnosis front-end module | present via `js/diagnosis.js` | preserve behavior, modularize shell |
| Worker-backed diagnosis backend | known preserved boundary from project docs | preserve contract and document it better |
| DeepSeek-backed diagnosis ability | already configured and tested behind the diagnosis path | preserve as future primary service entry |
| Cloudflare delivery layer | active production boundary | preserve |

## SEO-Visible Rule Snapshot

Observed from sampled live pages on `2026-04-22`:

| SEO Surface | Current Pattern |
|---|---|
| Title tags | present across sampled core pages |
| Meta description | present on sampled content and trust pages |
| Canonical tags | present across sampled core pages |
| Open Graph basics | visible on sampled about and article pages |
| Article time metadata | visible on sampled news article page |
| JSON-LD | homepage and sampled article page visibly include structured data blocks |
| Stable route style | root, `/news/`, `/news/{slug}/`, `/countries/{slug}.html`, utility `.html` pages |
| Sitemap | public and active |
| Robots | public and active |

## V1 First-Batch Exclusion Snapshot

These are now explicitly treated as out of scope for the first `v2` build batch:

| Exclusion | Reason |
|---|---|
| payment productionization | not yet a first-order rebuild dependency |
| subscription growth optimization | `v1` is not using it as a current business priority |
| large visual redesign | structure comes first |
| user account system | adds complexity before the foundation is clean |
| broad new feature expansion | would recreate `v1` scope drift |
| shrinking content depth for convenience | conflicts with `D61` |

## V1 Product Surface To Preserve

| Surface | Freeze Decision For V2 Reference |
|---|---|
| Home | preserve as the master orientation and discovery page |
| Country pages | preserve as the main search and trust surface |
| News pages | preserve as the freshness and change-tracking surface |
| Diagnosis page | preserve as a mid-funnel conversion shell |
| Membership page | preserve as a future monetization shell, not yet fully activated |
| About page | preserve as trust and method surface |

## Content Standard Freeze

Based on the latest production documentation update at commit `a424f15`, the active content rule is no longer the old slim-content model.

| Item | Current Freeze Decision |
|---|---|
| Governing rule | `D61` content-depth core principle |
| Old slim-content direction | revoked for planning purposes |
| Target article depth | 3000-5000 Chinese characters |
| Heading depth | 6-9 H2 sections with required H3 support |
| Table depth | large tables are expected, not optional decoration |
| FAQ depth | multi-question FAQ expected |
| Persona depth | multi-persona slicing expected |
| Source density | stronger official-source density is part of the baseline |

## V2 Planning Impact From D61

| Area | Impact |
|---|---|
| News template | must support long-form article bodies instead of short compact summaries |
| Country template | must preserve space for deep explanatory sections, not only teaser cards |
| Content model | needs structured fields for FAQ, personas, tables, and source blocks |
| Page layout | must remain readable at much greater depth and scrolling length |
| Build scope | content depth is now a core product rule, not a later enhancement |
| Performance work | should optimize long pages instead of trying to avoid them |

## Infrastructure To Preserve

| System | Current Direction |
|---|---|
| Domain | preserve `immiforyou.com` |
| Delivery layer | preserve Cloudflare zone and edge layer where possible |
| Production repository | preserve `lbing2181-sudo.github.io` as `v1` live system |
| Rebuild repository | use `immiforyou-v2` for `v2` implementation |
| Control layer | keep `2026Codex` as planning and memory system |
| Subscriber data | preserve current Supabase project where schema remains compatible |
| Diagnosis backend | preserve Worker-backed protected integration boundary |
| Analytics | prioritize Google stack; keep Baidu only as low-priority compatibility |
| SEO-critical URLs | preserve where possible during cutover |

## Analytics And Distribution Freeze

| Layer | Decision |
|---|---|
| Search priority | Google-first |
| Primary analysis | GA / GSC |
| Distribution priority | X, Xiaohongshu, Zhihu, WeChat |
| Baidu | compatibility only, not a core growth bet |

## What V1 Is Allowed To Change During M0

| Allowed | Not Allowed |
|---|---|
| normal content publishing | large structural rewrites |
| urgent production bug fixes | new monetization systems in `v1` |
| factual content correction | expanding random new page classes |
| route-safe SEO maintenance | turning `v1` into a second rebuild track |

## M0 Checklist

| Status | Task | Intent |
|---|---|---|
| `done` | freeze `v1` operating rule in project memory | stop scope drift |
| `done` | freeze startup boot path for future threads and future AI handoff | defend against memory compression |
| `done` | freeze the new D61 deep-content rule as a `v2` planning constraint | stop accidental return to slim templates |
| `done` | record the final route inventory from production repo and live sitemap | define page parity target |
| `done` | record page-template classes from `v1` | define `v2` template scope |
| `done` | record all external integrations and boundaries | prevent migration omissions |
| `done` | record SEO-visible assets and route rules | protect cutover stability |
| `done` | mark what stays out of `v2` first batch | defend against overbuilding |
| `done` | confirm freeze review with user | unlock `M1` |

## Exit Criteria For M0

`M0` is complete only when all of the following are true:

| Condition | Meaning |
|---|---|
| route inventory is written | we know what `v2` must cover |
| template classes are written | we know what `v2` must standardize |
| integration boundaries are written | we know what must be preserved |
| content-depth baseline is written | we know what the new templates must physically support |
| exclusion list is written | we know what not to build yet |
| startup protocol is locked | future threads can recover quickly |
| user has reviewed the freeze | `M1` can start cleanly |

## M1 Entry Condition

After `M0` review is accepted, `M1` should begin with only these two outputs:

| Order | Output | Why |
|---|---|---|
| 1 | `v2` content model matrix | define what each page type must structurally carry |
| 2 | `v2` template matrix | define what each template class must render and share |

Do not start implementation before those two outputs exist.
