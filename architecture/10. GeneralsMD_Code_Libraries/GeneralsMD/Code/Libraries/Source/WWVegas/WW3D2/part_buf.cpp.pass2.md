# GeneralsMD/Code/Libraries/Source/WWVegas/WW3D2/part_buf.cpp - Enhanced Analysis

## Architectural Role
This file implements the core particle system buffer management in the SAGE engine's rendering pipeline. It handles particle lifecycle, property interpolation, and LOD management, serving as the bridge between particle emitters and the actual rendering backends (PointGroup, LineGroup, LineRenderer).

## Cross-References
### Incoming
- `part_emt.cpp` (ParticleEmitterClass) - Creates and manages ParticleBufferClass instances
- `ww3d.cpp` (main rendering loop) - Calls Update() and Render() during frame processing
- `scene.cpp` (Scene management) - Uses particle buffers for scene effects
- `camera.cpp` (Camera system) - Provides view frustum data for LOD calculations

### Outgoing
- `texture.cpp` (TextureClass) - Texture management for particle rendering
- `shader.cpp` (ShaderClass) - Shader state for particle blending modes
- `dx8wrapper.cpp` (DirectX8 abstraction) - Low-level rendering commands
- `vector3.cpp` (Vector3 math) - Position/velocity calculations

## Design Patterns
- **Circular Buffer**: Manages particle lifecycle with Start/End indices for efficient memory reuse
- **Strategy Pattern**: Different render modes (points, lines, quads) implemented via separate renderer objects
- **Observer Pattern**: Particle buffers notify emitters when they become inactive (IsEmitterDead flag)

Rules followed. Output under 400 tokens.
