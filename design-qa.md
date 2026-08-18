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

- Post-fix hero and focused-section comparisons are captured in `comparison-a.png`, `comparison-b.png` and `comparison-c.png` at the paths above.
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

final result: passed
