# Generals/Code/Libraries/Source/WWVegas/WW3D2/streak.cpp

## Purpose
Implements the `StreakLineClass` for rendering streaks and lines in the game, supporting features like subdivision, texturing, and collision detection.

## Responsibilities
- Manages line segment rendering with configurable properties (width, color, texture)
- Handles LOD (Level of Detail) optimization for performance
- Supports per-point colors and widths for "streak" effects
- Provides collision detection via ray casting
- Integrates with the game's rendering pipeline and sorting system

## Key Types
- `StreakLineClass` (Class): Main class for streak/line rendering with properties and rendering logic
- `SegLineRendererClass` (Class): Line renderer used internally (forward-declared)
- `StreakRendererClass` (Class): Streak-specific renderer (forward-declared)
- `Vector3`, `Vector4`, `Vector2` (Structs): Math utility types
- `RenderInfoClass` (Class): Rendering context information
- `SphereClass`, `AABoxClass` (Structs): Bounding volume types

## Key Functions
### `Render`
- Purpose: Main rendering entry point that dispatches to appropriate render method
- Calls: `Render_Seg_Line`, `Render_Streak_Line`, `WW3D::Add_To_Static_Sort_List`

### `Render_Seg_Line`
- Purpose: Renders a simple segmented line
- Calls: `LineRenderer.Render`

### `Render_Streak_Line`
- Purpose: Renders a streak line with per-point colors and widths
- Calls: `StreakRenderer.RenderStreak`

### `Cast_Ray`
- Purpose: Performs ray collision detection against the line
- Calls: `Ray.Find_Intersection`

### `Prepare_LOD`
- Purpose: Prepares the object for LOD processing
- Calls: `PredictiveLODOptimizerClass::Add_Object`, `PredictiveLODOptimizerClass::Add_Cost`

## Globals
- `_LineRenderer` (SegLineRendererClass): Static line renderer instance

## Dependencies
- Key includes: `streak.h`, `ww3d.h`, `rinfo.h`, `predlod.h`, `v3_rnd.h`, `texture.h`, `coltest.h`, `w3d_file.h`, `dx8wrapper.h`, `vp.h`, `vector3i.h`, `sortingrenderer.h`
- External symbols: `WW3D`, `PredictiveLODOptimizerClass`, `RenderObjClass`, `SphereClass`, `AABoxClass`, `LineSegClass`, `RayCollisionTestClass`
