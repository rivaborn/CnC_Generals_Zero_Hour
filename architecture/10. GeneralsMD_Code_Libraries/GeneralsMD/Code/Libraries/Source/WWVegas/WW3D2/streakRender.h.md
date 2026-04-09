# GeneralsMD/Code/Libraries/Source/WWVegas/WW3D2/streakRender.h

## Purpose
Defines the `StreakRendererClass` for low-level line rendering in the SAGE engine, used by particle and line systems.

## Responsibilities
- Manages line rendering properties (texture, shader, width, color, opacity)
- Handles texture mapping modes and subdivision levels
- Controls rendering flags (merging, sorting, end caps)
- Provides vertex buffer management for rendering

## Key Types
- **StreakRendererClass (Class)**: Core class for line rendering with configurable properties.
- **TextureMapMode (Enum)**: Defines texture mapping modes (uniform width/length, tiled).
- **BitShiftOffsets (Enum)**: Bit shift constants for flag manipulation.
- **VertexFormatXYZUV1 (Class)**: Vertex format for rendering (forward-declared).

## Key Functions
### `Init`
- Purpose: Initializes renderer with emitter line properties.
- Calls: None visible.

### `Render`
- Purpose: Renders a line segment with given points and transform.
- Calls: `subdivision_util`, vertex buffer management.

### `RenderStreak`
- Purpose: Renders a streak with per-point colors/widths.
- Calls: `Render`, vertex buffer management.

### `subdivision_util`
- Purpose: Handles subdivision of line points for rendering.
- Calls: None visible.

## Globals
- **MAX_STREAK_SUBDIV_LEVELS (const)**: Maximum subdivision level (7).

## Dependencies
- `shader.h`, `texture.h`, `matrix3d.h`, `vector2.h`
- `RenderInfoClass`, `SphereClass`, `W3dEmitterLinePropertiesStruct` (forward-declared).
