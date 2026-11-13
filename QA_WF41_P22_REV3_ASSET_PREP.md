# WF41-P22 — Rev.3 Organic Terrain Asset Preparation

**Status:** Design-only / extraction preparation, **not** finished PNG assets.

## Evidence
- Owner approved **Rev.3 Organic Terrain** as the R02 art reference.
- Read-only check of existing `r02-p21.html` and `art.html` completed before preparing this specification.
- Existing playable reference graph: **337 nodes / 416 edges**. No geometry/collision validation is implied.

## Planned 3-piece decomposition
1. **Upper Landing:** irregular mossy grassy plateau, weathered rock rim and eroded soil entering the slope.
2. **Slope:** naturally worn and uneven earth surface, embedded stones, irregular grass shoulders, roots and layered cliff rock.
3. **Lower Landing:** dirt disperses gradually into grass, with stones, moss and vegetation around—not across—the visual walking corridor.

Proposed output paths are listed in `r02-rev3-asset-manifest.json`. They are **planned names only**, not existing PNGs.

## Required checks before export
- Verify the original Rev.3 image bytes are available for lawful extraction or regenerate/export a clean source; never silently substitute the P21 procedural canvas.
- Determine true pixel dimensions, alpha coverage, overlap padding and isometric seam anchors from the source image.
- Export three transparent RGBA PNGs, verify exact pixel alignment at upper/slope and slope/lower joins, and inspect at native scale.
- Test in isolated Safari preview; do not unlock any UNKNOWN space.

## Prohibitions
No edits to main game repository, `world.js`, Save Engine, graph fixture, collision, height logic or Pages settings; no Merge.

## P22 QA
| Check | Result |
|---|---|
| Approved Rev.3 reference documented | PASS |
| Existing P21 file inspected | PASS |
| Graph reference 337 nodes / 416 edges | PASS |
| Three-piece asset plan and export acceptance | PASS |
| Three actual transparent PNGs exported | NOT EXECUTED |
| Pixel-perfect seam/alpha validation | NOT EXECUTED |
| Safari iPhone actual asset test | NOT EXECUTED |
| Real H2/H1 and collision clearance | NOT EXECUTED |

**Next gate:** actual source artwork + 3 RGBA PNGs, then seam QA before integration.
