# GeneralsMD/Code/Libraries/Source/WWVegas/WW3D2/streakRender.cpp

## Purpose
Implements the `StreakRendererClass` for rendering streaks/lines with configurable properties like texture mapping, subdivision, and noise.

## Responsibilities
- Manages streak rendering with subdivision and texture mapping
- Handles vertex generation and triangle strip creation
- Supports merging of intersections and sorting
- Configures shaders and materials for rendering

## Key Types
- `StreakRendererClass` (Class): Main streak rendering class with configuration and rendering methods
- `StreakSubdivision` (Struct): Helper struct for subdivision stack processing
- `LineSegmentIntersection` (Struct): Represents intersection points for merging logic

## Key Functions
### `RenderStreak`
- Purpose: Renders a streak with per-point colors and widths
- Calls: `subdivision_util`, `getVertexBuffer`, `DX8Wrapper` methods, `SortingRendererClass::Insert_Triangles`

### `subdivision_util`
- Purpose: Subdivides line segments with noise and texture coordinate generation
- Calls: `Random3Class`, `Vector3SolidBoxRandomizer`

### `getVertexBuffer`
- Purpose: Allocates and returns vertex buffer of requested size
- Calls: `W3DNEWARRAY`

## Globals
- `STREAK_CHUNK_SIZE` (const): Chunk size for processing points
- `MAX_STREAK_POINT_BUFFER_SIZE` (const): Maximum points per chunk
- `MAX_STREAK_POLY_BUFFER_SIZE` (const): Maximum polygons per chunk

## Dependencies
- `streakrender.h`, `ww3d.h`, `rinfo.h`, `dx8wrapper.h`, `sortingrenderer.h`, `vp.h`, `vector3i.h`, `random.h`, `v3_rnd.h`
- `TextureClass`, `ShaderClass`, `VertexMaterialClass`, `DynamicVBAccessClass`, `DynamicIBAccessClass`
