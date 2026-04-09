# GeneralsMD/Code/Libraries/Source/WWVegas/WW3D2/part_emt.h

## Purpose
Defines the `ParticleEmitterClass` and related structures for particle effects in the W3D engine.

## Responsibilities
- Manages particle emission properties (position, velocity, color, size, etc.)
- Handles particle buffer creation and updates
- Provides serialization and cloning for particle emitters
- Supports keyframe-based property interpolation

## Key Types
- `ParticlePropertyStruct<T>` (template struct): Stores keyframe data for particle properties (color, opacity, size, etc.)
- `ParticleEmitterClass` (class): Main particle emitter class that emits particles into a buffer
- `ParticleEmitterDefClass` (class): Definition class for serialization (forward declared)
- `ChunkSaveClass` (class): Chunk save interface (forward declared)
- `NewParticleStruct` (struct): Particle data structure (forward declared)

## Key Functions
### `Copy_Emitter_Property_Struct`
- Purpose: Copies keyframe property data from one struct to another
- Calls: `W3DNEWARRAY`, `memcpy`

## Globals
- `DefaultRemoveOnComplete` (static bool): Controls whether emitters auto-delete when complete
- `DebugDisable` (static bool): Debug flag to disable all particle emitters

## Dependencies
- `rendobj.h`, `random.h`, `part_buf.h`, `quat.h`, `w3d_file.h`, `w3derr.h`, `v3_rnd.h`
- `Vector3`, `Vector3Randomizer`, `Quaternion`, `TextureClass`, `ShaderClass`, `ParticleBufferClass`, `SceneClass`, `RenderInfoClass`, `AABoxClass`, `SphereClass`, `StringClass`, `DynamicVectorClass`
