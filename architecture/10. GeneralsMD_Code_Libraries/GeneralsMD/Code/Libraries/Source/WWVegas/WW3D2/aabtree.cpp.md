# GeneralsMD/Code/Libraries/Source/WWVegas/WW3D2/aabtree.cpp

## Purpose
Implements an Axis-Aligned Bounding Box (AABB) tree for spatial partitioning and collision detection in 3D meshes.

## Responsibilities
- Manages AABB tree construction, traversal, and updates
- Performs collision tests (ray, box, oriented box) against mesh polygons
- Generates active polygon tables for culling
- Loads/saves tree data from W3D files

## Key Types
- **AABTreeClass** (Class): Main tree structure managing nodes and polygons
- **CullNodeStruct** (Struct): Tree node containing bounding box and child/polygon references
- **OBBoxAPTContextStruct** (Struct): Context for oriented box active polygon table generation

## Key Functions
### `Build_Tree_Recursive`
- Purpose: Recursively builds the tree from a builder structure
- Calls: None (internal recursion)

### `Cast_Ray_Recursive`
- Purpose: Tests ray intersection against tree nodes
- Calls: `Cast_Ray_To_Polys`, `Cast_Semi_Infinite_Axis_Aligned_Ray_To_Polys`

### `Generate_OBBox_APT_Recursive`
- Purpose: Generates active polygon table for oriented box culling
- Calls: `CollisionMath::Intersection_Test`

### `Update_Bounding_Boxes_Recursive`
- Purpose: Recomputes node bounding boxes after mesh modification
- Calls: `Update_Min_Max`

### `Load_W3D`
- Purpose: Loads tree data from W3D file format
- Calls: `Read_Poly_Indices`, `Read_Nodes`

## Globals
- **MeshGeometryClass *Mesh** (Pointer): Associated mesh geometry

## Dependencies
- `aabtree.h`, `aabtreebuilder.h`, `wwdebug.h`, `tri.h`, `meshgeometry.h`, `coltest.h`, `inttest.h`, `colmathinlines.h`, `w3d_file.h`, `chunkio.h`
- `CollisionMath`, `Vector3`, `Vector4`, `AABoxClass`, `OBBoxClass`, `TriClass`
