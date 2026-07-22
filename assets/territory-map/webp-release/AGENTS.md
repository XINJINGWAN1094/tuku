# Repository guidance

- Treat files under `maps/autumn` and `maps/winter` as immutable production assets. Do not resize, recompress, rename, recolor, or regenerate them.
- Load tile paths from each season's manifest; do not hard-code an incomplete tile list.
- Decode WebP directly in the browser using `HTMLImageElement`, `createImageBitmap`, Canvas, or the selected rendering engine. Do not convert assets to PNG at runtime.
- Load only the visible tiles plus a small neighboring preload ring. Release decoded bitmaps/textures after they leave the cache budget.
- Draw tiles at consistent integer-aligned world coordinates. Prevent texture wrapping and verify there are no one-pixel gaps at every supported zoom.
- Preserve the documented L0/L1/L2 grids and dimensions. Revalidate the provisional zoom thresholds during frontend testing.
- Buildings must remain separate transparent overlays and must never be baked into terrain tiles.
- After changes, test both seasons, level transitions, failed URL handling, caching, CORS behavior, and memory cleanup.
