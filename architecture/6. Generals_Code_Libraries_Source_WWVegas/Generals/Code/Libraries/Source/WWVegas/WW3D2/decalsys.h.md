# Generals/Code/Libraries/Source/WWVegas/WW3D2/decalsys.h

## Purpose
Defines the decal system architecture for rendering decals on 3D meshes in the SAGE engine.

## Responsibilities
- Manages decal generation and lifecycle
- Provides interfaces for decal creation/destruction
- Tracks meshes affected by decals
- Supports multiple decal pools for organization

## Key Types
- **DecalSystemClass (Class)**: Base class for decal management systems
- **DecalGeneratorClass (Class)**: Encapsulates decal generation parameters and tracks affected meshes
- **MultiFixedPoolDecalSystemClass (Class)**: Manages multiple fixed-size decal pools
- **LogicalDecalClass (Class)**: Stores mesh references for a specific decal
- **LogicalDecalPoolClass (Class)**: Manages an array of logical decals

## Key Functions
### DecalSystemClass::Lock_Decal_Generator
- Purpose: Creates and returns a decal generator
- Calls: Generate_Decal_Id

### DecalSystemClass::Unlock_Decal_Generator
- Purpose: Releases a decal generator back to the system
- Calls: None

### DecalGeneratorClass::Add_Mesh
- Purpose: Registers a mesh that generated decal polygons
- Calls: None

### MultiFixedPoolDecalSystemClass::Clear_Decal_Slot
- Purpose: Removes a decal from a specific pool slot
- Calls: find_logical_decal

## Globals
- **DecalIDGenerator (uint32)**: Static counter for generating unique decal IDs

## Dependencies
- `matrix3d.h`, `matrix4.h`, `obbox.h`, `robjlist.h`, `matpass.h`, `projector.h`
- `ProjectorClass`, `MaterialPassClass`, `RenderObjClass`
