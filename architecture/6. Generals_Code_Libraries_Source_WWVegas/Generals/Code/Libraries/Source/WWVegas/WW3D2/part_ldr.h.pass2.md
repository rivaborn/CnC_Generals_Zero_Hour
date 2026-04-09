# Generals/Code/Libraries/Source/WWVegas/WW3D2/part_ldr.h - Enhanced Analysis

## Architectural Role
This file defines the core asset management infrastructure for particle emitters in the W3D rendering pipeline, bridging between serialized W3D assets and runtime rendering objects. It implements the Prototype pattern for emitter instantiation and handles version compatibility for particle effects.

## Cross-References
### Incoming
- Asset management system calls `ParticleEmitterLoaderClass::Load_W3D` during W3D file loading
- Rendering system uses `ParticleEmitterPrototypeClass::Create` to instantiate emitters
- Animation system references keyframe accessors (`Get_Color_Keyframe`, etc.)

### Outgoing
- Calls into `ChunkLoadClass`/`ChunkSaveClass` for binary serialization
- Uses `Vector3Randomizer` for particle distribution calculations
- Depends on `W3DMPO` and `PrototypeClass` for prototype management

## Design Patterns
- **Prototype Pattern**: `ParticleEmitterPrototypeClass` enables cloning of emitters without copying internal state
- **Composite Pattern**: Keyframe properties are stored in `ParticlePropertyStruct` containers
- **Strategy Pattern**: Different render modes and frame modes are selected via setters/getters

Rules followed. Output under 400 tokens.
