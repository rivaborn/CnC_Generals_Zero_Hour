# Generals/Code/Tools/WW3D/max2w3d/MeshDeformData.h

## Purpose
Defines the `MeshDeformModData` class for managing mesh deformation data in the 3DS Max plugin.

## Responsibilities
- Manages multiple deformation sets for a mesh
- Provides accessors for vertex data and deformation states
- Handles saving/loading deformation data
- Controls auto-apply behavior for deformations

## Key Types
- `SETS_LIST` (typedef): Dynamic vector of `MeshDeformSetClass` pointers
- `MeshDeformModData` (Class): Main class for mesh deformation data management

## Key Functions
### `Record_Mesh_State`
- Purpose: Records the current state of a mesh for deformation tracking
- Calls: `MeshDeformSetClass` methods

### `Save` / `Load`
- Purpose: Persists deformation data to/from disk
- Calls: `ISave`/`ILoad` interface methods

### `Restore_Set`
- Purpose: Restores a mesh to a specific deformation set state
- Calls: `Util_Restore_Set`

## Globals
- None

## Dependencies
- `<Max.h>` (3DS Max SDK)
- `"Vector.H"` (custom vector class)
- `"MeshDeformSet.H"` (deformation set class)
- Inherits from `LocalModData` (3DS Max modifier data base class)
