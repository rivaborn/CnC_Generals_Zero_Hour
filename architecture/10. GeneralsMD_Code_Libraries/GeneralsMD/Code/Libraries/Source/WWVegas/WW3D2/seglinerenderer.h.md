# GeneralsMD/Code/Libraries/Source/WWVegas/WW3D2/seglinerenderer.h

## Purpose
Header for `SegLineRendererClass`, which implements low-level line rendering functionality used by segmented lines and particle buffers in the W3D engine.

## Responsibilities
- Manages line rendering properties (texture, shader, width, color, opacity)
- Handles subdivision, texture mapping, and UV animation
- Controls rendering flags (intersection merging, sorting, end caps)
- Provides utility functions for line rendering

## Key Types
- **SegLineRendererClass (Class)**: Core line renderer with properties and rendering logic.
- **TextureMapMode (Enum)**: Defines texture mapping modes (uniform width/length, tiled).
- **BitShiftOffsets (Enum)**: Bit shift offsets for flags.
- **VertexFormatXYZDUV1 (Class)**: Vertex format for rendering (forward-declared).

## Key Functions
### `Render`
- Purpose: Renders a line segment with given points and properties.
- Calls: `subdivision_util`, `getVertexBuffer`.

### `subdivision_util`
- Purpose: Handles subdivision of line segments for rendering.
- Calls: None (utility function).

### `Set_Texture_Mapping_Mode`
- Purpose: Sets the texture mapping mode for the line.
- Calls: None (inline).

### `Set_UV_Offset_Rate`
- Purpose: Sets the rate at which UV offsets animate.
- Calls: None (inline).

## Globals
- **MAX_SEGLINE_SUBDIV_LEVELS (const)**: Maximum subdivision level (7).

## Dependencies
- `shader.h`, `texture.h`, `matrix3d.h`, `vector2.h`
- `RenderInfoClass`, `SphereClass`, `W3dEmitterLinePropertiesStruct` (forward-declared).
