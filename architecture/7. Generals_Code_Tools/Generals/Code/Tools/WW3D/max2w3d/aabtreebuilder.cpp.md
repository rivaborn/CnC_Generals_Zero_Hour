# Generals/Code/Tools/WW3D/max2w3d/aabtreebuilder.cpp

## Purpose
Builds Axis-Aligned Bounding Box (AABB) trees for 3D meshes, used for spatial partitioning and culling in the W3D engine.

## Responsibilities
- Constructs hierarchical AABB trees from polygon meshes
- Computes bounding volumes for tree nodes
- Exports trees to W3D chunk format for runtime use
- Implements recursive tree building with plane splitting
- Manages memory for mesh data and tree nodes

## Key Types
- **AABTreeBuilderClass**: Main builder class managing tree construction
- **CullNodeStruct**: Internal node structure for the tree
- **SplitChoiceStruct**: Stores plane splitting evaluation results
- **SplitArraysStruct**: Holds partitioned polygon arrays
- **Vector3/Vector3i**: 3D point/vertex types

## Key Functions
### Build_AABTree
- Purpose: Main entry point to build AABB tree from mesh data
- Calls: Reset, Build_Tree, Compute_Bounding_Box, Assign_Index

### Build_Tree
- Purpose: Recursively builds the tree by partitioning polygons
- Calls: Select_Splitting_Plane, Split_Polys, Compute_Bounding_Box

### Select_Splitting_Plane
- Purpose: Finds optimal axis-aligned splitting plane for polygons
- Calls: Compute_Plane_Score, Which_Side

### Export
- Purpose: Serializes the tree to W3D chunk format
- Calls: Build_W3D_AABTree_Recursive

### Compute_Bounding_Box
- Purpose: Calculates min/max bounds for tree nodes
- Calls: Update_Min_Max

## Globals
- **COINCIDENCE_EPSILON (float)**: Tolerance value for floating-point comparisons

## Dependencies
- **aabtreebuilder.h**: Header with class definitions
- **chunkio.h**: W3D chunk I/O utilities
- **w3d_file.h**: W3D file format definitions
- **stdlib.h**, **string.h**, **assert.h**: Standard C libraries
