# Autumn and winter map WebP release

This package contains browser-ready WebP map tiles for the autumn and winter versions of the same territory.

- Each season contains 43 tiles: L0 1/1, L1 6/6, L2 36/36.
- WebP encoding is lossy quality 92, method 6, with metadata stripped.
- Pixel dimensions are unchanged from the accepted PNG masters.
- The browser should decode WebP directly into an image/bitmap. Do not convert WebP to PNG at runtime.
- PNG source masters are intentionally excluded from this release and remain the authoritative archive.
- Buildings and artificial objects are absent from all map tiles.

Read `AGENTS.md`, both season manifests, and the handoff documents before implementing the frontend.
