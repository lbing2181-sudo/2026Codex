# WORKING_MEMORY

## Current Stage

- Project entry created inside `2026Codex`
- Active for `v2` rebuild planning
- `v1` remains live
- `immiforyou-v2` repository has been created
- `v1` development work is paused except content publishing and urgent fixes
- `M0` has been reviewed and passed
- `M1` is active
- Local `immiforyou-v2` scaffold work has started
- Core `v2` entry pages now have real local implementations:
  home, news list, news article, country detail, diagnosis, membership, about
- The trust layer is no longer only skeletal:
  about now expresses team-first trust, operating disciplines, and official-source boundary
- News article pages now behave more like system nodes:
  they carry tags, role explanation, and internal country-page linkage
- The latest `v1` editorial and country-page standards have been reread locally from the source repository
- `v2` country detail pages are now moving closer to the proven `v1` standard:
  static-first body, quick-jump navigation, fit/not-fit framing, process section,
  fee reference section, and internally authored updates only
- News article pages now include reading-time metadata,
  aligning more closely with the validated `v1` editorial structure
- Country detail pages now include an explicit source-and-boundary disclaimer section,
  aligning more closely with the validated `v1` trust layer
- Shared `v2` content cards now exist for article previews and country discovery cards
- Homepage now includes a true country-discovery layer instead of only explanatory panels
- `v2` now has three country examples live locally:
  Canada, Portugal, and the United States
- Country-page scope is now re-tightened:
  the United States page is the only active canonical template baseline
  until its structure is considered stable enough to copy

## Current Focus

- preserve the approved `M0` freeze state
- use the approved content model and template matrix as the scaffold base
- expand the Astro-based `v2` structure carefully
- avoid visual overcorrection while the first batch is still structural
- move repeated page structure into shared content components
- keep legacy `.html` route compatibility as a later cutover task,
  not as a scaffold-stage constraint
- keep country pages static-first with internal-original related-news aggregation only
- keep diagnosis positioned as a core future service entry,
  while payment productionization remains out of scope for the first batch
- keep membership intentionally light:
  structure first, hard selling later
- let about and article pages explain the system itself,
  not just act as placeholder pages
- keep rebuilding from validated `v1` logic where it is strong,
  while moving those rules into cleaner reusable `v2` structure
- treat example countries as reusable pattern checks,
  not as isolated one-off mockups
- stop broad country expansion for now;
  improve the U.S. page first, then propagate
- keep a reserved account entry in the first-batch architecture,
  but delay real auth implementation until the service and membership layers are ready
- let visual refinement become slightly more international and fluid,
  while staying recognizably close to `v1` in tone and trust
- keep diagnosis, account, and membership connected as one future flow,
  instead of letting them drift into isolated pages
- let country pages start acting as guidance pages,
  not only information repositories:
  next-step sequencing should now sit above dynamic article aggregation
- keep country pages dense enough to communicate real decision pressure;
  do not flatten them into brochure-style clarity that hides the complexity users actually face
- treat document backtesting as active maintenance work:
  when new direction is confirmed,
  scan lower-level files and clean stale or reversed language
- keep the charging narrative singular for now:
  open platform publicly,
  `移民路径诊断` as the current paid service,
  membership reserved for later
- keep membership visibly secondary in the current product story:
  reserved for future continuity,
  not competing with the current paid diagnosis service
- keep the diagnosis page moving from concept-page to real paid-service page:
  clarify intake, deliverable, and explicit scope boundary
- keep pushing the diagnosis page toward visible service realism:
  show questionnaire structure, report structure, and fit boundary,
  not just abstract service language
- let the diagnosis page start showing interface-level previews,
  so users can picture the questionnaire and report before implementation is wired
- make the U.S. page show verification method explicitly:
  source hierarchy, update logic, and cleaned/modelled data pipeline should become visible trust signals
- make country-page status visible too:
  last verification date, dynamic-layer scope, and refresh cadence should be explicit
- let country pages surface recent tracked changes too:
  not only state and method, but the specific kinds of change currently being watched in the article layer
- let the canonical U.S. page start showing persona slices too:
  not as marketing personas,
  but as real applicant situations that help users locate themselves faster
- let the canonical U.S. page also expose a first-pass decision framework:
  users should be able to see the order of judgment,
  not only the names of pathways and the final service CTA
- let the canonical U.S. page surface evidence reality more directly too:
  U.S. complexity is often about proof strength, material organization,
  and whether a long narrative can actually stand up
- let the canonical U.S. page expose readiness self-check too:
  users should be able to see whether they are still scattered,
  roughly aligned, or close to a truly organized submission narrative
- let the canonical U.S. page call out common mistakes too:
  users should be shown where judgment often goes wrong,
  not only where the “correct” path might begin
- let the canonical U.S. page keep one calmer orientation layer too:
  a short first-look summary should help users enter the page
  before they sink into the heavier sections
- let the canonical U.S. page expose a driver matrix too:
  users should be able to align their strongest real-world condition
  with a likely starting direction before deeper judgment begins
- begin the refinement phase after the first scaffold checkpoint:
  stop adding more country-page content by default,
  extract heavy judgment sections into reusable components,
  and reduce page-file sprawl before further design work
- keep the U.S. country page from becoming an endlessly expanding page:
  retain deeper judgment data in the content model,
  but render only the strongest decision layers by default
  until progressive disclosure or account-level continuity is designed

## Current Rule

- use GitHub repo and live site as primary references
- keep the first batch focused on structure, parity, and maintainability
- treat deep long-form content as the default content shape,
  not as an optional premium enhancement
- keep the first visual pass close to `v1` temperament:
  calm, clear, reading-first, and not overdesigned
- reserve room for future registration/login without pushing sign-in before it is useful
- keep the first commercial path sequence clear:
  diagnosis entry -> account continuity -> membership/service depth
- keep document hierarchy strict:
  upper-level rules suppress lower-level files unless the upper level is changed first
- country-page refinement is now subtraction-first:
  visible density should come from fewer stronger blocks,
  not from rendering every available internal judgment field
- country-page componentization has started:
  process, pathway comparison, preparation checklist, and fee table
  should live as reusable content components,
  not as one-off blocks embedded in the route file
- public-facing pages should not expose internal rebuild language:
  remove `v2`, `scaffold`, `template status`, and similar development labels
  from visible UI copy before treating a page as product-facing
- homepage copy is now user-first:
  it should guide users through country discovery,
  policy reading, and immigration path diagnosis,
  instead of explaining the internal rebuild process
- homepage entry structure now uses three clear action cards:
  country path discovery,
  policy news reading,
  and immigration path diagnosis
  should remain the primary first-click sequence
- diagnosis page has entered a subtraction-first service-page structure:
  keep definition, three-step experience, interface preview,
  launch entry, price boundary, fit boundary, account continuity,
  and trust boundary;
  avoid repeating questionnaire/report/deliverable explanations in multiple sections
- policy news pages should read as an active content system:
  avoid `sample`, `future`, and internal role-explanation language
  in public article summaries and news index copy;
  present articles as real judgment support and country-page dynamic inputs
- account and membership pages should be product-facing:
  account is the user judgment center for diagnosis records,
  saved countries, policy tracking, and membership state;
  membership is a public service explanation with purchase currently closed,
  not an internal roadmap or placeholder page

## Primary Planning File

- `M0_V1_FREEZE_CHECKLIST.md`
- `V2_REBUILD_PLAN.md`
- `REPO_STRATEGY.md`
- `M1_CONTENT_MODEL_MATRIX.md`
- `M1_TEMPLATE_MATRIX.md`
