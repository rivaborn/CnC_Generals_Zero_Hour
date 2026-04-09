# GeneralsMD/Code/Libraries/Source/WWVegas/WW3D2/streakRender.h - Enhanced Analysis

## Architectural Role
This file defines the core rendering logic for particle trails and line effects in the SAGE engine's W3D2 subsystem. It bridges the particle system and rendering pipeline, handling vertex buffer management and shader configuration for visual effects.

## Cross-References
### Incoming
- `SegmentedLineClass` (friend class) - Uses `StreakRendererClass` for line rendering
- Particle system classes (inferred) - Likely call `RenderStreak` for trail effects
- Emitter systems (inferred) - Call `Init` with `W3dEmitterLinePropertiesStruct`

### Outgoing
- `RenderInfoClass` - Used for rendering context
- `TextureClass` - For texture management
- `ShaderClass` - For shader configuration
- Vertex buffer management (internal) - Allocates and manages `VertexFormatXYZUV1` buffers

## Design Patterns
- **Property Object Pattern**: Encapsulates all rendering properties (width, color, texture) in a single class
- **Bitmask Flags**: Uses bitfields for rendering options (merging, sorting, end caps)
- **Vertex Buffer Object (VBO)**: Manages vertex data in `m_vertexBuffer` for efficient rendering

Rules followed. Output under 400 tokens.
