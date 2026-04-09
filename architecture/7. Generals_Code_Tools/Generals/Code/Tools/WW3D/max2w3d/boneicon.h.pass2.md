# Generals/Code/Tools/WW3D/max2w3d/boneicon.h - Enhanced Analysis

## Architectural Role
This header defines the geometric data structure for bone icons used in the 3D model conversion pipeline (max2w3d tool). It serves as a bridge between 3DS Max plugin development and W3D model format requirements.

## Cross-References
### Incoming
- `Generals/Code/Tools/WW3D/max2w3d/skin.cpp` (uses bone icon data for skinning visualization)
- `Generals/Code/Tools/WW3D/max2w3d/vxldbg.cpp` (debug visualization of bone hierarchy)

### Outgoing
- None (header-only, no external dependencies)

## Design Patterns
- **Data Module Pattern**: Encapsulates bone icon geometry as reusable data structures
- **Resource Pool**: Predefined vertex/face arrays suggest optimized memory layout for rendering
- **Not inferable**: No clear behavioral patterns (header-only)

*Cross-cutting insight*: This file represents the "asset pipeline" layer of the engine, where external tools (3DS Max) interact with the W3D format. The bone icon data is likely used during model export to visualize skeletal animation in the editor.
