# Generals/Code/Tools/WW3D/max2w3d/vxllayer.cpp - Enhanced Analysis

## Architectural Role
This file implements the core voxelization pipeline for 3D model export, bridging between 3DS Max's polygon mesh representation and the W3D voxel format. It handles the critical transformation from surface geometry to volumetric representation, which is fundamental to the SAGE engine's rendering pipeline.

## Cross-References
### Incoming
- `max2w3d` exporter tool (likely calls `VoxelLayerClass` constructor and rendering methods)
- 3DS Max plugin infrastructure (uses MAX SDK types like `INode`, `TriObject`)

### Outgoing
- `PlaneClass` from `plane.h` (for clipping operations)
- MAX SDK geometry functions (mesh iteration, transformation)

## Design Patterns
- **Scanline Rendering**: Implements traditional scanline conversion for polygon rasterization into voxel space
- **Barycentric Coordinates**: Uses barycentric interpolation for texture coordinate and attribute mapping during voxelization
- **Spatial Partitioning**: Clips geometry against voxel slab boundaries to optimize voxel generation

*Not inferable*: No clear use of object-oriented patterns beyond basic class structure.
