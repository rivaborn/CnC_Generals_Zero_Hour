# Generals/Code/Libraries/Source/WWVegas/WW3D2/part_ldr.cpp - Enhanced Analysis

## Architectural Role
This file is the core of the particle emitter asset pipeline in the SAGE engine, bridging between W3D file I/O and runtime particle systems. It handles serialization/deserialization of emitter definitions while maintaining compatibility with the engine's chunk-based asset system.

## Cross-References
### Incoming
- **part_emt.cpp**: Uses `ParticleEmitterDefClass` for emitter instantiation
- **assetmgr.cpp**: Likely calls `ParticleEmitterLoaderClass::Load_W3D` during asset loading
- **W3D file importers**: Directly invoke loader methods during level/asset loading

### Outgoing
- **part_emt.cpp**: Calls `ParticleEmitterClass::Create_From_Definition` for prototype creation
- **chunkio.h**: Uses `ChunkLoadClass`/`ChunkSaveClass` for binary I/O
- **texture.h**: References texture management for particle materials

## Design Patterns
- **Singleton**: `_ParticleEmitterLoader` ensures single loader instance
- **Prototype**: `ParticleEmitterPrototypeClass` enables efficient emitter instantiation
- **Composite**: `ParticlePropertyStruct` aggregates keyframe data hierarchically

*Not inferable*: Exact factory usage with other emitter types (e.g., line emitters).
