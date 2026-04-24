# DECISIONS

## 2026-04-19

- The repository `lbing2181-sudo/lbing2181-sudo.github.io` and live site `immiforyou.com` are now registered inside `2026Codex` as a formal project entry.
- The project is connected for future work but is not yet active for execution.
- When work begins, GitHub repository content and live site state should be treated as primary sources.
- Policy, eligibility, and process claims must be verified against official government sources before being used operationally.
- Before formal takeover, the latest repository content and live site state must be reread and synchronized into the control-layer understanding before execution starts.

## 2026-04-22

- `immiforyou` enters `v2` rebuild planning mode.
- The rebuild strategy is parallel:
  keep `v1` live while `v2` is rebuilt separately.
- The correct migration principle is:
  preserve infrastructure, replace the application layer.
- Stable systems should be reused when possible:
  domain, Cloudflare layer, Supabase project, Worker-backed diagnosis boundary, analytics, and verification wiring.
- `v2` should become template-driven and modular, not a continuation of page-by-page handcrafted growth.
- Payment productionization is explicitly excluded from the first `v2` rebuild batch.
- Repository strategy is now fixed:
  `lbing2181-sudo.github.io` remains the live production repository,
  `immiforyou-v2` should be created as a separate private rebuild repository,
  and `2026Codex` remains the control layer.
- The private rebuild repository now exists:
  `https://github.com/lbing2181-sudo/immiforyou-v2`
- `2026Codex` should track `immiforyou-v2` as the implementation target for all future `v2` work.
- `v1` development is now paused except for normal content publishing and urgent live fixes.
- Subscription and payment should not be activated in `v1`;
  monetization waits for `v2`.
- The diagnosis capability itself is not deferred:
  the Worker-backed AI diagnosis path remains a preserved core product capability,
  and is expected to become a primary monetization entry in `v2`.
- Analytics and search priority should be:
  Google Search, GA, and GSC first;
  X, Xiaohongshu, Zhihu, and WeChat as external distribution;
  Baidu only as low-priority compatibility.
- Memory-compression defense is now a project rule:
  every new thread or future AI handoff must start from the repository boot path,
  not from chat memory.
- The current phase-control file is now:
  `M0_V1_FREEZE_CHECKLIST.md`
- The latest production repository state is verified at commit:
  `a424f15`
- Content depth is now a hard rebuild constraint:
  `D61` replaces the old `D51` slim-content direction.
- `v2` must be designed for deep long-form content by default,
  not compact content by default.
- For planning purposes, the active editorial baseline is now:
  3000-5000 Chinese characters per article,
  6-9 H2 sections,
  required H3 depth,
  large tables,
  multiple persona slices,
  and stronger official-source density.
- This means `v2` template and content-model work must preserve space for depth,
  not optimize around short-form publishing convenience.
- `M1` has now moved from abstract planning into scaffold work.
- The first `v2` application scaffold is now being built inside the real
  `immiforyou-v2` repository cloned into the local workspace.
- The initial implementation direction is Astro-based:
  static-first, template-friendly, and suitable for content-heavy public pages
  with limited interactive islands later.
- `v2` visual continuity is now explicit:
  the first batch should preserve the calm, reading-first feel of `v1`
  instead of forcing a drastic redesign.
- The first implemented `v2` page set now covers:
  home, news list, news article, country detail, diagnosis, membership, and about.
- The homepage should function as a true decision-entry layer,
  not as a blog-style article dump.
- Country detail pages are now fixed as static-first evergreen pages,
  with only one dynamic layer:
  internally authored related-policy articles aggregated from the site's own news corpus.
- Diagnosis pages must stay explainable and bounded:
  preserve the Worker-backed capability,
  reject "mystical AI" framing,
  and structure the experience as intake -> judgment -> explained next step.
- Membership should remain commercially restrained in the first batch:
  preserve the shell for future monetization,
  but do not turn the page into a hard-sell surface before the value layer is mature.
- About / Trust must evolve beyond a placeholder:
  it should explain team-first trust, operating discipline,
  official-source priority, and non-legal-opinion boundary.
- News article pages should not behave like isolated posts:
  they should visibly connect article depth, author responsibility,
  and country-page aggregation logic into one system story.
- `v2` implementation is not greenfield invention:
  when `v1` already contains mature rules for article structure or country-page logic,
  those rules should be reread and translated into cleaner `v2` templates instead of being ignored.
- The `v1` content workflow has now been reaffirmed as the article-writing baseline:
  deep long-form articles, author block, timestamps, FAQ, official sources,
  and decision-support framing remain core.
- The `v1` country-page standard has now been reaffirmed as the page-structure baseline:
  quick section navigation, static-first evergreen body, fee tables,
  FAQ, and internally aggregated updates as the only dynamic layer.
- `v2` article pages should carry explicit reading-time metadata,
  not just author and timestamp metadata.
- `v2` country pages should carry an explicit source-and-boundary disclaimer section,
  so trust and legal boundary are visible on the page itself instead of being implicit.
- Repeated preview cards should now be componentized instead of copied page by page:
  article-preview cards and country-discovery cards are now shared building blocks.
- The homepage should now surface country discovery directly,
  not only describe the idea of country discovery in text.
- The first multi-country local examples are now:
  Canada, Portugal, and the United States.
  Their purpose is to validate reusable country-page structure across different decision styles,
  not to create isolated showcase pages.
- Country-page execution is now narrowed again:
  the U.S. page is the only canonical template to actively refine.
  Canada and Portugal remain as secondary reference samples,
  but broad country expansion is paused until the U.S. template is stable.
- The `v2` information architecture now reserves a formal account layer:
  add a visible `/account/` entry now,
  but do not connect real authentication or force sign-in in the first batch.
  This layer is reserved for future registration, login, membership state,
  diagnosis history, and saved user pathways.
- The first visual refinement direction is now clarified:
  move the interface toward a more international and fluid feeling,
  closer to high-end product sites,
  but preserve the calm, restrained, reading-first temperament already validated in `v1`.
- The reserved account layer is no longer only a route placeholder:
  it now has visible navigation presence
  and is explicitly connected to diagnosis and membership logic.
  The intended future order is:
  low-friction diagnosis first,
  account-based history and saved state later,
  then deeper membership and service continuity.
- Country pages should now begin to carry an explicit action sequence,
  not only static information and related articles.
  The intended right-rail order is:
  next-step guidance first,
  then internally authored related-news updates.
- Country pages should not be optimized into false simplicity:
  they must preserve enough real information density and decision pressure
  for users to feel the complexity of the choice itself.
  The goal is not to manufacture confusion,
  but to let true complexity surface clearly enough that diagnosis becomes a natural next step.
- The country-page density principle now includes two explicit structural layers:
  a pathway-comparison matrix
  and a practical preparation checklist.
  These should increase decision weight through real comparison and execution guidance,
  not through visual clutter.
- Country pages should now also surface verification method more visibly:
  make source hierarchy, dynamic-update handling, and cleaned/modelled data workflow legible,
  so professionalism is shown through method, not only claimed in copy.
- The canonical U.S. page should now begin surfacing persona slices as a first-class layer:
  not as abstract marketing personas,
  but as concrete applicant situations that help users identify their likely decision context earlier.
  This layer should support real self-location and decision pressure,
  not reduce complexity into oversimplified audience labels.
- The canonical U.S. page should now also surface a first-pass decision framework:
  make users confront the order of judgment directly
  through key questions, why they matter, and common misjudgments.
  This should help country pages behave more like real decision pages,
  not only dense information containers.
- The canonical U.S. page should now also surface evidence reality explicitly:
  make proof strength, material organization,
  and long-form narrative pressure visible as first-order decision factors.
  This is especially important for U.S. pathways,
  where user difficulty often comes from evidence structure rather than only route names.
- The canonical U.S. page should now also expose readiness self-check:
  let users see whether they are still in scattered exploration,
  early alignment,
  or near-submission narrative formation.
  This should turn the country page from passive explanation
  into a more active decision-orientation surface.
- The canonical U.S. page should now also call out common mistakes explicitly:
  country pages should not only explain routes and pressures,
  but also name the recurring judgment errors that mislead users early.
  This supports correction, not just information density.
- The canonical U.S. page should keep a calmer orientation layer near the top as well:
  before users enter the dense judgment blocks,
  give them a short first-look summary of the 2-3 variables that matter most.
  This is not simplification into brochure language;
  it is an entry ramp into density.
- The canonical U.S. page should now also expose a driver matrix:
  map users' strongest real-world condition
  to a likely starting direction and a corresponding caution.
  This should help users stop guessing from route names alone.
- After the first scaffold checkpoint, the work should move into refinement:
  avoid adding more country-page content by default,
  extract heavy judgment sections into reusable components,
  and reduce page-file sprawl before continuing visual or content expansion.
- Document governance is now explicit for this project:
  upper-level control files must suppress lower-level files,
  stale or reversed lower-level instructions should be revised or deleted,
  and document backtesting is required whenever a major direction changes.
- The diagnosis concept is now fixed more precisely:
  `开始诊断` is only the CTA,
  and the actual product is `移民路径诊断`.
  It is the single clearly defined paid service entry for now,
  priced at 599 RMB per use.
- Public positioning and service positioning must stay separate:
  the site remains an open information platform externally,
  while `移民路径诊断` remains a distinct paid report service.
- External wording should avoid `AI诊断`:
  internal implementation may use DeepSeek,
  but outward-facing language should use `自研移民大模型`.
- Current monetization order is now fixed more clearly:
  keep the public platform open,
  keep `移民路径诊断` as the single active paid service entry,
  and keep membership as a reserved future layer rather than a second immediate paid narrative.
- The diagnosis service definition is now clearer:
  the paid unit is one structured diagnosis report,
  including intake, path prioritization, risk alerts, and next-step guidance.
  It does not include legal representation, materials outsourcing,
  filing execution, or outcome guarantees.
