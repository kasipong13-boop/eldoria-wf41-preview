# WF41-P19 — Natural Terrain Ramp (Design-only)

## Scope
Only `kasipong13-boop/eldoria-wf41-preview`, `main`, new standalone `r02-p19.html`. Previous P18 and playable preview files are untouched.

## Implementation
- New 256×224 low-resolution canvas pixel-art composition, displayed with nearest-neighbor scaling on iPhone.
- Integrated upper plateau, lower plateau, cliff faces and sloped dirt surface as connected polygonal terrain.
- Deterministic grass/stone/dirt pixel speckles and grassy shoulders.
- Removed P18's thick overlay bridge; P19 renders a single coherent visual study, not a stack of 3 sprites.
- Added guide toggle for illustrative H2/H1, zoom, drag, center and comparison link to P18.
- Design-only: no map coordinate validation, no collision, no walkable area unlock.

## QA
- GitHub commit: `cf6286895dd36980da17949cdec0d2f755ebb95e`.
- GitHub readback of `r02-p19.html`: PASS.
- JavaScript syntax: PASS.
- Existing playable `art.html` graph: 337 nodes / 416 edges: PASS, unchanged.
- No storage/Save Engine calls in new page: PASS.
- Main game repo, `world.js`, graph fixture, GitHub Pages settings, merge: NOT MODIFIED.
- Browser/Safari iPhone actual render: NOT EXECUTED.
- Pixel-perfect production PNG / seam matching: NOT EXECUTED.
- True H2/H1 ramp elevation, occlusion, collision and path clearance: NOT EXECUTED.

## Visual acceptance
Owner should open `https://kasipong13-boop.github.io/eldoria-wf41-preview/r02-p19.html` on iPhone Safari, compare P18, toggle guide and zoom, then provide screenshot. Assess whether the path appears to connect naturally and whether cliff side silhouettes and slope are convincing. This is a concept study only; do not promote into game without real asset geometry and gameplay QA.
