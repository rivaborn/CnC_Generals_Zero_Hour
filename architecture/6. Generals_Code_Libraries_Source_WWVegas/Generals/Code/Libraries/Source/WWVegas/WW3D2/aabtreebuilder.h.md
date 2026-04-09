# Generals/Code/Libraries/Source/WWVegas/WW3D2/aabtreebuilder.h

## Purpose
Header for `AABTreeBuilderClass`, which constructs Axis-Aligned Bounding (AAB) trees for 3D mesh culling optimization.

## Responsibilities
- Builds AAB trees from polygon and vertex data
- Computes optimal splitting planes for tree nodes
- Exports tree data for serialization
- Tracks node and polygon counts

## Key Types
- **AABTreeBuilderClass (Class)**: Main builder class for AAB trees
- **CullNodeStruct (Struct)**: Temporary node structure during tree construction
- **SplitChoiceStruct (Struct)**: Stores partitioning plane evaluation results
- **SplitArraysStruct (Struct)**: Holds split polygon arrays
- **OverlapType (Enum)**: Flags for polygon-plane overlap tests

## Key Functions
### Build_AABTree
- Purpose: Initiates AAB tree construction from polygon/vertex data
- Calls: `Reset`, `Build_Tree`

### Select_Splitting_Plane
- Purpose: Chooses optimal plane to split polygons at a node
- Calls: `Compute_Plane_Score`

### Compute_Plane_Score
- Purpose: Evaluates a plane's suitability for splitting
- Calls: `Split_Polys`, `Which_Side`

### Build_W3D_AABTree_Recursive
- Purpose: Recursively builds the final W3D AAB tree structure
- Calls: `Compute_Bounding_Box`, `Assign_Index`

## Globals
- **MIN_POLYS_PER_NODE (Enum)**: Minimum polygons per leaf node (4)
- **SMALL_VERTEX/BIG_VERTEX (Enum)**: Bounding box clipping values

## Dependencies
- `vector3.h`, `vector3i.h`, `aaplane.h`, `bittype.h`
- `AABTreeClass`, `ChunkSaveClass`, `W3dMeshAABTreeNode` (forward declarations)
