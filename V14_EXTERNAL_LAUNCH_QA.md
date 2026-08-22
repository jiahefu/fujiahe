# v1.4 External Launch QA

## Final classification

`V14_LOCAL_INTEGRATION_READY_FOR_EXTERNAL_REVIEW`

This is a local, content-equivalent integration baseline. GitHub was unavailable
for remote reconciliation during this run.

## Baseline and safety boundary

- `BASELINE_MODE: CONTENT_EQUIVALENT_LOCAL_FALLBACK`
- Production target commit: `dd4c085604c989d5282122e44d43c6c19688f29a`
- Production target tree: `a4dd3faa81df71fc8a04b6dce90647531a5b698c`
- Local fallback commit: `b7e1c3af6a494e9f04f45319b52f8452c53f13eb`
- Local fallback tree: `a4dd3faa81df71fc8a04b6dce90647531a5b698c`
- `PUSH_BLOCKED_UNTIL_REMOTE_RECONCILIATION: TRUE`
- No push, pull request, merge, or deploy was performed.
- The existing development clone was not modified; all work was isolated to
  `feature/site-v1.4-integration` at `/private/tmp/fujiahe-v1.4-integration-worktree`.

## Integrated surface

- Homepage: locked Leadership Thesis, Case 01 homepage-lite artifact, Twin Orbit
  AI surface, PMF perspective copy, About / Formation, and Beyond single-image
  treatment.
- Case detail: locked Detail Full artifact with explicit Context, Judgment,
  What Changed, My Role, and Validation sections.
- Local production-intent assets:
  `assets/v1.4/hkust-hong-kong.jpg`, `assets/v1.4/unsw-sydney.jpg`, and
  `assets/v1.4/shelties-landscape.jpg`.
- The public HTML/CSS contains zero `/private/tmp` or prototype-worktree refs.

## Responsive QA

All rows passed overflow, clipping, section-order, copy, artifact readability,
image loading, and zero-console-error checks.

| Surface | Viewports | Result |
| --- | --- | --- |
| Homepage | 1440×1000, 1280×900, 1024×900, 768×900, 430×932, 390×844, 360×800, 320×568 | PASS |
| Case Detail | 1440×1000, 1024×900, 768×900, 430×932, 390×844, 360×800, 320×568 | PASS |

Additional Detail checks passed: four customer-signal cells, mobile signal
indexes hidden at widths ≤390px, three compact outcome paths, and the next-
decision note.

## Semantic and content assertions

- Case primary exact count: `1`
- Case secondary exact count: `1`
- PMF exact phrase (`product–market fit`) count: `1`
- AI thesis exact count: `1`
- AI supporting sentence exact count: `1`
- Locked Case 01 present: `TRUE`
- Locked AI surface present: `TRUE`
- Stale AI copy present: `FALSE`
- Old Case primary present: `FALSE`
- Second Sheltie image present: `FALSE`
- Temporary-path refs in public HTML/CSS: `0`

## Browser, resource, and navigation checks

- Homepage and Detail Full each reported zero console errors, warnings, and
  console entries at every QA viewport.
- HTTP resource checks returned `200` for `/`, all three component stylesheets,
  all three local v1.4 images, `/cases/enterprise-growth/`, `/sitemap.xml`,
  `/robots.txt`, and `/CNAME`.
- Local CTA navigation reached
  `/cases/enterprise-growth/` with title `Reframing Enterprise Customer Growth — Fu Jiahe`.
- Local back navigation returned to `/#featured-case` with title
  `Fu Jiahe — AI Strategy, Transformation & Enterprise Growth`.
- Skip links, semantic landmarks/headings, and visible focus styles are present
  in the integrated markup and styles.

## Review package

The review folder contains exactly nine JPEGs and no other files:

`/private/tmp/fujiahe-v1.4-clean-integration-review/FOR_CHATGPT_REVIEW/`

The local checkpoint commit is created after this QA pass; use `git rev-parse
HEAD` in the integration worktree for its final SHA.
