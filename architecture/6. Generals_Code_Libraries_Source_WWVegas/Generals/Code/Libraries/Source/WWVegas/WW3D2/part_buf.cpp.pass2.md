# Generals/Code/Libraries/Source/WWVegas/WW3D2/part_buf.cpp - Enhanced Analysis

## Architectural Role
This file implements the core particle system buffer management in the SAGE engine's rendering pipeline. It handles particle property interpolation, LOD management, and emitter interactions, serving as the bridge between particle emitters and the rendering backend.

## Cross-References
### Incoming
- `part_emt.cpp` (ParticleEmitterClass) - calls Update() and rendering methods
- `scene.cpp` (SceneClass) - queries particle buffers during scene traversal
- `predlod.cpp` (PredLODManager) - uses LOD screen size clamping
- `ww3d.cpp` (WW3D core) - accesses particle buffers during frame rendering

### Outgoing
- `ww3d.h` - uses WW3D::Get_Sync_Time() for timing
- `texture.h` - references TextureClass for particle textures
- `dx8wrapper.h` - indirect DX8 rendering dependencies
- `vector3.h` - mathematical operations on particle positions

## Design Patterns
- **Object Pool Pattern**: Manages fixed-size particle buffers with circular queues
- **Flyweight Pattern**: Shares particle property data across multiple particles
- **Strategy Pattern**: Different rendering modes (points/lines) via LineRenderer/PointGroup delegation

Rules followed. Output under 400 tokens.
