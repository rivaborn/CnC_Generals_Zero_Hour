# Generals/Code/Libraries/Source/WWVegas/WWMath/aabtreecull.h

## Purpose
Defines an Axis-Aligned Bounding Box (AABB) tree culling system for spatial partitioning and efficient object collection.

## Responsibilities
- Manages AABB tree construction and partitioning
- Handles object insertion, removal, and culling
- Provides statistics and iteration over the tree
- Supports serialization of tree structure

## Key Types
- **AABTreeCullSystemClass (Class)**: Main culling system using AABB trees
- **AABTreeNodeClass (Class)**: Node structure for the AABB tree
- **AABTreeIterator (Class)**: Iterator for traversing the tree
- **TypedAABTreeCullSystemClass (Class)**: Templated type-safe wrapper
- **AABTreeLinkClass (Class)**: Link structure for object-tree associations
- **StatsStruct (Struct)**: Statistics tracking for the culling system
- **SplitChoiceStruct (Struct)**: Data for tree splitting decisions

## Key Functions
### Re_Partition
- Purpose: Rebuilds the tree structure
- Calls: Partition, Re_Index_Nodes

### Collect_Objects
- Purpose: Collects objects intersecting a primitive
- Calls: Collect_Objects_Recursive (various overloads)

### Update_Bounding_Boxes
- Purpose: Updates all bounding boxes in the tree
- Calls: Update_Bounding_Boxes_Recursive

## Globals
- None

## Dependencies
- `cullsys.h`, `aaplane.h`, `wwmath.h`, `mempool.h`, `simplevec.h`
- `CullSystemClass`, `CullableClass`, `CullLinkClass`, `AABoxClass`, `Vector3`, `OBBoxClass`, `FrustumClass`, `SphereClass`
