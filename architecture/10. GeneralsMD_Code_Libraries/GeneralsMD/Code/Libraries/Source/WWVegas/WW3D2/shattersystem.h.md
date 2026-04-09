# GeneralsMD/Code/Libraries/Source/WWVegas/WW3D2/shattersystem.h

## Purpose
Declares the `ShatterSystem` class, which manages mesh shattering into fragments for physics and rendering.

## Responsibilities
- Initialize and shut down shatter system resources
- Shatter meshes into fragments at a given point with velocity
- Manage fragment access and lifecycle
- Process clip pools for mesh shattering

## Key Types
- **ShatterSystem (Class)**: Manages mesh shattering into fragments.
- **MeshClass (Class)**: Not inferable.
- **PhysicsSceneClass (Class)**: Not inferable.
- **RenderObjClass (Class)**: Not inferable.
- **Vector3 (Class)**: Not inferable.
- **Matrix3D (Class)**: Not inferable.
- **MeshMtlParamsClass (Class)**: Not inferable.

## Key Functions
### ShatterSystem::Init
- Purpose: Initialize shatter system resources and load BSP shatter planes.
- Calls: None.

### ShatterSystem::Shutdown
- Purpose: Release shatter system resources.
- Calls: None.

### ShatterSystem::Shatter_Mesh
- Purpose: Shatter a mesh into fragments at a specified point with given velocity.
- Calls: `Process_Clip_Pools`, `Reset_Clip_Pools`.

### ShatterSystem::Get_Fragment_Count
- Purpose: Return the number of mesh fragments created.
- Calls: None.

### ShatterSystem::Get_Fragment
- Purpose: Retrieve a reference-counted pointer to a fragment.
- Calls: None.

### ShatterSystem::Peek_Fragment
- Purpose: Retrieve a pointer to a fragment without incrementing reference count.
- Calls: None.

### ShatterSystem::Release_Fragments
- Purpose: Release references to fragments.
- Calls: None.

### Sh
