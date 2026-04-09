# GeneralsMD/Code/Libraries/Source/WWVegas/WWMath/aabtreecull.cpp

## Purpose
Implements an Axis-Aligned Bounding Box (AABB) tree culling system for spatial partitioning and efficient object queries.

## Responsibilities
- Manages AABB tree construction, partitioning, and object insertion/removal
- Supports spatial queries (point, box, frustum, sphere containment tests)
- Handles serialization/deserialization of tree structure
- Provides tree traversal utilities via iterator
- Maintains object references and tree statistics

## Key Types
- `IOAABNodeStruct` (Struct): Serialization structure for AABB tree nodes containing center, extent, and attributes
- `AABTreeCullSystemClass` (Class): Main culling system managing the tree and objects
- `AABTreeNodeClass` (Class): Individual nodes in the AABB tree
- `AABTreeLinkClass` (Class): Links objects to tree nodes
- `AABTreeIterator` (Class): Tree traversal iterator
- `SplitChoiceStruct` (Struct): Helper for partitioning decisions

## Key Functions
### `Add_Object_Internal`
- Purpose: Adds an object to the tree at a specific node or recursively finds appropriate node
- Calls: `Add_Object_Recursive`, `Add_Object`

### `Update_Culling`
- Purpose: Re-inserts an object into the tree when its bounding box changes
- Calls: `Add_Object_Recursive`, `Remove_Object`

### `Collect_Objects_Recursive`
- Purpose: Recursively collects objects intersecting with various query shapes
- Calls: Various overlap test functions from `CollisionMath`

### `Partition`
- Purpose: Partitions a node's contents using spatial splitting
- Calls: `Select_Splitting_Plane`, `Split_Boxes`

### `Select_Splitting_Plane`
- Purpose: Finds optimal splitting plane for partitioning
- Calls: `Compute_Score`, `Select_Splitting_Plane_Brute_Force`

## Globals
- `AABTREE_CURRENT_VERSION` (uint32): File format version constant
- `AABTREE_CHUNK_*` (Enum values): Chunk ID constants for serialization

## Dependencies
- `aabtreecull.h`, `chunkio.h`, `iostruct.h`, `sphere.h`, `colmath.h`, `colmathinlines.h`
- `CullableClass`, `AABoxClass`, `OBBoxClass`, `FrustumClass`, `SphereClass`, `Vector3`
- Memory allocation utilities (`new`, `delete`)
- Math utilities (`rand()`, `MIN()`, `FLT_MAX`)
