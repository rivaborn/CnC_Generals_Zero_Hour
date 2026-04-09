# Generals/Code/Libraries/Source/WWVegas/WW3D2/shattersystem.h

## Purpose
Header file defining the `ShatterSystem` class for mesh shattering functionality in the SAGE engine.

## Responsibilities
- Manages mesh shattering into fragments
- Handles fragment creation and retrieval
- Initializes and shuts down shatter system resources
- Processes clip pools for shattering operations

## Key Types
- **ShatterSystem (Class)**: Manages mesh shattering operations and fragment handling
- **MeshClass (Class)**: External mesh class used for shattering
- **RenderObjClass (Class)**: External render object class for fragments
- **Vector3 (Class)**: External 3D vector class
- **Matrix3D (Class)**: External 3D matrix class
- **MeshMtlParamsClass (Class)**: External mesh material parameters class
- **PhysicsSceneClass (Class)**: External physics scene class

## Key Functions
### ShatterSystem::Init
- Purpose: Initializes the shatter system and loads BSP shatter planes
- Calls: Not inferable

### ShatterSystem::Shatter_Mesh
- Purpose: Shatters a mesh into fragments at a specified point with given velocity
- Calls: Process_Clip_Pools, Reset_Clip_Pools

### ShatterSystem::Get_Fragment_Count
- Purpose: Returns the number of mesh fragments created
- Calls: None

### ShatterSystem::Get_Fragment
- Purpose: Returns a reference-counted pointer to a specific fragment
- Calls: None

### ShatterSystem::Release_Fragments
- Purpose: Releases references to all fragments
- Calls: None

### ShatterSystem::Process_Clip_Pools
- Purpose: Processes clip pools for shattering operations
- Calls: None

## Globals
None

## Dependencies
