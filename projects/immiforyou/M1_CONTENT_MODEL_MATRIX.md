# IMMIFORYOU M1 CONTENT MODEL MATRIX

## Purpose

This file defines what each major `v2` page class must structurally carry before template implementation begins.

It is the first required output of `M1`.

## Modeling Principle

- model content before code
- model depth before layout polish
- preserve SEO-critical semantics
- preserve diagnosis as a primary service-entry capability
- design for long-form density by default

## Page Class Matrix

| Page Class | Core Role | Required Content Blocks | Structured Fields | Notes |
|---|---|---|---|---|
| Home | orientation and discovery | hero, value proposition, search, country discovery, news freshness signal, diagnosis entry, trust signal | seo title, seo description, hero copy, primary nav groups, featured destinations, featured news, trust stats | homepage is not a blog index; it is the system entry |
| News List | freshness and discovery | page intro, article cards, tag/topic grouping, recency cues | seo title, seo description, list items, card summaries, article dates, tags | must support deep-content article discovery without looking crowded |
| News Article | search traffic and authority depth | article header, author block, summary, deep body, section hierarchy, tables, persona impact, FAQ, official sources, related links | slug, title, excerpt, publish date, modified date, author chinese name, author english name, author coverage region, country tags, topic tags, body, table blocks, faq items, persona impact, official sources, schema fields | default assumption is `D61` long-form depth |
| Country Detail | trust, comparison, and path education | hero, positioning summary, pathway breakdown, requirements, cost/timeline, comparison tables, persona-fit interpretation, FAQ, official links, auto-aggregated related news, disclaimer | slug, chinese name, english name, region, teaser, pathways, requirements, costs, timelines, comparison tables, persona slices, faq items, official links, last verified at, related news feed, seo fields | this is the core evergreen page class; keep it mostly static except the related-news layer |
| Diagnosis | service-entry and conversion | intro, questionnaire shell, qualification framing, loading state, result shell, payment boundary placeholder, trust / disclaimer layer | seo title, seo description, steps, question schema, scoring or routing config, result types, cta copy, worker adapter config | diagnosis logic stays behind protected backend boundaries |
| Membership | offer explanation and future monetization shell | offer framing, who it is for, benefit blocks, comparison with free layer, faq, call to action | seo title, seo description, offer sections, pricing placeholder, faq items, cta blocks | can stay commercially light in first batch but structure must be ready |
| About / Trust | brand trust and method | mission, method, why trust us, source discipline, non-legal-advice boundary, editorial discipline | seo title, seo description, trust blocks, methodology blocks, disclaimers | supports conversion indirectly through credibility |

## Shared Field Families

### SEO Fields

- `seo_title`
- `seo_description`
- `canonical_path`
- `og_title`
- `og_description`
- `og_type`

### Freshness Fields

- `published_at`
- `updated_at`
- `last_verified_at`

### Source Fields

- `official_sources`
- `source_notes`
- `jurisdiction`

### Attribution Fields

- `author_chinese_name`
- `author_english_name`
- `author_coverage_region`

### Deep-Content Fields

- `section_blocks`
- `table_blocks`
- `faq_items`
- `persona_slices`

## Content Depth Rules By Class

| Page Class | Depth Expectation |
|---|---|
| Home | concise but layered; not long-form article depth |
| News List | concise summaries only |
| News Article | full `D61` long-form depth by default |
| Country Detail | deep evergreen depth, often equal to or greater than article depth |
| Diagnosis | concise interface copy plus rich result logic and explanation layers |
| Membership | concise to medium depth, focused on clarity and trust |
| About / Trust | medium depth with strong credibility density |

## Content Classes Needed In V2 Data Layer

| Content Class | Purpose |
|---|---|
| `site_page` | homepage, about, membership, and other static trust pages |
| `news_article` | policy news and comparative analysis articles |
| `country_profile` | evergreen country and region pages |
| `diagnosis_config` | questionnaire and result routing support |

## Country Detail Update Policy

Country-detail pages should be treated as mostly static evergreen assets.

| Area | Update Mode |
|---|---|
| pathway explanation | static-first |
| requirements and process explanation | static-first |
| cost / timeline baseline | static-first with periodic review |
| official-link block | static-first with periodic review |
| related-news aggregation block | dynamic or auto-aggregated |

This means the main country page should not depend on constant full-manual rewriting.
The living layer should concentrate in the related-news aggregation block.

## Entry To Template Matrix

After this file is reviewed, the next required file is:

- `M1_TEMPLATE_MATRIX.md`

That file should answer:

- what each template renders
- which blocks are shared
- which blocks are optional
- which blocks depend on structured fields from this matrix
