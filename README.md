# pixpat

Single-file HTML pixel-pattern designer. Tile a grid of cells (square, dot, star, custom polygon, etc.) and use spatial **attractors** — points, ellipses, pen paths, gradients — to scale, fade, or punch holes through the pattern. Export PNG or SVG.

No build step. Open the `index.html` file in any modern browser.

## Versions

- **[v1/](v1/index.html)** — initial release. Per-attractor radius, curve, strength, mode (scale / hole).
- **[v1.5/](v1.5/index.html)** — adds a per-attractor **Pull** control (magnetic displacement) plus a **draggable magnetic anchor** for each attractor: cells inside the attractor's radius get visually shifted toward (or away from) the anchor. The anchor defaults to the geometry centroid (point itself for Point, center for Ellipse, midpoint for Gradient, average of nodes for Pen) and is movable independently. A reset button restores it to the centroid. Closer cells get pulled harder, producing a clustering / magnet effect. Also: hover cursor changes to a pointer over attractors, and Delete / Backspace removes the selected attractor.

## Attractor controls (v1.5)

| Control  | Purpose |
|----------|---------|
| Strength | Effect amplitude (-1 to 1; sign flips push/pull on the chosen Mode) |
| Radius   | Outer extent — beyond this, no effect |
| Pull     | Magnetic displacement (-1 to 1). Positive = cells migrate toward the attractor; negative = cells get pushed away. 0 = no displacement. |
| Curve    | Falloff exponent (sharper vs. softer edge) |
| Mode     | `scale` (resize cells) or `hole` (fade out cells) |

## Usage

- **Click** the canvas to add an attractor of the current Tool.
- **Drag** to move; **alt+drag** to duplicate; **right-click** or **Delete / Backspace** to remove.
- **Shift+wheel** over an attractor to resize its radius.
- **Wheel** zooms; **space+drag** pans.
- **Ctrl+Z** / **Ctrl+Shift+Z** undo/redo.
- Hover an attractor (Point / Ellipse / Gradient tools) and the cursor turns into a pointer to indicate it is selectable.
- When an attractor is selected, its **magnetic anchor** (small ringed dot with crosshair) appears at the geometry centroid. Drag to reposition. Click the **↻ reset magnet to centroid** button in the right panel to restore it.
