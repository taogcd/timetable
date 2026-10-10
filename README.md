# Timetable — Space Walk / 04.1

Walk on a continuous level surface, or descend through its central opening into the underground timetable. The exterior remains level over the buried tunnel. The roof starts below ground and follows the descent; it no longer protrudes above the surface.

Live view: https://taogcd.github.io/timetable/space.html

Click the view. **WASD** moves, **Q/E** turns, **hold Shift** moves three times faster. Drag to look around, **R** resets and **Esc** releases the controls. Standard movement is also faster than in 04.

Left and right walls retain the original League Gothic and Superclarendon outlines in progressively recombined compositions. Their arrangement stays fixed in space, and the upper field fades with height.

The ceiling uses real triangulated Clarendon Text Pro outlines and the original time data shared with the Blender room (display columns 10–18). It does not use a screenshot or an image texture. Empty source cells stay empty. Continuous world rows and a procedural grid avoid stretched image seams.

Both surface and underground geometry use a fixed pool of 25 sections around the walker. The surface extends in both longitudinal directions without a maximum walking boundary. The underground route continues downwards and leads back to its entrance when reversed. Walking level is tracked independently so crossing the surface above the tunnel cannot drop the viewer into it.

Ten logic/geometry checks cover buried ceilings, level ground, route transitions, collision during sprinting, an hour of forward/backward movement, Shift release, source data, and bounded recycling. Local browser loading and navigation checked before publishing; the author reviews the visual result.

This revision changes the website only. Existing Blender files remain historical finite samples.

## Development

`npm ci`, `npm test`, `npm run build`. `release/space.html` is self-contained apart from the existing Adobe Fonts stylesheet used by the interface. The original main page is unchanged.

`assets/ceiling-provenance.json` records the source hashes. `scripts/export-ceiling-data.py` reads the original Blender source export; check its source path before rebuilding. The old `assets/tunnel/ceiling.png` is retained only as an unused historical asset.
