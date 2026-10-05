# Idols of Dust — Ritual Pixel v1 card frames

Blank tradition frames for live type. Generate new plates against
`RITUAL_PIXEL_FRAME_RULES.md`. Painted masters live in
`artwork/card-ui-ritual-pixel/painted/`. Rebuild with
`node scripts/build-ritual-pixel-frames.mjs` (contain-fit the plates, punch
the empty art-hole fill, and fill leftover exterior). Wells are empty circles:
a small banner hangs from Command; Devotion sits on a small dais.

## Contents

- `128/`, `220/`, `440/`: six tradition identities at the dedicated ready sizes.
  The 128 export keeps readable cost holders; do not downscale the 440.
- `layout.json`: master geometry, ready sizes, and CSS percentage tokens.
  It still names all seven identities and the Rite frame; that geometry is
  the contract the masters are generated against, not a list of shipped files.
- Masters and optional separate holders live in `artwork/card-ui-ritual-pixel/`.

Identities: Hellenic, Kemetic, Mesopotamian, Norse, Roman, and Hindu.

The Neutral plate and every `rite-<identity>.png` moved to
`quarantine/public/assets/ui/card-frames/` on 2026-09-22: every Unit and Rite
takes Unit frame v5, so no runtime or catalogue path can request them. The
painted masters stay in `artwork/card-ui-ritual-pixel/`, and
`node scripts/build-ritual-pixel-frames.mjs` still writes the quarantined
plates back into this directory — move them out again if you run it.

## Import

1. Place the illustration in the artwork rectangle in `layout.json`.
2. Overlay the matching complete frame at the same origin.
3. Draw the name, cost numerals, stats, rules, and metadata as live content.

Frames already include the empty nameplate, faction border, top cost wells,
and mid-band combat wells. Do not stack the optional nameplate or holders on
top of them. No numerals, card text, illustrations, or stat icons are baked
into the frames.

All layout coordinates use the 1056 × 1488 master canvas; multiply by
`cardWidth / 1056`. The artwork window is transparent; the outer edge is not.

Sand-marble masters remain in `artwork/card-ui-sand-marble/` for comparison.
