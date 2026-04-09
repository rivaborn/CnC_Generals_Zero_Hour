# GeneralsMD/Code/Libraries/Source/WWVegas/wwshade/shdloader.h

## Purpose
Defines prototype loaders for shader meshes and legacy mesh conversion in the SAGE engine.

## Responsibilities
- Declares `ShdMeshLoaderClass` for loading shader meshes.
- Declares `ShdMeshLegacyLoaderClass` for converting legacy meshes to shader meshes.
- Provides global instances of both loaders.
- Integrates with the W3D chunk loading system.

## Key Types
- **ShdMeshLoaderClass (Class)**: Loader for shader mesh prototypes.
- **ShdMeshLegacyLoaderClass (Class)**: Loader for converting legacy meshes to shader meshes.

## Key Functions
### `ShdMeshLoaderClass::Chunk_Type`
- Purpose: Returns the chunk type for shader meshes.
- Calls: None.

### `ShdMeshLoaderClass::Load_W3D`
- Purpose: Loads a shader mesh from a W3D chunk.
- Calls: Not inferable (implementation in `.cpp`).

### `ShdMeshLegacyLoaderClass::Chunk_Type`
- Purpose: Returns the chunk type for legacy meshes.
- Calls: None.

### `ShdMeshLegacyLoaderClass::Load_W3D`
- Purpose: Converts a legacy mesh to a shader mesh.
- Calls: Not inferable (implementation in `.cpp`).

## Globals
- `_ShdMeshLoader (ShdMeshLoaderClass)`: Global instance of the shader mesh loader.
- `_ShdMeshLegacyLoader (ShdMeshLegacyLoaderClass)`: Global instance of the legacy mesh loader.

## Dependencies
- `proto.h`: Base `PrototypeLoaderClass` and related types.
- `W3D_CHUNK_SHDMESH` and `W3D_CHUNK_MESH`: Chunk type constants.
