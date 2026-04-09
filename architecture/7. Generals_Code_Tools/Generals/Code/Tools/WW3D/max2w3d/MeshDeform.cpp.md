# Generals/Code/Tools/WW3D/max2w3d/MeshDeform.cpp

## Purpose
Implements a 3DS Max modifier plugin for mesh deformation in the W3D export pipeline.

## Responsibilities
- Defines the MeshDeformClassDesc for plugin registration
- Manages vertex selection and deformation across multiple sets
- Handles UI integration with 3DS Max rollup panels
- Implements transformation modes (move, rotate, scale)
- Maintains deformation state and keyframe data

## Key Types
- MeshDeformClassDesc (Class): Plugin class descriptor for 3DS Max
- MeshDeformClass (Class): Main modifier class implementing deformation logic

## Key Functions
### ModifyObject
- Purpose: Applies deformation to mesh geometry
- Calls: mod_data->Record_Mesh_State, tri_obj->PointsWereChanged, tri_obj->UpdateValidity

### BeginEditParams
- Purpose: Initializes UI and mode handlers when modifier is selected
- Calls: m_MaxInterface->AddRollupPage, MeshDeformPanelClass::Get_Object, max_interface->RegisterSubObjectTypes

### Set_Current_Set
- Purpose: Switches between deformation sets and updates selection
- Calls: mod_data->Set_Current_Set, mod_data->Select_Set, m_MaxInterface->RedrawViews

## Globals
- _MeshDeformClassID (Class_ID): Unique identifier for the modifier class
- last_delta (Point3): Stores last transformation delta
- last_scale (Point3): Stores last scaling factors
- last_rot (Quat): Stores last rotation quaternion

## Dependencies
- MeshDeform.H, MeshDeformData.H, MeshDeformPanel.H, MeshDeformUndo.H
- DLLMain.H, Resource.H, Util.H
- 3DS Max SDK classes (ClassDesc, IObjParam, ModContext, etc.)
