# GeneralsMD/Code/Libraries/Source/WWVegas/WW3D2/pointgr.h - Enhanced Analysis

## Architectural Role
This file defines the core rendering infrastructure for particle systems and point-based effects in the SAGE engine. It bridges the high-level game logic (particle emitters) with the low-level rendering pipeline (GERD), handling both CPU-side data management and GPU-side rendering commands.

## Cross-References
### Incoming
- Particle system managers (e.g., `ParticleSystemClass`) call `Set_Arrays` and `Render`
- Game object rendering loops invoke `Render` during the draw phase
- Camera systems may call `Set_Billboard` to control point orientation

### Outgoing
- Calls into `ShareBufferClass` for memory management of point attributes
- Uses `ShaderClass` and `TextureClass` for material setup
- Interfaces with `RenderInfoClass` for view/projection matrix data
- Relies on `Vector3/4` math types for transformations

## Design Patterns
- **Flyweight Pattern**: Precomputed vertex/UV tables (`_TriVertexLocationOrientationTable`, etc.) shared across all instances to reduce memory usage
- **Strategy Pattern**: Different `PointModeEnum` values (TRIS/QUADS/SCREENSPACE) represent interchangeable rendering strategies
- **Object Pooling**: Static intermediate arrays (`compressed_loc`, etc.) reused across frames rather than allocated per-render

*Not inferable*: Exact relationship with GERD (Graphics Engine Rendering Device) or how `SegmentGroupClass` differs functionally from `PointGroupClass`.
