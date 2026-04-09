# Generals/Code/Tools/WW3D/max2w3d/MeshDeformData.cpp

## Purpose
Manages mesh deformation data for 3D models in the Max2W3D toolchain.

## Responsibilities
- Maintains a list of deformation sets for a mesh
- Handles recording and restoring mesh states
- Manages loading/saving deformation data
- Updates mesh geometry based on deformation sets

## Key Types
- `MeshDeformModData` (Class): Main deformation data container
- `MeshDeformSetClass` (Class): Individual deformation set
- `DeformChunk` (Struct): Data structure for saving/loading

## Key Functions
### `Record_Mesh_State`
- Purpose: Updates mesh state for all deformation sets
- Calls: `Set_State`, `Update_Mesh`

### `Free_Sets_List`
- Purpose: Cleans up all deformation sets
- Calls: `SAFE_DELETE`

### `Set_Max_Deform_Sets`
- Purpose: Adjusts the number of deformation sets
- Calls: `Restore_Set`, `SAFE_DELETE`

### `Save`
- Purpose: Serializes deformation data to a save object
- Calls: `BeginChunk`, `Write`, `EndChunk`

### `Load`
- Purpose: Deserializes deformation data from a load object
- Calls: `OpenChunk`, `Read`, `CloseChunk`

## Globals
None

## Dependencies
- `MeshDeformData.H`
- `Util.H`
- `MeshDeformSaveDefs.H`
- `TriObject` (3DS Max SDK)
- `ISave`, `ILoad` (Max2W3D save/load interfaces)
