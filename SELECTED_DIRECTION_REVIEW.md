# FU JIAHE — Selected Homepage Direction Review

## Decision

The selected production candidate uses Direction A as the visual foundation, with a deliberately limited contribution from Directions B and C:

- **70% Direction A — Apple Executive:** hero, near-black and warm-neutral palette, whitespace, modern system sans-serif, portrait treatment, executive altitude and restrained motion.
- **20% Direction B — Editorial Leader:** subtle section numbering, leadership-case framing, stronger viewpoint hierarchy and the editorial rhythm of Perspectives.
- **10% Direction C — Human Business Builder:** a deeper About narrative, a restrained personal layer and a slightly warmer human tone.

This is not an averaged visual mixture. Direction A still controls the first impression and overall system. B and C are used only where they solve a specific weakness in A: B makes the point of view more memorable, while C adds enough personal context to build trust.

## Production-Candidate Storyline

The page is organized around four ideas the visitor should remember:

1. **FU JIAHE**
2. **Building businesses for the AI era.**
3. **Execution is getting cheaper. Judgment is not.**
4. **Tools don't transform businesses. Workflows do.**

Every other section supports those four ideas:

- The hero establishes identity, positioning and business territory.
- The leadership thesis creates one high-impact statement about judgment in the AI era.
- Three leadership cases demonstrate how that judgment is applied without adding unsupported outcomes.
- AI Transformation moves the discussion from tools to workflows, operating model, people and business outcomes.
- Perspectives reduces six equal principles to three prioritized viewpoints.
- About explains the path from engineering to business building without becoming a résumé timeline.
- Beyond Work adds a single text-led human note without repeating the portrait.
- Contact keeps the public email explicit as pending and preserves WeChat `Chat_Away`.

## Why This Is Stronger

### 1. Executive Altitude

The selected candidate keeps A's near-black hero, large sans-serif name, disciplined palette and broad negative space. It therefore reads first as a senior business leader's page, not as a magazine, résumé, blog or SaaS landing page. The numbered sections are small navigational signals rather than a dominant editorial device.

### 2. Memorability

Direction A was visually clear but depended heavily on the hero and work list. The selected version adds two large, standalone ideas — the Leadership Thesis and AI Transformation statement — so the page has a stronger verbal memory structure without adding visual noise.

### 3. Intellectual Authority

B's most useful contribution is not its serif styling; it is its ability to frame work and viewpoints as leadership judgment. The selected candidate borrows that structure through numbered cases, a clear transformation hierarchy and three prioritized Perspectives, while retaining A's modern, executive identity.

### 4. Humanity

C showed that a fuller About story can make the professional positioning more credible and relatable. The selected version keeps that depth but removes the repeated portrait and lifestyle-led presentation. The personal note remains brief, specific and text-only.

### 5. Simplicity

The candidate reduces competing devices: one portrait, one primary type system, three core neutral colors, three cases, three viewpoints and no card grid. It avoids B's full masthead/monogram/serif/rust system and C's olive/terracotta/lifestyle language. The result is easier to scan and easier to maintain as a production homepage.

## Direction-by-Direction Comparison

### Versus Direction A

What remains:

- executive near-black hero;
- warm ivory and stone supporting fields;
- modern system sans-serif;
- oversized type and generous whitespace;
- restrained portrait and motion treatment.

What improves:

- the Leadership Thesis creates a more memorable second beat;
- cases read as leadership decisions rather than generic portfolio work;
- three Perspectives add a sharper point of view;
- About carries more human context without changing the overall altitude.

Visual evidence: `prototypes/qa/selected-vs-a.jpg`.

### Versus Direction B

What is retained:

- selective numbering;
- editorial hierarchy for cases and viewpoints;
- a clearer sense of intellectual authority.

What is intentionally rejected:

- a Georgia-led identity;
- rust as the dominant accent;
- the FJ monogram and publication-style masthead;
- self-quotation styling;
- an overall strategy-journal feeling.

The candidate has B's judgment structure without allowing editorial styling to overtake the personal executive identity.

Visual evidence: `prototypes/qa/selected-vs-b.jpg`.

### Versus Direction C

What is retained:

- a fuller career narrative;
- a warmer, more personal tone;
- a specific but restrained Beyond Work layer.

What is intentionally rejected:

- olive and terracotta as the main palette;
- repeated use of `portrait.jpg`;
- lifestyle-blog composition;
- the line “Let's build what's next.”

The candidate keeps C's humanity without allowing personal content to weaken the business positioning.

Visual evidence: `prototypes/qa/selected-vs-c.jpg`.

## Visual and Content Guardrails Preserved

- No employer or company names.
- No logos, fake metrics, fake outcomes, testimonials or unsupported detail.
- No résumé timeline or résumé download.
- No remote fonts, remote assets, trackers or frameworks.
- No generic AI illustration, dashboard language, glassmorphism or repeated cards.
- `portrait.jpg` appears once and retains its real studio background.
- Public email remains an explicit placeholder until approved.
- Production `index.html`, `CNAME`, GitHub Pages and `main` remain untouched.

## Validation Summary

The candidate was visually inspected in the in-app browser at:

- 1440 × 1000 desktop, 1× screenshot density;
- 390 × 844 mobile, 1× screenshot density.

Validated:

- no horizontal overflow at either viewport;
- responsive hero, case, transformation, perspective, About and contact layouts;
- all navigation targets exist and a representative anchor lands within approximately 16px of its section;
- one semantic `h1` and ordered section headings;
- visible 3px keyboard focus treatment;
- parsed reduced-motion rules disable animation/transitions and restore automatic scrolling;
- the portrait loads once at its natural 2079 × 2952 dimensions;
- no remote page assets;
- no page-originated console warnings or errors.

Detailed evidence and the comparison history are in `design-qa.md` and `prototypes/qa/`.

## Accepted Trade-offs

- The real portrait retains its gray studio background instead of using a synthetic dark cutout. Asset integrity is more important than forcing a visual effect.
- The exact system font rendering can vary slightly by operating system; the hierarchy and spacing are designed to remain intact.
- The mobile navigation uses shortened labels to fit at 390px while keeping all five destinations available.
- Long-form viewpoint copy extends below a single viewport, but it remains fully readable through normal page scrolling and is not clipped.

## Product Owner Decision

The remaining decision is whether this selected candidate is approved to replace the production homepage in a separate implementation step. Approval should be based on whether the page makes the four brand-memory ideas clear while balancing executive authority, point of view and a restrained human layer.

This branch is review-only. No production replacement, publication, Pull Request or merge is part of this delivery.
