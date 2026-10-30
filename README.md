# Loft Studio

A browser-based tool that turns a 2D loft floor plan into an interactive 3D model for renovation and decoration planning.

## Features

- **3D loft model** built from the blueprint (3.2 m × 8.65 m, 4.05 m total height, mezzanine at 2.25 m): entry, shower, WC, kitchen with fridge and washing machine, living room with TV wall, storage under the stairs, table for two, reading corner, and a mezzanine bedroom.
- **Mirror switch** to flip the layout left ↔ right (bathroom on the right or left as you enter).
- **Colors & finishes** for walls, feature wall, TV wall, floors, ceiling, bathroom, cabinets, stairs and frames (paint, plaster, concrete, brick, slats, tile, marble, wood, chevron, terrazzo).
- **8 preset styles**: Scandinavian, Japandi, Industrial, Modern Luxe, Coastal, Dark Moody, Mediterranean, Warm Minimal.
- **Furniture library** (26 items) with common size presets and custom dimensions; drag, rotate, resize, recolor, duplicate, delete, move between floors.
- **Views**: whole loft / ground / mezzanine, 3D / top / window / entry cameras, cutaway walls, ceiling toggle, day/evening lighting, snapshots.
- **Plan tracer**: upload any floor-plan image, set the scale from one known dimension, trace walls, and build a 3D room.
- **Save**: autosaves in the browser; export/import designs as JSON text.

## Run locally

It is a single static page. Serve the folder with any static server, for example:

```sh
python3 -m http.server 8000
```

Then open http://localhost:8000. Three.js (0.165) is loaded from the jsDelivr CDN, so an internet connection is needed.

## Files

- `index.html` — the whole app (HTML, CSS, JavaScript).
- `blueprint.jpg` — the source floor plan, used in the Plan tab and as the tracer's default image.

## Deploy to Render

This repo includes a `render.yaml` Blueprint. In Render, choose **New → Blueprint**, connect this repository, and apply it. Render publishes the folder as a static site and redeploys on every push to `main`.
