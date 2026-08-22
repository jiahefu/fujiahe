# v1.4 Integration Source Manifest

## Baseline provenance

- Production baseline commit: `dd4c085604c989d5282122e44d43c6c19688f29a`
- Production tree: `a4dd3faa81df71fc8a04b6dce90647531a5b698c`
- Local fallback commit: `b7e1c3af6a494e9f04f45319b52f8452c53f13eb`
- Local fallback tree: `a4dd3faa81df71fc8a04b6dce90647531a5b698c`
- Status: `CONTENT_EQUIVALENT_V1_3_BASELINE`
- Reason: Remote Git network unavailable in the Codex environment; external verification supplied the identical repository tree relationship.
- `MANDATORY_REBASE_ONTO_DD4C_BEFORE_PUSH = TRUE`

## Locked component lineage

| Logical component | Source absolute path | Source SHA-256 | Destination | Status | Adaptation | Internal structure |
| --- | --- | --- | --- | --- | --- | --- |
| Homepage locked integration (Profile → Contact) | `/private/tmp/fujiahe-v1.4-worktree/v14-current-locked-visual-integration-preview.html` | `ac9dabb03ea361f685eee73b27a316755571aa00baef1ded20f703cab2517f98` | `index.html` | Integrated | Preserved production metadata; changed only repository-local asset paths, canonical CTA route, and loading attributes | Unchanged |
| Case 01 Homepage Lite artifact | `/private/tmp/fujiahe-v1.4-worktree/featured-case-artifact-preview.html` | `9d66ea9b06927d26ca48f6221fafe06134806a17ce0ab4d868469fdff516650f` | Inline in `index.html` | Integrated | None beyond page integration | Unchanged |
| Case 01 Detail Full | `/private/tmp/fujiahe-v1.4-worktree/enterprise-growth-detail-artifact-preview.html` | `4cff93a0ec9011a15ff6b6205b5f8ee176e62adc74b3862d6330cc5a89ca57d1` | `cases/enterprise-growth/index.html` | Integrated | Added production metadata, accessible back link, and explicit 02 / JUDGMENT block; artifact markup retained | Artifact unchanged |
| Customer Growth Decision Model CSS | `/private/tmp/fujiahe-v1.4-worktree/customer-growth-decision-model.css` | `34b5e723b1aa2ca67ba9eca7ab1c5df6b0601fc30627ec2f004b2726448ccd46` | `customer-growth-decision-model.css` | Integrated | Added only Detail Full judgment copy styling | Structure unchanged |
| Twin Orbit CSS | `/private/tmp/fujiahe-v1.4-worktree/customer-os-twin-orbit.css` | `c41dcb8dadd2a7ff5affb12403e71d85f5562ba245c4fffbef79f40a0f855e17` | `customer-os-twin-orbit.css` | Integrated | None | Unchanged |
| Outer locked integration CSS | `/private/tmp/fujiahe-v1.4-worktree/v14-current-locked-visual-integration-preview.css` | `7ba34fad846d0b437a09c3a754be6fc93e277aac2c781defc2c998a29e33ea9e` | `v14-current-locked-visual-integration-preview.css` | Integrated | None | Unchanged |

## Production-intent image assets

| Logical asset | Source absolute path | Source SHA-256 | Destination | Dimensions | Adaptation |
| --- | --- | --- | --- | --- | --- |
| HKUST / Hong Kong | `/private/tmp/fujiahe-v1.4-worktree/beyond-work-preview-assets/01_HKUST_FINAL_PICK.jpg` | `94281661b5962bd86c93922332d89ea7769bd138d5011ebdf7ef86e59cc0f3e9` | `assets/v1.4/hkust-hong-kong.jpg` | 720×420 | Local copy; intentional CSS crop |
| UNSW / Sydney | `/private/tmp/fujiahe-v1.4-worktree/beyond-work-preview-assets/02_UNSW_FINAL_PICK.jpg` | `4e66ba903960dca02213365467134e6e54986c2be794fddd1e438518e6be9a02` | `assets/v1.4/unsw-sydney.jpg` | 1000×563 | Local copy; intentional CSS crop |
| Beyond Work Shelties | `/private/tmp/fujiahe-v1.4-worktree/beyond-work-preview-assets/03_SHELTIES_DOMINANT_LANDSCAPE.jpg` | `9d031851997b46054cf556b92048af51affb1ea100e3d309f470192e3380c671` | `assets/v1.4/shelties-landscape.jpg` | 1465×1096 | Local copy; one landscape image, intentional crop |

No review screenshots or prototype-only images are copied into the integration repository.
