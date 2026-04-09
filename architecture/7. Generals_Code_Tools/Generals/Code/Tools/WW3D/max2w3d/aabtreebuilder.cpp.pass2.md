# Generals/Code/Tools/WW3D/max2w3d/aabtreebuilder.cpp - Enhanced Analysis

## Architectural Role
This file implements the AABB tree construction tool used during the asset pipeline to pre-process 3D models for efficient runtime culling in the W3D rendering system. It bridges the gap between 3DS Max plugin tools and the runtime W3D engine by generating spatial partitioning data.

## Cross-References
### Incoming
- **max2w3d plugin tools**: Likely calls `Build_AABTree` and `Export` to process 3D models
- **W3D asset pipeline**: Uses the generated chunk data for runtime culling

### Outgoing
- **chunkio.h**: Uses `ChunkSaveClass` for W3D chunk serialization
- **w3d_file.h**: References W3D-specific types like `W3dMeshAABTreeNode`
- **Memory management**: Directly allocates/deletes arrays for tree nodes and polygons

## Design Patterns
- **Recursive Composition**: Tree building uses recursive methods (`Build_Tree`, `Build_W3D_AABTree_Recursive`) to partition space
- **Visitor Pattern**: `Export` method traverses the tree structure to serialize it
- **Strategy Pattern**: `Select_Splitting_Plane` implements a strategy for choosing optimal partitions

*Not inferable*: Exact relationship with W3D runtime AABTreeClass loading mechanism.
