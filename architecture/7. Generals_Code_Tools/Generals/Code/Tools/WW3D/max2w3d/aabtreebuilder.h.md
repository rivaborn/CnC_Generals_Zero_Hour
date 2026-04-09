# Generals/Code/Tools/WW3D/max2w3d/aabtreebuilder.h

## Purpose
Header file for AABTreeBuilderClass, which constructs Axis-Aligned Bounding (AAB) trees for 3D mesh optimization.

## Responsibilities
- Defines data structures for AAB tree construction
- Declares methods for building and exporting AAB trees
- Manages intermediate tree nodes and splitting logic

## Key Types
- **AABTreeBuilderClass (Class)**: Main builder class for AAB trees
- **CullNodeStruct (Struct)**: Intermediate node structure during tree construction
- **SplitChoiceStruct (Struct)**: Stores partitioning plane evaluation results
- **SplitArraysStruct (Struct)**: Holds split polygon arrays
- **OverlapType (Enum)**: Defines polygon-plane overlap classification

## Key Functions
### Build_AABTree
- Purpose: Initiates AAB tree construction from polygon/vertex data
- Calls: Reset, Build_Tree

### Build_Tree
- Purpose: Recursively builds the intermediate tree structure
- Calls: Select_Splitting_Plane, Split_Polys, Compute_Bounding_Box

### Select_Splitting_Plane
- Purpose: Evaluates optimal plane for partitioning polygons
- Calls: Compute_Plane_Score

### Build_W3D_AABTree_Recursive
- Purpose: Converts intermediate tree to final W3D format
- Calls: None (leaf function)

## Globals
- **MIN_POLYS_PER_NODE (Enum)**: Minimum polygons per node (4)
- **SMALL_VERTEX/BIG_VERTEX (Enum)**: Vertex bounds constants

## Dependencies
- "vector3.h", "vector3i.h", "aaplane.h", "bittype.h"
- AAPlaneClass, AABTreeClass, ChunkSaveClass, W3dMeshAABTreeNode
