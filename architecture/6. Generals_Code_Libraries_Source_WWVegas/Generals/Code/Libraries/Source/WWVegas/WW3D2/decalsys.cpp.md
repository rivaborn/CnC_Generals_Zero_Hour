# Generals/Code/Libraries/Source/WWVegas/WW3D2/decalsys.cpp

## Purpose
Manages decal generation and rendering in the game's 3D engine.

## Responsibilities
- Manages decal IDs and generation
- Handles decal mesh registration and cleanup
- Provides pooling system for decal management
- Tracks decal transformations and material properties

## Key Types
- **DecalSystemClass**: Base class for decal management
- **DecalGeneratorClass**: Generates decals for meshes
- **MultiFixedPoolDecalSystemClass**: Manages decals in fixed-size pools
- **LogicalDecalClass**: Represents a single decal instance
- **LogicalDecalPoolClass**: Manages a pool of decals

## Key Functions
### DecalSystemClass::Lock_Decal_Generator
- Purpose: Creates and returns a new decal generator
- Calls: `W3DNEW`, `Generate_Decal_Id`

### DecalGeneratorClass::Add_Mesh
- Purpose: Registers a mesh that generates decals
- Calls: `MeshList.Add`

### MultiFixedPoolDecalSystemClass::Unlock_Decal_Generator
- Purpose: Registers a completed decal generator and cleans up
- Calls: `find_logical_decal`, `DecalSystemClass::Unlock_Decal_Generator`

### MultiFixedPoolDecalSystemClass::Clear_Decal_Slot
- Purpose: Removes a decal from a specific pool slot
- Calls: `find_logical_decal`, `encode_decal_id`

## Globals
- **DecalIDGenerator (uint32)**: Tracks unique decal IDs

## Dependencies
- `decalsys.h`, `rendobj.h`, `mesh.h`, `decalmsh.h`, `matrixmapper.h`, `texture.h`
- `MaterialPassClass`, `SurfaceClass`, `WW3D` namespace
- Memory allocation functions (`W3DNEW`, `W3DNEWARRAY`)
