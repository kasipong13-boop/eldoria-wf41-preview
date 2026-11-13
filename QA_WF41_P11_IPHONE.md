# WF41-P11 — Safari iPhone Acceptance Report

## Scope
LEGEND OF ELDORIA — WF41 experimental 128×128 **logical graph** preview, independent repository `kasipong13-boop/eldoria-wf41-preview`. The test was performed by the project owner on a physical iPhone using Safari and results were reported in chat. This is owner-reported acceptance evidence, **not** an independently instrumented browser run.

## Owner-reported results

| Test | Result |
| --- | --- |
| Walk left and back right | PASS |
| Walk north from spawn | PASS |
| Attempt to walk outside graph path shows BLOCKED | PASS |
| Zoom in / out (+ / -) | PASS |
| Drag camera and recenter | PASS |
| Tap directly connected node to move | PASS |

**Acceptance: 6/6 PASS, 0 FAIL (owner-reported).**

## Repository evidence
- Experimental standalone `index.html` exists on `main` in this **separate preview repository**.
- Graph snapshot embedded in standalone: 337 nodes / 416 edges, not the unverified 347-node proposal.
- Main game repository `kasipong13-boop/legend-of-eldoria` is **not changed** by this report.
- No Save Engine, Save Schema, world.js, GitHub Pages settings of the main game, or Merge touched.

## Important limits / remaining gates
- The preview is a graph-only diagnostic map, **not** a complete isometric forest or physical terrain occupancy/collision test.
- H2/H1 multi-surface collision, R02/R04 ramps, same-XY surface disambiguation, height rendering, foot collider, occlusion: **NOT EXECUTED / NOT VERIFIED**.
- Full 128×128 terrain occupancy remains UNKNOWN except for graph simulation. Unknown areas remain blocked.
- Automated end-to-end browser smoke tests: **NOT EXECUTED**.
- No changes to runtime gameplay or Save Engine are authorized by this report.

## Recommendation
Freeze this 6/6 baseline as WF41-P11 accepted, and next create a separate P12 art/terrain prototype that overlays isometric visual tiles **without promoting unknown terrain to walkable**. Test R02/R04 with explicit height and collision evidence before integration.
