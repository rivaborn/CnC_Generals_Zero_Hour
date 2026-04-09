# GeneralsMD/Code/Libraries/Source/WWVegas/WW3D2/decalsys.cpp

## Purpose
Manages decal generation and rendering in the game engine, including decal ID management and mesh association.

## Responsibilities
- Manages decal ID generation and pooling
- Handles decal generator lifecycle (lock/unlock)
- Tracks meshes associated with decals
- Provides decal system implementation with fixed-size pools

## Key Types
- **DecalSystemClass** (Class): Base decal system interface
- **DecalGeneratorClass** (Class): Generates decals for meshes
- **MultiFixedPoolDecalSystemClass** (Class): Manages decals in fixed-size pools
- **LogicalDecalClass** (Struct): Represents a logical decal with mesh associations
- **LogicalDecalPoolClass** (Struct): Manages a pool of logical decals

## Key Functions
### DecalSystemClass::Lock_Decal_Generator
- Purpose: Creates and returns a new decal generator
- Calls: `W3DNEW`, `Generate_Decal_Id`

### DecalGeneratorClass::Add_Mesh
- Purpose: Adds a mesh to the generator's mesh list
- Calls: `MeshList.Add`

### MultiFixedPoolDecalSystemClass::Unlock_Decal_Generator
- Purpose: Registers a decal generator and cleans up
- Calls: `find_logical_decal`, `DecalSystemClass::Unlock_Decal_Generator`

### MultiFixedPoolDecalSystemClass::Clear_Decal_Slot
- Purpose: Removes decal from a specific pool slot
- Calls: `find_logical_decal`, `LogicalDecalClass::Clear`

## Globals
- **DecalIDGenerator** (uint32): Global counter for generating unique decal IDs

## Dependencies
- `decalsys.h`, `rendobj.h`, `mesh.h`, `decalmsh.h`, `matrixmapper.h`, `texture.h`
- `MaterialPassClass`, `Matrix3D`, `Matrix4x4`, `TextureClass`, `MeshClass`, `DecalMeshClass`
