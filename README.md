# LS3 180° Header Builder Macro

This repository contains a FreeCAD macro that generates a collision-aware 180° header setup for an LS-series engine. The script builds individual primaries with automatic adjustments and then merges them into pairs.

## Loading the Macro

1. Open your FreeCAD model of the engine. Ensure coordinate systems named `Port*_CS` exist for each exhaust port.
2. Copy `Primaries.FCMacro` into your FreeCAD macros directory.
3. From FreeCAD, open the macro and press **Run**. The script removes any previous header objects and starts generating new pipes.
4. Ensure your engine solids have "engine" in their label or group them under
   an object named *Engine* so the script can test for collisions.

Collision intersections are stored in the *Header180_Collisions* group for inspection.


