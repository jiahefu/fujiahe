# Design QA — FU JIAHE Homepage Directions v1

## Comparison Targets

### Direction A — Apple Executive

- Source visual truth: `/Users/jiahefu/.codex/generated_images/01a013c6-bb3b-75e1-9bae-7fe0304cd2fa/exec-bc15c3dc-4ada-4194-9626-fdeb21c3020b.png`
- Source pixels: 864 × 1821, 1× concept-board density.
- Implementation hero: `prototypes/qa/direction-a-desktop.jpg`
- Focused implementation region: `prototypes/qa/direction-a-work.jpg`
- Mobile evidence: `prototypes/qa/direction-a-mobile.jpg`
- Combined comparison: `prototypes/qa/comparison-a.jpg`

### Direction B — Editorial Leader

- Source visual truth: `/Users/jiahefu/.codex/generated_images/01a013c6-bb3b-75e1-9bae-7fe0304cd2fa/exec-1003e978-4efa-462a-aa45-87fd3f6ec62b.png`
- Source pixels: 862 × 1824, 1× concept-board density.
- Implementation hero: `prototypes/qa/direction-b-desktop.jpg`
- Focused implementation region: `prototypes/qa/direction-b-transformation.jpg`
- Mobile evidence: `prototypes/qa/direction-b-mobile.jpg`
- Combined comparison: `prototypes/qa/comparison-b.jpg`

### Direction C — Human Business Builder

- Source visual truth: `/Users/jiahefu/.codex/generated_images/01a013c6-bb3b-75e1-9bae-7fe0304cd2fa/exec-e25472eb-5e80-4945-bec2-1553a0f50262.png`
- Source pixels: 862 × 1824, 1× concept-board density.
- Implementation hero: `prototypes/qa/direction-c-desktop.jpg`
- Focused implementation region: `prototypes/qa/direction-c-about.jpg`
- Mobile evidence: `prototypes/qa/direction-c-mobile.jpg`
- Combined comparison: `prototypes/qa/comparison-c.jpg`

## Viewport And Normalization

- Desktop implementation CSS viewport: 1440 × 1000, browser screenshot density 1×.
- Mobile implementation CSS viewport: 390 × 844, browser screenshot density 1×.
- State: default, unauthenticated, top-of-page hero plus one direction-defining focused section.
- The ImageGen sources are compact, full-page concept boards rather than literal 1440px browser captures. For comparison, source and implementation hero crops were placed in equal 1.44:1 frames, aligned to the top. Focused source crops use the corresponding vertical region of the concept board and are paired with a 1440 × 1000 browser viewport of the implemented section.
- The full-view evidence is the hero pair for each direction. Focused evidence covers A's selected work, B's AI transformation hierarchy and C's About/personal layer, where typography, spacing and copy need to remain readable.

## Required Fidelity Surfaces

### Fonts And Typography

- A uses the requested large, restrained system-sans hierarchy and keeps the name on one line at desktop.
- B uses local Georgia plus Arial/Helvetica to preserve the editorial serif/sans contrast without remote fonts.
- C combines a bold system-sans name with Georgia story headings for a warmer voice.
- Mobile screenshots confirm readable wrapping without truncation or cramped display copy.

### Spacing And Layout Rhythm

- A preserves broad negative space, minimal section transitions and row-based work presentation.
- B preserves the numbered left rail, asymmetric columns and editorial rules.
- C preserves the portrait-led hero, parallel work narratives and prominent About section.
- Desktop and mobile browser metrics show `scrollWidth === clientWidth` for all three pages.

### Colors And Visual Tokens

- A: near-black, warm ivory and stone gray.
- B: warm paper, ink and muted rust.
- C: cream, charcoal, olive and terracotta.
- No purple/blue AI gradient, glass surface, giant shadow or generic SaaS treatment is present.

### Image Quality And Asset Fidelity

- All portrait instances use the supplied local `portrait.jpg`, preserve the subject and natural 2079 × 2952 source ratio, and render through `object-fit: cover` without distortion.
- A and C intentionally preserve the supplied gray studio background rather than synthesizing a cutout or new setting.
- No fake pet or lifestyle imagery is used.

### Copy And Content

- Hero positioning, selected-work titles and descriptions, six principles, AI-transformation hierarchy, About themes and WeChat handle match the approved brief.
- No company or employer names, exact metrics, testimonials, awards, results, résumé data or private phone details were added.
- Email remains a non-functional placeholder label because no approved public address was available.

### States, Interactions And Accessibility

- All internal navigation targets exist; representative anchor links in A, B and C were clicked and landed within approximately 16px of the target section.
- Each page has one `h1`, semantic sections, a primary navigation label, image alt text and a skip link.
- Keyboard focus testing produced a visible solid 3px outline in every direction.
- Browser-parsed `prefers-reduced-motion: reduce` rules set automatic scrolling and disable animation/transition behavior.
- Browser console inspection returned no page-originated warnings or errors.

## Comparison History

### Pass 1 — Blocked

- [P2] Portrait containers inherited default `figure` margins, leaving unintended white seams and weakening the edge-to-edge portrait treatment in all three hero designs.
- [P2] Direction A forced `FU JIAHE` onto two lines at desktop, materially changing the source's calm, horizontal executive hierarchy.

### Fixes

- Reset figure margins in A, B and C and slightly increased the in-container portrait crop so the supplied image fills the intended frame while preserving aspect ratio.
- Changed A's name treatment to a single-line, responsive display and rebalanced the supporting hero scale.

### Pass 2 — Passed

- Post-fix hero and focused-section comparisons are captured in `comparison-a.jpg`, `comparison-b.jpg` and `comparison-c.jpg` at the paths above.
- No actionable P0, P1 or P2 mismatch remains.

## Findings

No actionable P0/P1/P2 findings remain.

Accepted P3 differences:

- A's implementation retains the real gray portrait background rather than the source board's synthetic near-black cutout treatment.
- B omits the source board's diagonal portrait edge because the approved source asset is rectangular and no additional decorative asset was authorized.
- C omits the concept board's decorative principle icons, keeping the section text-led and avoiding unapproved or approximate icon assets.

These differences preserve asset integrity and the user's stated visual restrictions without weakening each direction's defining hierarchy.

## Open Questions

- Product Owner preference remains the only open design question: restrained executive minimalism (A), editorial authority (B), or warmer whole-person leadership (C).

## Implementation Checklist

- [x] Recreate all three selected visual directions as standalone pages.
- [x] Use only local/system fonts and the supplied portrait.
- [x] Validate desktop and mobile overflow, assets, navigation and focus.
- [x] Validate parsed reduced-motion behavior and console state.
- [x] Compare source and browser-rendered implementation in combined visual evidence.
- [x] Resolve all P0/P1/P2 findings.

## Follow-up Polish

- If A is selected, consider commissioning an approved transparent or dark-background portrait treatment.
- If B is selected, tune editorial density after real production copy is locked.
- If C is selected, keep the personal layer secondary as additional content is added.

---

# Design QA — Selected Production Candidate

## Findings

No actionable P0/P1/P2 findings remain.

Accepted P3 differences:

- The selected hero preserves the real gray studio background in `portrait.jpg` rather than synthesizing Direction A's dark-background cutout.
- System-font rendering may vary slightly by operating system; the tested hierarchy, wrapping and spacing remain stable at both target viewports.
- Mobile navigation uses concise labels for all five destinations so it remains available at 390px without overflow.
- The third Perspective extends beyond one 1000px desktop viewport because the statement is intentionally large; it remains fully readable through normal scrolling and is not clipped.

## Comparison Targets

- Written source specification: `/Users/jiahefu/.codex/attachments/7329177b-373c-4c5a-94a0-ba6f0b250f21/pasted-text-1.txt`.
- Direction A source implementation: `prototypes/qa/direction-a-desktop.jpg` and `prototypes/qa/direction-a-work.jpg`.
- Direction B source implementation: `prototypes/qa/direction-b-desktop.jpg` and `prototypes/qa/direction-b-transformation.jpg`.
- Direction C source implementation: `prototypes/qa/direction-c-desktop.jpg` and `prototypes/qa/direction-c-about.jpg`.
- Selected implementation hero: `prototypes/qa/selected-desktop.jpg`.
- Selected mobile hero: `prototypes/qa/selected-mobile.jpg`.
- Selected focused implementation regions:
  - `prototypes/qa/selected-thesis.jpg`
  - `prototypes/qa/selected-cases.jpg`
  - `prototypes/qa/selected-ai.jpg`
  - `prototypes/qa/selected-perspectives.jpg`
  - `prototypes/qa/selected-about.jpg`
  - `prototypes/qa/selected-closing.jpg`
- Selected focused mobile regions:
  - `prototypes/qa/selected-mobile-thesis.jpg`
  - `prototypes/qa/selected-mobile-cases.jpg`
  - `prototypes/qa/selected-mobile-perspectives.jpg`
  - `prototypes/qa/selected-mobile-about.jpg`
  - `prototypes/qa/selected-mobile-closing.jpg`
- Same-input comparison evidence:
  - `prototypes/qa/selected-vs-a.jpg`
  - `prototypes/qa/selected-vs-b.jpg`
  - `prototypes/qa/selected-vs-c.jpg`

## Viewport, State and Normalization

- Desktop implementation CSS viewport: 1440 × 1000; screenshot pixels: 1440 × 1000; density: 1×.
- Mobile implementation CSS viewport: 390 × 844; screenshot pixels: 390 × 844; density: 1×.
- Combined A/B/C comparison screenshots: 1600 × 1200 pixels at 1×.
- State: default, unauthenticated, static single-page homepage.
- Full-view evidence compares each source direction's hero with the selected hero in the same combined visual.
- Focused evidence compares A's leadership work framing with the selected thesis, B's editorial hierarchy with selected Perspectives, and C's About treatment with the selected About treatment.
- Additional focused implementation captures keep display copy, hierarchy, portrait treatment and responsive structure large enough to judge directly.

## Required Fidelity Surfaces

### Fonts and Typography

- The selected candidate is primarily rendered in the requested modern system sans-serif stack.
- Georgia appears only in the small supporting About note, preserving the 70/20/10 hierarchy rather than allowing B's serif identity to take over.
- The four brand-memory ideas have the largest and clearest typographic hierarchy.
- Desktop and mobile captures show intentional wrapping, no truncation and no cramped navigation text.

### Spacing and Layout Rhythm

- The hero, thesis and transformation sections preserve A's broad negative space and one-major-idea rhythm.
- Cases and Perspectives use B-style numbering and editorial rules without introducing cards or a publication masthead.
- About and Beyond Work add C's narrative depth without a repeated portrait or lifestyle layout.
- Browser metrics show `scrollWidth === clientWidth` at 1440px and 390px.

### Colors and Visual Tokens

- The palette remains near-black, warm ivory and restrained stone gray.
- Muted gray type and hairline rules provide hierarchy without rust, olive, terracotta or synthetic AI accent colors.
- No gradient, glass surface, heavy shadow, dashboard styling or generic SaaS component system is present.

### Image Quality and Asset Fidelity

- The only photographic instance uses `prototypes/assets/portrait.jpg` once.
- The browser reports a valid natural size of 2079 × 2952 and the layout preserves the source ratio through `object-fit: cover`.
- The supplied studio background is retained; no cutout, generated replacement, repeated portrait or placeholder pet imagery is used.
- The page uses no inline SVG, CSS illustration, emoji asset or remote image substitute.

### Copy and Content

- Hero, thesis, three case titles and descriptions, transformation hierarchy, three Perspectives, About themes, Beyond Work copy and contact copy match the selected brief.
- No employer names, company names, logos, metrics, results, awards, testimonials or unsupported details were added.
- The email remains an explicit pending placeholder and WeChat remains `Chat_Away`.

### States, Interactions and Accessibility

- All five primary navigation targets exist; the AI anchor was clicked and landed approximately 16px from the section start after smooth scrolling completed.
- The skip link points to the existing `main` element.
- One semantic `h1`, ordered section headings, navigation labeling, portrait alt text and landmark elements are present.
- A keyboard focus check on the wordmark produced `:focus-visible` with a solid 3px outline.
- Browser-parsed `prefers-reduced-motion: reduce` rules restore automatic scrolling and disable animation and transition behavior.
- Browser console inspection after navigation and responsive checks returned no page-originated warnings or errors.
- Browser inspection found no remote page assets.

## Comparison Assessment

### Selected vs Direction A

The selected candidate keeps A's strongest executive signals — the near-black hero, large sans-serif name, portrait treatment and restraint — while adding a high-impact leadership thesis and sharper viewpoint structure. The result is more memorable without reducing visual altitude.

### Selected vs Direction B

The selected candidate borrows B's useful hierarchy through subtle numbering, leadership-case framing and editorial Perspectives. It rejects B's full Georgia identity, rust system, monogram, masthead and self-quotation, so intellectual authority supports rather than replaces the executive identity.

### Selected vs Direction C

The selected candidate keeps C's deeper About narrative and human tone but removes the repeated portrait, lifestyle composition and warmer olive/terracotta system. Humanity is visible but remains secondary to the business positioning.

## Comparison History

### Selected Pass 1 — Blocked

- [P2] The Beyond Work section used a broad paragraph selector, causing the small editorial marker to inherit the large body-copy scale. The issue materially weakened the intended section hierarchy, including at the mobile breakpoint.

### Selected Fix

- Added a dedicated `.beyond-copy` class and scoped both the base and mobile type rules to that class, leaving `.section-marker` at its intended 0.68rem size.

### Selected Pass 2 — Passed

- Revised desktop and mobile closing captures confirm the marker and personal statement now retain separate hierarchy.
- Fresh hero, focused-section and A/B/C combined comparisons show no remaining actionable P0/P1/P2 mismatch.

## Implementation Checklist

- [x] Use Direction A as the dominant visual foundation.
- [x] Limit B and C contributions to the explicitly selected roles.
- [x] Preserve the four required brand-memory ideas.
- [x] Use the existing portrait once and no other photographic imagery.
- [x] Validate desktop and mobile overflow, navigation, assets, semantics, focus, reduced motion and console state.
- [x] Put each source direction and the selected implementation together in same-input comparison evidence.
- [x] Resolve all actionable P0/P1/P2 findings.
- [x] Preserve production files and existing A/B/C evidence.

## Follow-up Polish

- If a future approved portrait with a transparent or near-black background becomes available, it can be evaluated as a non-blocking visual refinement.
- Replace the public email placeholder only after the Product Owner supplies an approved address.

final result: passed
