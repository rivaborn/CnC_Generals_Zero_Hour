# Generals/Code/Tools/WW3D/max2w3d/meshbuild.h - Enhanced Analysis

## Architectural Role
This header defines the core mesh processing pipeline for the WW3D toolchain, bridging 3DS Max export tools with the game's W3D format. It abstracts mesh optimization, vertex/face management, and material handling, serving as the foundation for asset conversion workflows.

## Cross-References
### Incoming
- **max2w3d toolchain**: Uses MeshBuilderClass to process exported meshes
- **W3D exporter plugins**: Likely call into this for mesh preprocessing
- **Asset pipeline tools**: Depend on this for mesh validation and optimization

### Outgoing
- **Vector math utilities**: Uses Vector2/Vector3 for geometric operations
- **Memory management**: Allocates/deallocates vertex/face arrays internally
- **Winged-edge data structures**: For strip optimization (internal only)

## Design Patterns
- **Strategy Pattern**: WorldInfoClass abstracts external world data access
- **Builder Pattern**: MeshBuilderClass encapsulates complex mesh construction
- **Composite Pattern**: VertClass/FaceClass hierarchy manages mesh components

*Not inferable*: Exact usage of WingedEdge structures in strip optimization.
