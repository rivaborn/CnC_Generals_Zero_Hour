# GeneralsMD/Code/Libraries/Source/WWVegas/WW3D2/part_buf.h - Enhanced Analysis

## Architectural Role
This file defines the core particle system rendering component in the SAGE engine's W3D2 subsystem. It bridges the particle emission logic (ParticleEmitterClass) with the rendering pipeline, handling both visual representation and performance optimization through LOD management.

## Cross-References
### Incoming
- Particle emitter systems call `Render()` to synchronize particle generation
- Scene management calls `Notify_Added/Removed()` for scene integration
- LOD system queries `Get_Cost/Value()` for rendering decisions

### Outgoing
- Calls into `PointGroupClass` and `SegLineRendererClass` for actual rendering
- Uses `ShareBufferClass` for memory management of particle data
- Interfaces with `ParticleEmitterClass` for new particle acquisition

## Design Patterns
- **Observer Pattern**: ParticleBuffer notifies scene on addition/removal
- **Flyweight Pattern**: Uses shared buffers (ShareBufferClass) for particle data
- **Strategy Pattern**: Different rendering modes (points/lines/line groups) via conditional rendering paths

*Not inferable*: Exact implementation of LOD calculation or collision handling details.
