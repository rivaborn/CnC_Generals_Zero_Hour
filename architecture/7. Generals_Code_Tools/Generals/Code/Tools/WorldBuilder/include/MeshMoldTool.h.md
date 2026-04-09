# Generals/Code/Tools/WorldBuilder/include/MeshMoldTool.h

## Purpose
Defines the MeshMoldTool class for terrain shaping operations in the WorldBuilder tool.

## Responsibilities
- Manages mesh-based terrain deformation
- Handles mouse input for terrain editing
- Maintains terrain height map modifications
- Provides preview and application of mesh changes

## Key Types
- MeshMoldTool (Class): Terrain shaping tool for mesh-based deformations
- WorldHeightMapEdit (Class): Reference to height map edits (external)

## Key Functions
### MeshMoldTool()
- Purpose: Constructor for MeshMoldTool
- Calls: None

### ~MeshMoldTool()
- Purpose: Destructor for MeshMoldTool
- Calls: None

### applyMesh()
- Purpose: Applies mesh modifications to a copy of the terrain
- Calls: None

### apply()
- Purpose: Applies mesh changes to the actual terrain with undo support
- Calls: applyMesh()

### mouseDown()
- Purpose: Handles mouse down events for terrain editing
- Calls: None

### mouseUp()
- Purpose: Handles mouse up events for terrain editing
- Calls: None

### mouseMoved()
- Purpose: Handles mouse movement for terrain editing preview
- Calls: None

### activate()
- Purpose: Activates the mesh mold tool
- Calls: None

### deactivate()
- Purpose: Deactivates the mesh mold tool
- Calls: None

### updateMeshLocation()
- Purpose: Updates the mesh position for preview
- Calls: None

## Globals
- m_toolPos (Coord3D): Current location of the mesh on terrain
- m_tracking (Bool): Tracks whether mesh is being moved
- m_htMapEditCopy (WorldHeightMapEdit*): Reference-counted height map edit copy

## Dependencies
