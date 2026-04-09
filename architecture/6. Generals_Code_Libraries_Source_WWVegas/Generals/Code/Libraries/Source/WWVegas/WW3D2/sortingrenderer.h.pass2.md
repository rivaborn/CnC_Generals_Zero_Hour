# Generals/Code/Libraries/Source/WWVegas/WW3D2/sortingrenderer.h - Enhanced Analysis

## Architectural Role
This file defines the `SortingRendererClass`, a core component of the SAGE engine's rendering pipeline. It manages deferred sorting and rendering of geometry (triangles and volume particles) based on bounding spheres, enabling proper transparency and depth handling.

## Cross-References
### Incoming
- Likely called by rendering subsystems (e.g., `WW3D2/renderer.cpp`) for geometry submission.
- Used by particle systems (e.g., `WW3D2/particle.cpp`) for volume particle insertion.
- Accessed by debug tools (e.g., `_Enable_Triangle_Draw` toggles).

### Outgoing
- Depends on `SphereClass` for bounding volume calculations.
- Interacts with GPU state management (e.g., vertex buffer sizing via `SetMinVertexBufferSize`).
- Uses internal `SortingNodeStruct` for pool management.

## Design Patterns
- **Strategy Pattern**: Deferred rendering logic is encapsulated, allowing different sorting strategies (e.g., by distance, layer).
- **Object Pool**: Likely uses a pre-allocated pool (`SortingNodeStruct`) for efficient memory management.
- **Facade**: Hides complexity of sorting/flushing behind simple public methods.
