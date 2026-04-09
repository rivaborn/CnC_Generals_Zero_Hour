# GeneralsMD/Code/Libraries/Source/WWVegas/WW3D2/streak.h

## Purpose
Defines the `StreakLineClass` for rendering thick segmented lines with advanced features like varying thickness, opacity, and texture tiling.

## Responsibilities
- Manages line segment points and their properties (location, width, color).
- Handles texture mapping, shading, and rendering options.
- Implements LOD (Level of Detail) for performance optimization.
- Supports collision detection via ray casting.
- Provides cloning and identification for render objects.

## Key Types
- **TextureClass (Class)**: Not defined here; used for texture references.
- **StreakLineClass (Class)**: Render object for thick segmented lines with advanced features.

## Key Functions
### `Reset_Line`
- Purpose: Resets the line to its initial state.
- Calls: Not inferable.

### `Get_Num_Points`
- Purpose: Returns the number of points in the line.
- Calls: Not inferable.

### `Set_Point_Location`
- Purpose: Sets the object-space location for a given point.
- Calls: Not inferable.

### `Add_Point`
- Purpose: Adds a new point to the line.
- Calls: Not inferable.

### `Delete_Point`
- Purpose: Removes a point from the line.
- Calls: Not inferable.

### `Render`
- Purpose: Renders the line using the provided `RenderInfoClass`.
- Calls: `Render_Seg_Line`, `Render_Streak_Line`.

### `Cast_Ray`
- Purpose: Performs ray collision testing against the line.
- Calls: Not inferable.

### `Set_LocsWidthsColors`
- Purpose: Sets multiple point properties (location, width, color) at once.
- Calls: `Set_Locs`, `Set_Widths`, `Set_Colors`.

## Globals
- None.

## Dependencies
- Key includes: `rendobj.h`, `shader.h`, `simplevec.h`, `seglinerenderer.h`, `streakrender.h`.
- External symbols: `RenderObjClass`, `Vector3`, `Vector4`, `SphereClass`, `AABoxClass`, `CameraClass`, `RayCollisionTestClass`, `SegLineRendererClass`, `StreakRendererClass`.
