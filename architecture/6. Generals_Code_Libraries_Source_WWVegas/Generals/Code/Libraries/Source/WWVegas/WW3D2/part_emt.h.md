# Generals/Code/Libraries/Source/WWVegas/WW3D2/part_emt.h

## Purpose
Defines the `ParticleEmitterClass` and related structures for particle effects in the SAGE engine.

## Responsibilities
- Manages particle emission behavior and properties
- Handles particle buffer creation and updates
- Provides serialization and cloning capabilities
- Controls particle visual properties (color, size, opacity)
- Manages emitter lifecycle and visibility

## Key Types
- `ParticlePropertyStruct<T>` (Struct): Stores keyframe-based particle properties (color, size, opacity, etc.)
- `ParticleEmitterClass` (Class): Main particle emitter class that manages particle generation and rendering
- `ParticleEmitterDefClass` (Class): Not shown in detail, likely a definition/serialization class
- `ChunkSaveClass` (Class): Not shown in detail, likely handles chunk-based serialization
- `NewParticleStruct` (Struct): Not shown in detail, likely holds new particle data

## Key Functions
### `Copy_Emitter_Property_Struct`
- Purpose: Copies particle property keyframe data from source to destination
- Calls: `W3DNEWARRAY`, `memcpy`

### `ParticleEmitterClass` constructor
- Purpose: Initializes a particle emitter with various emission and visual properties
- Calls: Not visible in header

### `Create_From_Definition`
- Purpose: Creates a particle emitter from a definition structure
- Calls: Not visible in header

### `Build_Definition`
- Purpose: Builds a definition structure from the emitter's current state
- Calls: Not visible in header

### `Save`
- Purpose: Serializes the emitter to a chunk save object
- Calls: Not visible in header

### `Emit`
- Purpose: Generates new particles and adds them to the particle buffer
- Calls: Not visible in header

### `Create_New_Particles`
- Purpose: Creates new particles with interpolated transforms
- Calls: `Initialize_Particle`

### `Initialize_Particle`
- Purpose: Initializes a single new particle with given parameters
- Calls: Not visible in header

## Globals
- `DefaultRemoveOnComplete` (bool): Controls whether emitters are removed when complete
- `DebugDisable` (bool): Global flag to disable all particle emitters (debug builds only)

## Dependencies
- `rendobj.h` - Base render object class
- `random.h` - Random number generation
- `part_buf.h` - Particle buffer class
- `quat.h` - Quaternion math
- `w3d_file.h` - W3D file handling
- `w3derr.h` - W3D error handling
- `v3_rnd.h` - Vector3 randomizer
- `SceneClass` - Scene management
