# Generals/Code/Tools/WW3D/max2w3d/MeshDeformUndo.h - Enhanced Analysis

## Architectural Role
This file defines the undo/redo infrastructure for mesh deformations in the 3DS Max plugin, bridging the game's W3D pipeline with Max's native undo system. It enables non-destructive editing of vertex data during asset creation.

## Cross-References
### Incoming
- `MeshDeformClass` (uses undo/redo functionality)
- `MeshDeformModData` (stores deformation state)
- 3DS Max's `RestoreObj` system (base class integration)

### Outgoing
- Directly manipulates `Mesh` objects (3DS Max SDK)
- Uses `DEFORM_LIST` (custom container from `MeshDeformDefs.H`)
- Relies on `Point3` for vertex storage

## Design Patterns
- **Template Method**: `Copy_Vertex_State`/`Apply_Vertex_Data` define hooks for position/color-specific implementations.
- **Memento**: Captures and restores vertex state for undo/redo.
- **Composite**: `VertexRestoreClass` aggregates vertex data for batch operations.

*Not inferable*: Exact integration with Max's undo stack or threading model.
