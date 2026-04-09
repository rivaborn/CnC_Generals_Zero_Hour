# Generals/Code/Tools/WW3D/max2w3d/MeshDeformSet.cpp

## Purpose
Manages mesh deformation sets for 3D models, handling vertex position and color changes across keyframes.

## Responsibilities
- Tracks vertex/color deformations per keyframe
- Serializes/deserializes deformation data
- Updates and collapses deformation data
- Manages affected vertex sets

## Key Types
- `MeshDeformSetClass`: Manages mesh deformations across keyframes
- `KEY_FRAME` (struct): Stores deformation data for a single keyframe
- `VERT_INFO` (struct): Vertex deformation info (index, value, color index)

## Key Functions
### `Set_Current_Key_Frame`
- Purpose: Sets the active keyframe index
- Calls: None

### `Set_Vertex_Position`
- Purpose: Records vertex position changes for current keyframe
- Calls: None

### `Update_Set_Members`
- Purpose: Rebuilds list of affected vertices across all keyframes
- Calls: None

### `Save`
- Purpose: Serializes deformation data to save format
- Calls: `Apply_Position_Changes`, `Apply_Color_Changes`

### `Load`
- Purpose: Deserializes deformation data from save format
- Calls: None

## Globals
- `MAX_DEFORM_KEY_FRAMES` (const int): Maximum allowed keyframes (10)

## Dependencies
- `MeshDeformSet.H`, `Util.H`, `MeshDeformSaveSet.H`, `MeshBuild.H`, `MeshDeformSaveDefs.H`, `MeshDeformDefs.H`
- `Point3`, `VertColor`, `BitArray`, `Matrix3` types
- `MeshBuilderClass`, `MeshDeformSaveSetClass` classes
