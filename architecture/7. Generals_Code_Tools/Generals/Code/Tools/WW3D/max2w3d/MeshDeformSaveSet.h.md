# Generals/Code/Tools/WW3D/max2w3d/MeshDeformSaveSet.h

## Purpose
Defines a class for managing mesh deformation data in 3D models, including keyframes and vertex positions/colors.

## Responsibilities
- Store deformation data for 3D mesh vertices
- Manage keyframes for animated deformations
- Provide access to deformation states and vertex data
- Handle flags for additional state information

## Key Types
- **MeshDeformSaveSetClass (Class)**: Main class for managing mesh deformation data.
- **_DEFORM_DATA (Class)**: Represents deformation data for a single vertex (index, position, color).
- **KEYFRAME (Class)**: Contains deformation state and list of vertex deformations at a specific time.

## Key Functions
### MeshDeformSaveSetClass::Begin_Keyframe
- Purpose: Starts a new keyframe for deformation tracking.
- Calls: Not inferable.

### MeshDeformSaveSetClass::Add_Vert
- Purpose: Adds vertex deformation data to the current keyframe.
- Calls: Not inferable.

### MeshDeformSaveSetClass::Reset
- Purpose: Clears all deformation data.
- Calls: Not inferable.

### MeshDeformSaveSetClass::Replace_Deform_Data
- Purpose: Replaces deformation data for a specific keyframe.
- Calls: Not inferable.

## Globals
- None

## Dependencies
- `<Max.h>` (3DS Max SDK)
- `"Vector.H"` (local vector class)
- `ChunkSaveClass` (forward declared)
- `DynamicVectorClass` (used for container storage)
