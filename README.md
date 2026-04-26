# pixpat

Single-file HTML pixel-pattern designer. Tile a grid of cells (square, dot, star, custom polygon, etc.) and use spatial **attractors** — points, ellipses, pen paths, gradients — to scale, fade, or punch holes through the pattern. Export PNG or SVG.

No build step. Open the `index.html` file in any modern browser.

## Versions

- **[v1/](v1/index.html)** — initial release. Per-attractor radius, curve, strength, mode (scale / hole).
- **[v1.5/](v1.5/index.html)** — adds a per-attractor **Inner radius** control: a plateau zone close to the attractor where the effect stays at full strength before falloff begins. Set `Inner = 0` to behave exactly like v1; raise it to create a "ring" or "donut" influence.

## Attractor controls (v1.5)

| Control  | Purpose |
|----------|---------|
| Strength | Effect amplitude (-1 to 1; sign flips push/pull) |
| Radius   | Outer extent — beyond this, no effect |
| Inner    | Inner plateau — within this distance, effect stays at full strength |
| Curve    | Falloff exponent (sharper vs. softer edge) |
| Mode     | `scale` (resize cells) or `hole` (fade out cells) |

## Usage

- **Click** the canvas to add an attractor of the current Tool.
- **Drag** to move; **alt+drag** to duplicate; **right-click** to delete.
- **Shift+wheel** over an attractor to resize its radius.
- **Wheel** zooms; **space+drag** pans.
- **Ctrl+Z** / **Ctrl+Shift+Z** undo/redo.
