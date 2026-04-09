# Generals/Code/Libraries/Source/WWVegas/WW3D2/seglinerenderer.h

## Purpose
Defines the `SegLineRendererClass` for low-level line rendering in the W3D engine, used by segmented lines and particle buffers.

## Responsibilities
- Manages line rendering properties (texture, shader, width, color, opacity)
- Handles subdivision, texture mapping, and UV animation
- Controls rendering flags (merging, sorting, end caps)
- Provides utility functions for line subdivision

## Key Types
- **SegLineRendererClass (Class)**: Core line renderer with rendering properties and methods.
- **TextureMapMode (Enum)**: Texture mapping modes (uniform width/length, tiled).
- **BitShiftOffsets (Enum)**: Bit shift offsets for flags.
- **Anonymous enum (Enum)**: Rendering flags (merge intersections, freeze random, disable sorting, end caps).

## Key Functions
### `Init`
- Purpose: Initializes the renderer with emitter line properties.
- Calls: None visible.

### `Render`
- Purpose: Renders a line segment with given points and transform.
- Calls: `subdivision_util`, `RenderInfoClass` methods.

### `subdivision_util`
- Purpose: Handles line subdivision for rendering.
- Calls: None visible.

### `Set_Texture_Mapping_Mode`
- Purpose: Sets the texture mapping mode via bit flags.
- Calls: None.

### `Set_UV_Offset_Rate`
- Purpose: Sets the UV offset rate for texture animation.
- Calls: None.

## Globals
- **MAX_SEGLINE_SUBDIV_LEVELS (const)**: Maximum subdivision level (7).

## Dependencies
- `shader.h`, `texture.h`, `matrix3d.h`, `vector2.h`
- `RenderInfoClass`, `SphereClass`, `W3dEmitterLinePropertiesStruct` (forward declarations).
