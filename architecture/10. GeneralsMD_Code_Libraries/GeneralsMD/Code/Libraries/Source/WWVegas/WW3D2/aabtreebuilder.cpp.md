# GeneralsMD/Code/Libraries/Source/WWVegas/WW3D2/aabtreebuilder.cpp

## Purpose
Implements an Axis-Aligned Bounding Box (AABB) tree builder for 3D mesh culling optimization in the W3D engine.

## Responsibilities
- Constructs hierarchical AABB trees from mesh data (vertices and polygons)
- Computes optimal splitting planes for tree nodes
- Exports trees to W3D chunk format for runtime use
- Manages memory allocation/deallocation for tree structures

## Key Types
- `AABTreeBuilderClass` (Class): Main builder class managing tree construction
- `CullNodeStruct` (Struct): Internal tree node representation
- `SplitChoiceStruct` (Struct): Stores splitting plane evaluation results
- `AAPlaneClass` (Class): Axis-aligned plane representation

## Key Functions
### `Build_AABTree`
- Purpose: Main entry point to build AABB tree from mesh data
- Calls: `Reset`, `Build_Tree`, `Compute_Bounding_Box`, `Assign_Index`

### `Build_Tree`
- Purpose: Recursively builds the tree structure by partitioning polygons
- Calls: `Select_Splitting_Plane`, `Split_Polys`, `Compute_Bounding_Box`

### `Select_Splitting_Plane`
- Purpose: Evaluates potential splitting planes to find optimal partition
- Calls: `Compute_Plane_Score`, `Which_Side`

### `Export`
- Purpose: Serializes the tree to W3D chunk format for file storage
- Calls: `Node_Count`, `Poly_Count`, `Build_W3D_AABTree_Recursive`

## Globals
- `COINCIDENCE_EPSILON` (float): Tolerance value for floating-point comparisons

## Dependencies
- `aabtreebuilder.h`, `chunkio.h`, `w3d_file.h`
- Uses `Vector3`, `TriIndex`, `W3DNEWARRAY` macros
- Relies on `WWASSERT` for debugging assertions
