# Winter territory map — final WebP handoff

- Accepted PNG source set: L0 1/1, L1 6/6, L2 36/36.
- Runtime WebP set: L0 1/1, L1 6/6, L2 36/36; all files decode successfully at their original dimensions.
- Encoding: lossy WebP quality 92, method 6, metadata stripped.
- L0 dimensions: 1536×1024. L1 dimensions: 1536×1536. L2 dimensions: 2560×1707.
- Final L2 source batch was `r5-right`, covering `r5-c3.png` through `r5-c5.png`.
- One natural partially frozen river remains confined to the far-right region. It crosses the row 4–5 boundary continuously in c5 and exits the lower/right boundary.
- Final seam repairs include `c2-c3`, `c3-c4`, `c4-c5`, the corresponding `r4-r5` vertical seams, and their four-tile junctions.
- Buildings and every artificial object are prohibited and absent.
- PNG files remain the authoritative source archive. The files in `maps/winter` are the browser delivery set.
- The old partial q82 WebP files are superseded by this consistent q92 release and must not be mixed with it.
