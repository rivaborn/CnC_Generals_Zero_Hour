# GeneralsMD/Code/Libraries/Source/WWVegas/WW3D2/aabtreebuilder.h

## Purpose
Header for `AABTreeBuilderClass`, which constructs Axis-Aligned Bounding (AAB) trees for mesh geometry.

## Responsibilities
- Builds AAB trees from polygon and vertex data
- Manages intermediate tree structures during construction
- Exports the final tree to a chunk save format
- Provides node and polygon count utilities

## Key Types
- **AABTreeBuilderClass (Class)**: Main builder class for AAB trees
- **CullNodeStruct (Struct)**: Intermediate node structure used during tree construction
- **SplitChoiceStruct (Struct)**: Encapsulates partitioning plane evaluation results
- **SplitArraysStruct (Struct)**: Holds split polygon arrays
- **OverlapType (Enum)**: Flags for polygon-plane overlap testing

## Key Functions
### Build_AABTree
- Purpose: Builds an AAB tree from polygon and vertex data
- Calls: `Reset`, `Build_Tree`, `Export`

### Build_Tree
- Purpose: Recursively builds the intermediate tree structure
- Calls: `Select_Splitting_Plane`, `Split_Polys`, `Compute_Bounding_Box`, `Assign_Index`

### Select_Splitting_Plane
- Purpose: Chooses the optimal splitting plane for a node
- Calls: `Compute_Plane_Score`

### Compute_Plane_Score
- Purpose: Evaluates a plane's suitability as a splitter
- Calls: `Which_Side`, `Update_Min_Max`

### Build_W3D_AABTree_Recursive
- Purpose: Converts the intermediate tree to the final W3D format
- Calls: None (leaf function)

## Globals
- **MIN_POLYS_PER_NODE (Enum)**: Minimum polygons per node (4)
- **SMALL_VERTEX (Enum)**: Small vertex constant (-100000)
- **BIG_VERTEX (Enum)**: Large vertex constant (100000)

## Dependencies
- `vector3.h`, `vector3i.h`, `aaplane.h`, `bittype.h`, `meshgeometry.h`
- `AABTreeClass`, `ChunkSaveClass`, `W3dMeshAABTreeNode` (forward declarations)
