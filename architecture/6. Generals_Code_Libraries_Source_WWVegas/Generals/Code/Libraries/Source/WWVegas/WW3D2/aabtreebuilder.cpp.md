# Generals/Code/Libraries/Source/WWVegas/WW3D2/aabtreebuilder.cpp

## Purpose
Builds Axis-Aligned Bounding Box (AABB) trees for 3D mesh culling optimization in the W3D engine.

## Responsibilities
- Constructs hierarchical spatial partitioning trees for mesh data
- Computes bounding volumes for tree nodes
- Exports AABB trees to W3D chunk format
- Handles polygon partitioning and tree balancing

## Key Types
- AABTreeBuilderClass (Class): Main builder class for AABB trees
- CullNodeStruct (Struct): Internal tree node structure
- SplitChoiceStruct (Struct): Stores splitting plane evaluation results
- SplitArraysStruct (Struct): Stores partitioned polygon arrays

## Key Functions
### Build_AABTree
- Purpose: Main entry point to build AABB tree from mesh data
- Calls: Reset, Build_Tree, Compute_Bounding_Box, Assign_Index

### Build_Tree
- Purpose: Recursively builds the culling tree structure
- Calls: Select_Splitting_Plane, Split_Polys, Build_Tree (recursive)

### Compute_Plane_Score
- Purpose: Evaluates suitability of a splitting plane
- Calls: Which_Side, Update_Min_Max

### Export
- Purpose: Serializes AABB tree to W3D chunk format
- Calls: Node_Count, Poly_Count, Build_W3D_AABTree_Recursive

## Globals
- COINCIDENCE_EPSILON (float): Tolerance value for floating-point comparisons

## Dependencies
- aabtreebuilder.h (header)
- chunkio.h (W3D chunk I/O)
- w3d_file.h (W3D file format)
- stdlib.h, string.h, assert.h (standard C libraries)
