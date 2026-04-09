# Generals/Code/Libraries/Source/WWVegas/WW3D2/streak.h

## Purpose
Defines the `StreakLineClass` render object for rendering thick segmented lines with varying properties like width, opacity, and texture tiling.

## Responsibilities
- Manages line segments with per-point properties (location, width, color).
- Handles texture mapping, shading, and rendering of streak lines.
- Supports LOD (Level of Detail) for performance optimization.
- Provides collision detection via ray casting.
- Configures line rendering behavior (e.g., end caps, sorting, merging).

## Key Types
- **TextureClass (Class)**: Texture reference for the streak line.
- **StreakLineClass (Class)**: Render object for thick segmented lines with dynamic properties.
- **SegLineRendererClass::TextureMapMode (Enum)**: Texture mapping mode (not defined here).

## Key Functions
### `Render_Seg_Line`
- Purpose: Renders the streak line using segment-based rendering.
- Calls: `StreakRendererClass` methods, `SegLineRendererClass` methods.

### `Render_Streak_Line`
- Purpose: Renders the streak line with per-point properties (width, color, opacity).
- Calls: `StreakRendererClass` methods.

### `Set_LocsWidthsColors`
- Purpose: Sets multiple point properties (location, width, color) in one call.
- Calls: `Set_Locs`, `Set_Widths`, `Set_Colors`.

## Globals
- **None**

## Dependencies
- `rendobj.h`, `shader.h`, `simplevec.h`, `seglinerenderer.h`, `streakrender.h`
- `RenderObjClass`, `Vector3`, `Vector4`, `SphereClass`, `AABoxClass`, `CameraClass`, `RayCollisionTestClass`
