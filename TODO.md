# Development TODO

Based on the current `Primaries.FCMacro` script and the desired 8‑4‑2‑turbo‑1
"bundle of snakes" layout, these are the major tasks to tackle.

## Collision handling

- [x] Expose collided geometry so we can inspect where the tube hits the engine.
- [x] Improve the `intersects()` helper to return which object caused the clash
      and where it happened.
- [ ] Allow automatic path adjustments beyond the current angle/spread/drop
      strategy (e.g. incremental twist or additional control points).
- [ ] Avoid orange failures by trying shorter steps before giving up.
- [ ] Improve engine part detection so collisions work even if parts aren't
      labelled with "engine". Allow specifying a custom group or pattern.

## Path generation

- [x] Build a real cross‑over underneath the engine instead of the current
      straight drop through the centre. The path should snake under the block
      then route to the collector position.
- [x] Join paired primaries together into a Y‑pipe (currently only a straight
      placeholder cylinder is created).
- [ ] Parametrise collector position and orientation so that 4‑2 merge pieces can
      be generated automatically.

## General improvements

- [ ] Document the necessary coordinate systems (`Port*_CS` objects) expected in
      the FreeCAD model.
- [ ] Add a setup section in the README on how to load the macro and run it.
- [ ] Consider supporting multiple engine layouts (bank angle, firing order) via
      a configuration file.

