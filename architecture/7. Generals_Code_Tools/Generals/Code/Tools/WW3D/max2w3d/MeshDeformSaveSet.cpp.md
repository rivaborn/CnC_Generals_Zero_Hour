# Generals/Code/Tools/WW3D/max2w3d/MeshDeformSaveSet.cpp

## Purpose
Manages mesh deformation keyframes and vertex data for 3D model export in the max2w3d tool.

## Responsibilities
- Stores keyframe-based mesh deformations
- Manages vertex position/color data per keyframe
- Provides interface for adding/replacing deformation data
- Handles memory cleanup for deformation structures

## Key Types
- `MeshDeformSaveSetClass`: Manages deformation keyframes and vertex data
- `KEYFRAME` (struct): Contains deformation state and list of vertex deformations
- `DEFORM_DATA` (struct): Stores vertex index, position, and color

## Key Functions
### `Reset`
- Purpose: Clears all keyframe data and resets the current keyframe pointer
- Calls: `m_DeformData.Count()`, `SAFE_DELETE`, `m_DeformData.Delete_All()`

### `Begin_Keyframe`
- Purpose: Starts a new keyframe with the given state value
- Calls: `new KEYFRAME`, `m_DeformData.Add()`

### `End_Keyframe`
- Purpose: Ends the current keyframe (sets pointer to NULL)
- Calls: None

### `Add_Vert`
- Purpose: Adds vertex deformation data to the current keyframe
- Calls: `m_CurrentKeyFrame->deform_list.Add()`

### `Replace_Deform_Data`
- Purpose: Replaces vertex deformation list for a specific keyframe
- Calls: `key_frame->deform_list.Delete_All()`

## Globals
- `m_DeformData` (DynamicVectorClass<KEYFRAME*>): Stores all keyframe data
- `m_CurrentKeyFrame` (KEYFRAME*): Pointer to the active keyframe being edited

## Depend
