# GeneralsMD/Code/Libraries/Source/WWVegas/WWMath/aabtreecull.h

## Purpose
Defines an Axis-Aligned Bounding Box (AABB) tree culling system for spatial partitioning and efficient object collection.

## Responsibilities
- Manages AABB tree structure for spatial culling
- Provides object insertion/removal and collection methods
- Supports tree re-partitioning and serialization
- Tracks statistics for performance analysis
- Implements typed tree variant for type safety

## Key Types
- **AABTreeCullSystemClass (Class)**: Main culling system using AABB trees
- **AABTreeNodeClass (Class)**: Node structure for the AABB tree
- **AABTreeIterator (Class)**: Tree traversal iterator
- **TypedAABTreeCullSystemClass (Class)**: Typed wrapper for AABB trees
- **AABTreeLinkClass (Class)**: Link structure for object-tree associations
- **StatsStruct (Struct)**: Statistics tracking structure
- **SplitChoiceStruct (Struct)**: Splitting plane evaluation data

## Key Functions
### Re_Partition
- Purpose: Rebuilds the tree structure based on current objects
- Calls: Partition, Re_Index_Nodes

### Collect_Objects
- Purpose: Collects objects intersecting with various primitives
- Calls: Collect_Objects_Recursive variants

### Update_Bounding_Boxes
- Purpose: Updates all bounding boxes in the tree
- Calls: Update_Bounding_Boxes_Recursive

### Partition
- Purpose: Splits node into front/back children based on objects
- Calls: Select_Splitting_Plane, Split_Objects

## Globals
- None

## Dependencies
- cullsys.h, aaplane.h, wwmath.h, mempool.h, simplevec.h
- CullSystemClass, CullableClass, AABoxClass, Vector3, OBBoxClass, FrustumClass
- AutoPoolClass, SimpleDynVecClass, AAPlaneClass, MinMaxAABoxClass
