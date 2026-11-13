# WF41-P17 — Design-only Visual Refinement QA

## Source and deliverable
- Based on the P16 Safari screenshot evidence showing a dark seam and visually overlapped R02 samples.
- New isolated page `seam-p17.html`, commit `3f3c646`.
- Previous `seam.html` remains unchanged; its blob SHA was `6e71e5809054e9dd5f78d832145de4a17cafda92`.

## Changes
1. **Ground:** draw a solid muted-green diamond under each existing Grass/Moss/Dirt PNG tile, reducing visibility of dark cracks at transparent edge pixels. Default diagnostic outlines OFF; user can turn them ON. This is a visual mask/underlay, **NOT edge-matched seamless texture generation**.
2. **R02:** re-space the three existing Upper/Slope/Lower concept sprites into a closer centered vertical illustrative stack. This is **NOT verified H2→H1 geometry**, footprint or slope collider.
3. Keep all six source PNG assets unchanged and embedded.

## Static QA
- New GitHub file exists and JavaScript syntax parses: PASS
- Six PNG data URLs retained: PASS
- Visual-only reference states 337 graph nodes / 416 edges: PASS
- No graph, walkability or UNKNOWN status changed: PASS (no graph editing or walking code in diagnostic)
- No Save Engine, storage, main game, merge or GitHub Pages settings changes: PASS
- Browser/Safari iPhone visual result: NOT EXECUTED
- Actual seamless pixel matching, elevation and R02 collision: NOT EXECUTED

## Next owner check
Open `https://kasipong13-boop.github.io/eldoria-wf41-preview/seam-p17.html`. Compare P16 and P17 with outline OFF and ON; inspect whether the dark gaps appear reduced. Switch to R02 and judge the three-part alignment. Send screenshots to evaluate remaining defects.
