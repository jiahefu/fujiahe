# v1.4 External Launch Defect & Evidence Closure

## Final classification

`V14_EXTERNAL_LAUNCH_DEFECTS_CLOSED_READY_FOR_HUMAN_GATE`

Mode: surgical fix + verification only. The approved visual direction and
locked content were preserved.

## A. Hero contrast

WCAG relative luminance contrast was calculated from the rendered computed
foreground/background colors on the 1440px homepage. No color change was
required because every intentional normal-size text treatment already passes
4.5:1.

| Text | Computed foreground | Background | Before | After |
| --- | --- | --- | ---: | ---: |
| `Strategy · AI Transformation · Enterprise Growth` | `rgb(208, 208, 204)` / `#d0d0cc` | `rgb(16, 17, 16)` / `#101110` | `12.2342:1` | `12.2342:1` |
| Hero explanation | `rgb(168, 169, 165)` / `#a8a9a5` | `rgb(16, 17, 16)` / `#101110` | `8.0053:1` | `8.0053:1` |
| AI supporting paragraph | `rgb(143, 141, 135)` / `#8f8d87` | `rgb(16, 17, 16)` / `#101110` | `5.7022:1` | `5.7022:1` |

No font size, layout, spacing, or copy was changed.

## B. Case Detail Skip Link

Root cause: Case Detail loaded its dedicated decision-model stylesheet without
the global skip-link rules. The anchor therefore rendered as a normal static
link at the top of the page.

Minimal fix:

- Added the standard off-canvas `.skip-link` / `:focus` pattern to
  `customer-growth-decision-model.css`.
- Added `tabindex="-1"` to Case Detail `<main id="main">` so the skip target is
  focusable after activation.
- Added a stylesheet version query to ensure the corrected CSS is fetched by
  the local preview browser.

Programmatic evidence at 390×844:

- Fresh load: `activeElement = BODY`; skip-link rect `x=12, y=-52.5,
  w=180.7656, h=43`; transform `translateY(-150%)`; not visible.
- First Tab: `activeElement.className = skip-link`, `href = #main`; rect
  `x=12, y=12, w=180.7656, h=43`; transform `translateY(0)`; visible and
  focused.
- Activation from the focused link reached `<main id="main" tabindex="-1">`,
  set `location.hash = #main`, and moved the viewport to the main target.

## C. Leadership Cases

Unchanged. The targeted 1440 screenshot shows the heading plus all three case
entries, readable copy, and separators in one frame.

## D. About / Formation

Unchanged. The targeted 1440 screenshot shows the complete identity statement,
full right-side narrative, UNSW image/caption, and HKUST image/caption in one
frame.

## E. Mobile

No visual regression or horizontal overflow was found. Targeted 390px captures
cover Hero + Thesis, the complete Featured Case 01, the AI thesis plus a
complete Twin Orbit view, and the About / Formation to Beyond transition.

At 390px, the following Twin Orbit labels are readable and non-overlapping:
`CUSTOMER ASSET`, `AI / AGENT`, `RISK & OPPORTUNITY`, `ROUTING`, `HUMAN
OWNERSHIP`, and `OPERATING LEARNING`.

## F. Performance

Repository image sizes:

| Asset | Bytes | Loading behavior |
| --- | ---: | --- |
| `portrait.jpg` | 447,081 | eager; `fetchpriority="high"` |
| `portrait-720.jpg` | 68,215 | selected through `srcset` |
| `portrait-960.jpg` | 118,707 | selected through `srcset` |
| `portrait-1280.jpg` | 222,360 | selected through `srcset` |
| `assets/v1.4/unsw-sydney.jpg` | 221,376 | `loading="lazy"` |
| `assets/v1.4/hkust-hong-kong.jpg` | 59,915 | `loading="lazy"` |
| `assets/v1.4/shelties-landscape.jpg` | 282,245 | `loading="lazy"` |

All images have explicit width/height attributes; the hero uses valid
`srcset`/`sizes`, and below-the-fold images use lazy loading where appropriate.
`LIGHTHOUSE_NOT_AVAILABLE` (no local Lighthouse executable; no toolchain was
installed solely for this audit).

## G. QA

- Homepage matrix passed at 1440×1000, 1280×900, 1024×900, 768×900,
  430×932, 390×844, 360×800, and 320×568.
- Case Detail matrix passed at 1440×1000, 1024×900, 768×900, 430×932,
  390×844, 360×800, and 320×568.
- Current browser checks: no horizontal overflow; all required sections present;
  initial skip-link state hidden at every Detail viewport; mobile Twin Orbit
  has no clipping or label overlap.
- Resource checks returned `200` for all public HTML/CSS, local v1.4 images,
  sitemap, robots, and CNAME resources.
- Public HTML/CSS contains zero temporary-worktree or prototype references.
- The site has no executable JavaScript bundle; the only script tag is JSON-LD.

## H. Remote boundary

`PUSH_BLOCKED_UNTIL_REMOTE_RECONCILIATION = TRUE`

No push, PR, merge, or deploy was performed.

## I. Local checkpoint

The surgical fix is ready for one new local checkpoint commit after this QA
pass. No remote operation is authorized by this task.

## Targeted review package

Exactly eight screenshots are in:

`/private/tmp/fujiahe-v1.4-clean-integration-review/EXTERNAL_LAUNCH_REVIEW/`

1. `01_HERO_CONTRAST_FINAL_1440.jpg`
2. `02_LEADERSHIP_CASES_CONTENT_1440.jpg`
3. `03_ABOUT_FORMATION_COMPLETE_1440.jpg`
4. `04_MOBILE_HERO_THESIS_390.jpg`
5. `05_MOBILE_FEATURED_CASE_390_TRUE_FULL.jpg`
6. `06_MOBILE_AI_TWIN_ORBIT_390_TRUE_FULL.jpg`
7. `07_CASE_DETAIL_SKIPLINK_INITIAL_390.jpg`
8. `08_CASE_DETAIL_SKIPLINK_FOCUSED_390.jpg`
