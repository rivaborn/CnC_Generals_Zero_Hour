# Generals/Code/Libraries/Source/WWVegas/WW3D2/part_buf.h - Enhanced Analysis

## Architectural Role
This file defines the core particle system rendering component in the SAGE engine's W3D2 subsystem. It implements the particle buffer as a RenderObjClass derivative, handling particle state management, rendering, and LOD for visual effects.

## Cross-References
### Incoming
- Particle emitter systems call `Add_Uninitialized_New_Particle` to enqueue new particles
- Rendering pipeline calls `Render_Particles` and `Render_Line` during scene rendering
- Game loop calls `Update_Kinematic_Particle_State` and `Update_Visual_Particle_State` for particle updates

### Outgoing
- Calls into `PointGroupClass` for point-based rendering
- Calls into `SegLineRendererClass` for line-based rendering
- Depends on `ParticleEmitterClass` for particle generation synchronization

## Design Patterns
- **Circular Buffer**: Used for particle storage to efficiently handle overflow cases
- **Double Buffering (Ping-Pong)**: Implemented via `PingPongPosition` for collision detection and effects requiring previous frame state
- **LOD Management**: Implements predictive LOD with cost/value calculations for performance optimization

Rules followed. Analysis limited to 400 tokens.
