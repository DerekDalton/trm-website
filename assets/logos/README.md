# Client logos (marquee "Trusted by" strip)

These files feed the scrolling logo strip in `index.html`.

## How it works
- Logos sit directly on the dark strip (no background chip) with `filter: grayscale(100%)`.
- Each `<div class="client-logo">` in `index.html` points at a specific file here via its
  `<img src>`. If a file is missing, the company name shows as text instead.

## ⚠️ Known limitation of this treatment
Grayscale removes color but not lightness, and the strip background is near-black
(`#141414`). So **dark logos are hard to see**: black/navy wordmarks (Wintrust, NECA,
Lollapalooza, Kygo, Senses Fail, Two Friends, Maps & Atlases, Sonepar, Sura, Navy Pier,
United Center, Northwestern Medicine, etc.) render as dark gray and nearly disappear. The
opaque files (`decisionone.jpg`, `blockparty.jpg`, `mapsandatlases.png`, `twofriends.webp`)
show as gray boxes. For best results on a dark strip, logos should be **light/white on a
transparent background**, or switch the treatment to forced-white
(`filter: brightness(0) invert(1)`).

## File requirements
- Any web image format works: SVG (best), PNG, WebP, or JPEG.
- Transparent background strongly preferred (opaque files show a visible box).

## Adding / changing a logo
1. Drop the file in this folder (any name, any of the formats above).
2. Point its `<img src>` in **both** identical `.marquee-inner` blocks in `index.html`
   at the file (the second block is a duplicate that makes the scroll loop seamlessly).
