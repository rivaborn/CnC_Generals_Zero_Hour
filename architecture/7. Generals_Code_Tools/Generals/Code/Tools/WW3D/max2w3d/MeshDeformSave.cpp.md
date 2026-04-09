# Generals/Code/Tools/WW3D/max2w3d/MeshDeformSave.cpp

## Purpose
Handles saving mesh deformation data for the W3D format, extracting deformation modifiers from 3D objects and serializing them into chunks.

## Responsibilities
- Extracts mesh deformation data from 3D object modifiers
- Serializes deformation data into W3D chunk format
- Manages deformation sets and keyframes
- Handles vertex reindexing and color/alpha conversion

## Key Types
- **MeshDeformSaveClass** (Class): Main class handling deformation save operations
- **MeshDeformSaveSetClass** (Class): Represents a single deformation set
- **DEFORM_DATA** (Struct): Contains vertex deformation data (position, color)
- **W3dMeshDeform** (Struct): Header structure for deformation chunks
- **W3dDeformSetInfo** (Struct): Information about a deformation set
- **W3dDeformKeyframeInfo** (Struct): Information about a deformation keyframe
- **W3dDeformData** (Struct): Per-vertex deformation data

## Key Functions
### Initialize (MeshBuilderClass &, Object *, Mesh &, Matrix3 *)
- Purpose: Initializes deformation data from a 3D object's modifiers
- Calls: Reset(), GetModifier(), GetModContext(), Initialize() (overload)

### Initialize (MeshBuilderClass &, Mesh &, MeshDeformModData &, Matrix3 *)
- Purpose: Initializes deformation data from modifier data
- Calls: Get_Set_Count(), Peek_Set(), Is_Empty(), Save()

### Export (ChunkSaveClass &)
- Purpose: Exports deformation data to a chunk save stream
- Calls: Begin_Chunk(), Write(), Export_Sets(), End_Chunk()

### Export_Sets (ChunkSaveClass &)
- Purpose: Exports all deformation sets to the chunk stream
- Calls: Begin_Chunk(), Write(), Export_Keyframes(), End_Chunk()

### Export_Keyframes (ChunkSaveClass &, MeshDeformSaveSetClass &)
- Purpose: Exports keyframe data for a deformation set
- Calls: Begin_Chunk(), Write(), End_Chunk()

### Does_Deformer_Modify_DCG (void)
- Purpose: Checks if deformation modifies vertex colors
- Calls: Get_Keyframe_Count(), Get_Deform_Data_Count(), Get_Deform_Data()

## Globals
- **m_DeformSets** (DynamicVectorClass<MeshDeformSaveSetClass*>): Stores all deformation sets
- **m_AlphaPasses** (int): Controls alpha handling in deformation data

## Dependencies
- MeshDeform.H, MeshDeformSave.H, MeshDeformData.H, MeshDeformSet.H, MeshDeformSave
