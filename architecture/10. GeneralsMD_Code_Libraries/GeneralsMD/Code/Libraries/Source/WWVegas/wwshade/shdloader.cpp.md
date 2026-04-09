# GeneralsMD/Code/Libraries/Source/WWVegas/wwshade/shdloader.cpp

## Purpose
Implements shader mesh loading functionality for the SAGE engine, supporting both modern and legacy mesh formats.

## Responsibilities
- Loads shader meshes from W3D files
- Creates prototype objects for loaded meshes
- Handles legacy mesh conversion to shader meshes
- Manages reference counting for mesh objects

## Key Types
- `ShdMeshLoaderClass`: Loads modern shader meshes
- `ShdMeshLegacyLoaderClass`: Loads and converts legacy meshes to shader format
- `ShdMeshClass`: The shader mesh class (defined elsewhere)
- `MeshClass`: The legacy mesh class (defined elsewhere)
- `PrimitivePrototypeClass`: Prototype container for meshes

## Key Functions
### `ShdMeshLoaderClass::Load_W3D`
- Purpose: Loads a modern shader mesh from a W3D chunk
- Calls: `ShdMeshClass::Load_W3D`, `PrimitivePrototypeClass` constructor

### `ShdMeshLegacyLoaderClass::Load_W3D`
- Purpose: Loads a legacy mesh and converts it to shader format
- Calls: `MeshClass::Load_W3D`, `ShdMeshClass::Init_From_Legacy_Mesh`, `PrimitivePrototypeClass` constructor

## Globals
- `_ShdMeshLoader` (ShdMeshLoaderClass): Global instance for modern shader loading
- `_ShdMeshLegacyLoader` (ShdMeshLegacyLoaderClass): Global instance for legacy shader loading

## Dependencies
- `shdloader.h`, `shdmesh.h`, `mesh.h`
- `ChunkLoadClass`, `PrototypeClass`, `PrimitivePrototypeClass`, `WW3D_ERROR_OK`
- `NEW_REF`, `W3DNEW
