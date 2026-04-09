# Generals/Code/Libraries/Source/WWVegas/WW3D2/part_ldr.cpp

## Purpose
Handles loading and saving of particle emitter definitions in the W3D format.

## Responsibilities
- Manages `ParticleEmitterDefClass` for emitter properties (color, size, opacity, rotation, etc.)
- Implements chunk-based I/O for emitter data
- Handles version compatibility for emitter definitions
- Provides prototype creation for runtime emitter instances

## Key Types
- **ParticleEmitterDefClass** (Class): Core emitter definition with keyframes, textures, and randomizers
- **ParticleEmitterPrototypeClass** (Class): Prototype factory for emitter instances
- **ParticleEmitterLoaderClass** (Class): Loader singleton for W3D emitter files

## Key Functions
### `ParticleEmitterDefClass::Load_W3D`
- Purpose: Loads emitter definition from chunk stream
- Calls: `Read_Header`, `Read_User_Data`, `Read_Info`, `Read_InfoV2`, `Read_Props`

### `ParticleEmitterDefClass::Save_W3D`
- Purpose: Saves emitter definition to chunk stream
- Calls: `Save_Header`, `Save_User_Data`, `Save_Info`, `Save_InfoV2`, `Save_Props`

### `ParticleEmitterLoaderClass::Load_W3D`
- Purpose: Factory method for loading emitter prototypes
- Calls: `ParticleEmitterDefClass::Load_W3D`, `ParticleEmitterPrototypeClass` constructor

## Globals
- `_ParticleEmitterLoader` (ParticleEmitterLoaderClass): Singleton loader instance
- `EMITTER_TYPE_NAMES` (const char*): Array of emitter type names

## Dependencies
- `part_ldr.h`, `part_emt.h`, `w3derr.h`, `chunkio.h`, `win.h`, `assetmgr.h`, `texture.h`
- `ChunkLoadClass`, `ChunkSaveClass`, `Vector3Randomizer`, `ParticlePropertyStruct`
