# Generals/Code/Tools/WW3D/max2w3d/MeshDeformSet.h

## Purpose
Header file defining the `MeshDeformSetClass` for managing mesh deformations in 3D models.

## Responsibilities
- Manages vertex and color deformations across keyframes
- Handles interpolation between keyframes
- Provides methods for saving/loading deformation data
- Supports auto-apply functionality for deformations

## Key Types
- **MeshDeformSetClass (Class)**: Main class for mesh deformation management
- **KEY_FRAME (struct)**: Stores vertex/color deformation data and affected flags
- **KEY_FRAME_LIST (typedef)**: Dynamic vector of KEY_FRAME pointers

## Key Functions
### MeshDeformSetClass()
- Purpose: Constructor initializing deformation set
- Calls: `Init_Key_Frames()`

### Update_Mesh()
- Purpose: Updates mesh with current deformation state
- Calls: Not inferable

### Save()
- Purpose: Saves deformation data to persistent storage
- Calls: Not inferable

### Apply_Position_Changes()
- Purpose: Applies vertex position changes from keyframes
- Calls: Not inferable

## Globals
- None

## Dependencies
- `<Max.h>` (3DS Max SDK)
- `"Vector.H"`
- `"MeshDeformDefs.H"`
- `MeshDeformSaveSetClass` (forward declared)
- `MeshBuilderClass` (forward declared)
