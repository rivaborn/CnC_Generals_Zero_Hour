# GeneralsMD/Code/Libraries/Source/WWVegas/WW3D2/part_ldr.h

## Purpose
Defines classes for loading and managing particle emitter definitions and prototypes in the W3D engine.

## Responsibilities
- Declares `ParticleEmitterDefClass` for particle emitter properties
- Defines `ParticleEmitterPrototypeClass` for creating emitter instances
- Provides `ParticleEmitterLoaderClass` for W3D file loading
- Manages particle emitter serialization (load/save)
- Handles keyframe animations and randomizers for emitters

## Key Types
- **ParticleEmitterDefClass (Class)**: Stores particle emitter properties and serialization methods
- **ParticleEmitterPrototypeClass (Class)**: Prototype for creating emitter instances
- **ParticleEmitterLoaderClass (Class)**: Handles W3D file loading for emitters
- **ChunkLoadClass (Class)**: Forward declaration for chunk loading interface
- **ChunkSaveClass (Class)**: Forward declaration for chunk saving interface
- **Vector3Randomizer (Class)**: Forward declaration for randomizer utility

## Key Functions
### `Load_W3D`
- Purpose: Load emitter definition from W3D chunk
- Calls: `Read_Header`, `Read_User_Data`, `Read_Info`, etc.

### `Save_W3D`
- Purpose: Save emitter definition to W3D chunk
- Calls: `Save_Header`, `Save_User_Data`, `Save_Info`, etc.

### `Load_W3D` (in ParticleEmitterLoaderClass)
- Purpose: Factory method for loading emitter prototypes
- Calls: Constructor, `ParticleEmitterDefClass::Load_W3D`

## Globals
- **_ParticleEmitterLoader (ParticleEmitterLoaderClass)**: Global loader instance

## Dependencies
- `proto.h`, `rendobj.h`, `w3d_file.h`, `w3derr.h`, `w3d_util.h`, `part_emt.h`
- `ChunkLoadClass`, `ChunkSaveClass`, `Vector3Randomizer` (forward declarations)
- `W3DMPO`, `PrototypeClass`, `RenderObjClass` (inheritance)
