# Generals/Code/Tools/WW3D/max2w3d/MeshDeform.cpp - Enhanced Analysis

## Architectural Role
This file implements a 3DS Max modifier plugin specifically for the W3D export pipeline, bridging between Max's scene graph and the W3D format's mesh deformation requirements. It handles vertex-level transformations and selection states that are critical for the W3D's skeletal animation system.

## Cross-References
### Incoming
- Called by 3DS Max's modifier evaluation system during scene evaluation
- Used by max2w3d export tool when processing mesh assets
- Referenced by MeshDeformPanel.cpp for UI state synchronization

### Outgoing
- Calls into MeshDeformData.cpp for deformation state management
- Uses MeshDeformUndo.cpp for undo/redo functionality
- Interfaces with 3DS Max SDK for modifier evaluation and UI integration

## Design Patterns
- **Plugin Architecture**: Implements ClassDesc pattern for 3DS Max plugin registration
- **State Management**: Uses ModContext for maintaining deformation state across evaluations
- **Observer Pattern**: Notifies dependents when selection changes via NotifyDependents

*Not inferable*: Exact undo/redo implementation details (commented out sections suggest historical changes)
