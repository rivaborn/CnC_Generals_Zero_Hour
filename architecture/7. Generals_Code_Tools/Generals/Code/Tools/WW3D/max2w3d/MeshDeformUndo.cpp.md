# Generals/Code/Tools/WW3D/max2w3d/MeshDeformUndo.cpp

## Purpose
Implements undo/redo functionality for mesh deformations in the 3D modeling tool.

## Responsibilities
- Manages vertex position and color restoration for undo/redo operations
- Tracks mesh deformation state (sets and keyframes)
- Handles mesh geometry change notifications
- Provides redo support by storing pre-change vertex states

## Key Types
- **VertexRestoreClass (Class)**: Base class for undo operations on mesh deformations
- **VertexPositionRestoreClass (Class)**: Handles undo/redo for vertex position changes
- **VertexColorRestoreClass (Class)**: Handles undo/redo for vertex color changes
- **VERT_INFO (Struct)**: Stores vertex index, value, and color index

## Key Functions
### VertexRestoreClass::Restore
- Purpose: Restores mesh to previous state during undo
- Calls: Apply_Vertex_Data, m_pModifier->NotifyDependents, m_pModifier->Update_UI

### VertexRestoreClass::Redo
- Purpose: Reapplies changes after undo
- Calls: Apply_Vertex_Data, m_pModifier->NotifyDependents, m_pModifier->Update_UI

### VertexPositionRestoreClass::Copy_Vertex_State
- Purpose: Captures current vertex positions for undo
- Calls: m_pModData->Peek_Set, set_obj.Get_Vertex_Count, set_obj.Get_Vertex_Data

### VertexColorRestoreClass::Copy_Vertex_State
- Purpose: Captures current vertex colors for undo
- Calls: m_pModData->Peek_Set, set_obj.Get_Color_Count, set_obj.Get_Color_Data

## Globals
- None

## Dependencies
- MeshDeformUndo.H, Util.H, MeshDeformData.H, MeshDeformSet.H, MeshDeform.H
- Mesh, MeshDeformClass, MeshDeformModData, MeshDeformSetClass (external)
