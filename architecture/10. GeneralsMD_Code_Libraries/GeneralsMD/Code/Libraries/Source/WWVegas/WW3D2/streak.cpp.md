# GeneralsMD/Code/Libraries/Source/WWVegas/WW3D2/streak.cpp

## Purpose
Implements the `StreakLineClass` for rendering streaks and lines in the game, supporting features like subdivision, texturing, and collision detection.

## Responsibilities
- Manages line segment rendering with configurable properties (width, color, texture)
- Handles LOD (Level of Detail) optimization for performance
- Supports per-point colors and widths for "streak" effects
- Implements collision detection for ray casting
- Maintains object-space bounding volumes

## Key Types
- `StreakLineClass` (Class): Main class for rendering streaks/lines with configurable properties
- `SegLineRendererClass` (Class): Line renderer used internally (forward declared)
- `StreakRendererClass` (Class): Streak-specific renderer (forward declared)

## Key Functions
### `Render_Seg_Line`
- Purpose: Renders a simple segmented line
- Calls: `LineRenderer.Render`

### `Render_Streak_Line`
- Purpose: Renders a streak line with per-point colors and widths
- Calls: `StreakRenderer.RenderStreak`

### `Cast_Ray`
- Purpose: Performs ray collision detection against the line segments
- Calls: `Ray.Find_Intersection`

### `Prepare_LOD`
- Purpose: Prepares LOD processing for the line
- Calls: `PredictiveLODOptimizerClass::Add_Object`, `PredictiveLODOptimizerClass::Add_Cost`

## Globals
- `_LineRenderer` (SegLineRendererClass): Static line renderer instance

## Dependencies
- Key includes: `streak.h`, `ww3d.h`, `rinfo.h`, `predlod.h`, `v3_rnd.h`, `texture.h`, `coltest.h`, `w3d_file.h`, `dx8wrapper.h`, `vp.h`, `vector3i.h`, `sortingrenderer.h`
- External symbols: `WW3D`, `PredictiveLODOptimizerClass`, `RenderObjClass`, `SphereClass`, `AABoxClass`, `Vector3`, `Vector4`, `Vector2`, `LineSegClass`, `RayCollisionTestClass`
