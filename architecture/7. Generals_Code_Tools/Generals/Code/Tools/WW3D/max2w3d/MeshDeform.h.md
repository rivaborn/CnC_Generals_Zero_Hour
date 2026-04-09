# Generals/Code/Tools/WW3D/max2w3d/MeshDeform.h

## Purpose
Header file for a 3DS Max modifier plugin (MeshDeformClass) that handles mesh deformation operations for W3D export pipeline.

## Responsibilities
- Defines the MeshDeformClass modifier for 3DS Max
- Manages mesh deformation states and vertex colors
- Provides UI integration for deformation controls
- Handles transformation operations (move, rotate, scale)
- Manages multiple deformation sets

## Key Types
- MeshDeformClass (Class): Main modifier class for mesh deformation in 3DS Max
- MeshDeformPanelClass (Class): UI panel for deformation controls (forward declared)
- MeshDeformModData (Class): Modifier data container (forward declared)

## Key Functions
### Get_Mesh_Deform_Desc
- Purpose: Returns ClassDesc pointer for MeshDeformClass
- Calls: None

## Globals
- _MeshDeformClassID (Class_ID): Unique class identifier for MeshDeformClass

## Dependencies
- <Max.h>: 3DS Max SDK headers
- "Vector.H": Custom vector math library
- OSModifier: Base modifier class from 3DS Max SDK
- Various 3DS Max mode classes (SelectModBoxCMode, MoveModBoxCMode, etc.)
