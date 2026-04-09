# Generals/Code/Libraries/Source/WWVegas/WW3D2/part_ldr.h

## Purpose
Defines particle emitter asset classes and loader for the W3D engine, handling serialization and prototype management.

## Responsibilities
- Defines `ParticleEmitterDefClass` for emitter properties and serialization
- Provides `ParticleEmitterPrototypeClass` for runtime emitter instantiation
- Implements `ParticleEmitterLoaderClass` for W3D file loading
- Manages particle emitter keyframes, randomizers, and line properties

## Key Types
- **ParticleEmitterDefClass (Class)**: Stores particle emitter definition and serialization logic
- **ParticleEmitterPrototypeClass (Class)**: Prototype for creating runtime emitter instances
- **ParticleEmitterLoaderClass (Class)**: Handles W3D file loading for emitters
- **Vector3Randomizer (Class)**: Not defined here (forward declared)
- **ChunkLoadClass/ChunkSaveClass (Class)**: Not defined here (forward declared)

## Key Functions
### `Load_W3D`/`Save_W3D`
- Purpose: Serialize particle emitter definitions to/from W3D files
- Calls: `Read_Header`, `Read_Info`, `Read_Props`, etc. (load); `Save_Header`, `Save_Info`, etc. (save)

### `Create_Randomizer`
- Purpose: Factory method for creating `Vector3Randomizer` instances
- Calls: Not inferable

### `Initialize_To_Ver2`/`Convert_To_Ver2`
- Purpose: Version compatibility methods for emitter definitions
- Calls: Not inferable

## Globals
- **_ParticleEmitterLoader (ParticleEmitterLoaderClass)**: Global loader instance for particle emitters

## Dependencies
- `proto.h`, `rendobj.h`, `w3d_file.h`, `w3derr.h`, `w3d_util.h`, `part_emt.h`
- `ChunkLoadClass`, `ChunkSaveClass`, `Vector3Randomizer` (forward declared)
- `W3DMPO`, `PrototypeClass`, `RenderObjClass` (inheritance)
