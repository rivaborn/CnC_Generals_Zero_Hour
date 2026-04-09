# Generals/Code/Tools/WW3D/max2w3d/MeshDeformUndo.h

## Purpose
Defines undo/redo functionality for mesh deformation operations in the 3DS Max plugin.

## Responsibilities
- Provides base class for vertex state restoration
- Implements position and color-specific restoration classes
- Manages vertex data storage for undo/redo operations
- Integrates with 3DS Max's RestoreObj system

## Key Types
- **VertexRestoreClass (Class)**: Base class for vertex state restoration
- **VertexPositionRestoreClass (Class)**: Restores vertex positions
- **VertexColorRestoreClass (Class)**: Restores vertex colors
- **MeshDeformClass (Class)**: Forward declaration of modifier class
- **MeshDeformModData (Class)**: Forward declaration of modifier data

## Key Functions
### VertexRestoreClass::Restore
- Purpose: Restores vertex state from backup
- Calls: Copy_Vertex_State, Apply_Vertex_Data

### VertexRestoreClass::Redo
- Purpose: Re-applies the deformation
- Calls: Apply_Vertex_Data

### VertexPositionRestoreClass::Copy_Vertex_State
- Purpose: Captures current vertex positions
- Calls: None

### VertexColorRestoreClass::Copy_Vertex_State
- Purpose: Captures current vertex colors
- Calls: None

## Globals
- None

## Dependencies
- `<Max.H>` (3DS Max SDK)
- `"Vector.H"` (custom vector class)
- `"MeshDeformDefs.H"` (deformation definitions)
- `RestoreObj` (3DS Max base class)
- `Point3` (3D point structure)
- `TSTR` (string class)
- `DEFORM_LIST` (custom list type)
