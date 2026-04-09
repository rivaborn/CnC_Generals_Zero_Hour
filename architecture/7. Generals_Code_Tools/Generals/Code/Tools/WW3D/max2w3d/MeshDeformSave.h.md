# Generals/Code/Tools/WW3D/max2w3d/MeshDeformSave.h

## Purpose
Header file defining the `MeshDeformSaveClass` for exporting mesh deformation data in the max2w3d tool.

## Responsibilities
- Define the `MeshDeformSaveClass` for handling mesh deformation data.
- Provide methods for initializing, exporting, and managing deformation sets.
- Manage alpha passes for transparency effects.

## Key Types
- **MeshDeformSaveClass (Class)**: Main class for saving mesh deformation data.
- **DEFORM_SAVE_LIST (Class)**: Typedef for a dynamic vector of `MeshDeformSaveSetClass` pointers.
- **ChunkSaveClass (Class)**: Forward-declared class for chunk saving.
- **MeshDeformModData (Class)**: Forward-declared class for deformation modifier data.
- **MeshDeformSaveSetClass (Class)**: Forward-declared class for deformation sets.
- **MeshBuilderClass (Class)**: Forward-declared class for mesh building.

## Key Functions
### MeshDeformSaveClass::Initialize
- Purpose: Initialize the deformation save data from a mesh or modifier data.
- Calls: Not inferable (implementation in .cpp).

### MeshDeformSaveClass::Export
- Purpose: Export the deformation data to a chunk save.
- Calls: `Export_Sets`, `Export_Keyframes`.

### MeshDeformSaveClass::Export_Sets
- Purpose: Export deformation sets to a chunk save.
- Calls: Not inferable.

### MeshDeformSaveClass::Export_Keyframes
- Purpose: Export keyframe data for a deformation set.
- Calls: Not inferable.

## Globals
- None

## Dependencies
- `<Max.h>`: 3DS Max SDK headers.
- `"Vector.H"`: Custom vector class.
- Forward declarations for `ChunkSaveClass`, `Mesh
