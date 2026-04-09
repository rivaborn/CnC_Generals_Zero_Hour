# Generals/Code/Libraries/Source/WWVegas/WWMath/aabtreecull.cpp

## Purpose
Implements an Axis-Aligned Bounding Box (AABB) tree culling system for spatial partitioning and efficient object queries.

## Responsibilities
- Manages AABB tree construction and partitioning
- Handles object insertion, removal, and culling queries
- Supports serialization of tree structure
- Provides tree traversal utilities

## Key Types
- `IOAABNodeStruct` (Struct): Stores AABB node data (center, extent, attributes)
- `AABTreeCullSystemClass` (Class): Main culling system managing the tree
- `AABTreeNodeClass` (Class): Individual nodes in the AABB tree
- `AABTreeLinkClass` (Class): Links objects to tree nodes
- `AABTreeIterator` (Class): Tree traversal iterator

## Key Functions
### `Add_Object_Internal`
- Purpose: Adds an object to the tree at a specific node
- Calls: `Add_Object_Recursive`, `Add_Object`

### `Update_Culling`
- Purpose: Re-inserts an object into the tree after its bounds change
- Calls: `Add_Object_Recursive`, `Remove_Object`

### `Partition`
- Purpose: Recursively partitions objects/boxes into front/back subtrees
- Calls: `Select_Splitting_Plane`, `Split_Boxes`

### `Select_Splitting_Plane`
- Purpose: Finds optimal splitting plane for partitioning
- Calls: `Compute_Score`

## Globals
- `AABTREE_CURRENT_VERSION` (uint32): File format version constant

## Dependencies
- `aabtreecull.h`, `chunkio.h`, `iostruct.h`, `sphere.h`, `colmath.h`, `colmathinlines.h`
- `CollisionMath`, `AABoxClass`, `AAPlaneClass`, `SimpleDynVecClass`
