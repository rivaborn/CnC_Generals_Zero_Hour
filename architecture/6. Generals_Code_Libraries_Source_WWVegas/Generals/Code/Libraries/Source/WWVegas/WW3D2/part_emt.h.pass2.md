# Generals/Code/Libraries/Source/WWVegas/WW3D2/part_emt.h - Enhanced Analysis

## Architectural Role
This file defines the core particle emitter system in the SAGE engine's rendering pipeline. It manages particle generation, lifecycle, and visual properties, working closely with the particle buffer system to create visual effects.

## Cross-References
### Incoming
- `part_buf.h` (ParticleBufferClass) - Uses emitter to manage particle storage
- `SceneClass` - Notifies emitter of scene changes
- `ChunkSaveClass` - Serialization interface
- `ParticleEmitterDefClass` - Definition-based creation

### Outgoing
- `rendobj.h` (RenderObjClass) - Base class inheritance
- `part_buf.h` (ParticleBufferClass) - Particle storage management
- `random.h` - Randomization for particle properties
- `quat.h` - Quaternion math for particle transforms

## Design Patterns
- **Factory Method**: `Create_From_Definition` creates emitters from definitions
- **Observer**: `Notify_Added/Removed` for scene state changes
- **Template Method**: `Update_On_Visibilty` for visibility-dependent behavior

*Not inferable*: Exact serialization mechanism, thread safety guarantees.
