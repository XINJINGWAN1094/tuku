# Territory Map Detail Asset Pack

## Coordinate system

- World size: `3072 × 2048`
- Origin: top-left `(0, 0)`
- Base files: `01-base-autumn.png`, `02-base-winter.png`
- Every local-detail image is `1024 × 1024` and represents a `512 × 512` world rectangle (2× pixel density).
- Exact rectangles and season tags are in `asset-manifest.json`.

## Runtime layer order

1. Current-season base image
2. Current-season repeating ground textures
3. Visible local-detail overlays
4. Decoration sprites from atlases
5. Buildings and interactive UI

## Local overlays

Draw each local-detail image into its manifest `worldRect`. The PNG already contains a soft alpha edge for blending. Fade local details in around zoom 3.5–4.5 rather than switching instantly.

## Atlases

- Atlas size: `1024 × 1024`
- Layout: `4 × 4`
- Cell size: `256 × 256`
- Transparent PNG background

## Seasonal loading

Load only assets whose `season` is the active season plus assets tagged `shared`. Release the previous season's textures after the transition completes.

## Ground textures

Ground textures are intended for subtle, low-opacity detail. Randomize UV offset and use quarter-turn rotation where appropriate to reduce visible repetition. They were visually checked in a 2×2 repeat layout.
