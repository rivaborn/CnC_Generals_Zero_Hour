# Generals/Code/Libraries/Source/WWVegas/WW3D2/meshgeometry.cpp - Enhanced Analysis

## Architectural Role
Core 3D mesh management component in the WW3D2 rendering subsystem, bridging between W3D file I/O and runtime geometry operations. Acts as the central data structure for all mesh-related operations including collision detection, spatial queries, and mesh transformations.

## Cross-References
### Incoming
- Rendering pipeline (e.g., `WW3D2/render.cpp` for mesh drawing)
- Physics/collision system (e.g., `WW3D2/collision.cpp` for spatial queries)
- Animation system (e.g., `WW3D2/skin.cpp` for vertex influences)
- W3D file loader (e.g., `WW3D2/w3d_file.cpp` for model loading)

### Outgoing
- **AABTreeClass** (spatial partitioning for culling)
- **ChunkLoadClass** (W3D file parsing)
- **ShareBufferClass** (memory management)
- **Math primitives** (Vector3/4, Plane, AABox, OBBox)

## Design Patterns
- **Resource Pooling**: Global `_PlaneEQArray` and `_VNormArray` buffers for optimization
- **Composite**: Mesh geometry as container for vertices, polygons, and spatial data
- **Strategy**: Multiple collision detection algorithms (e.g., `cast_aabox_*`) selected at runtime

*Not inferable*: Exact factory usage for mesh creation, observer pattern for mesh updates.
