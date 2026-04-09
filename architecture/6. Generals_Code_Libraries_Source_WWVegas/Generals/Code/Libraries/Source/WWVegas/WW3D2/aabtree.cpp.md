# Generals/Code/Libraries/Source/WWVegas/WW3D2/aabtree.cpp

## Purpose
Implements an Axis-Aligned Bounding Box (AABB) tree for spatial partitioning and collision detection in 3D meshes.

## Responsibilities
- Manages tree construction from builder objects
- Performs collision tests (ray, box, oriented box)
- Generates active polygon tables for culling
- Supports serialization via W3D file format
- Updates bounding volumes after mesh modifications

## Key Types
- `AABTreeClass`: Main tree class handling construction and queries
- `CullNodeStruct`: Node structure storing min/max bounds and child/polygon references
- `OBBoxAPTContextStruct`: Context for oriented box active polygon table generation

## Key Functions
### `Build_Tree_Recursive`
- Purpose: Recursively constructs the tree from builder nodes
- Calls: None (internal recursion)

### `Generate_OBBox_APT_Recursive`
- Purpose: Generates active polygon table for oriented box culling
- Calls: `CollisionMath::Intersection_Test`

### `Cast_Ray_Recursive`
- Purpose: Casts a ray through the tree for collision detection
- Calls: `Cast_Ray_To_Polys`, `CollisionMath::Collide`

### `Update_Bounding_Boxes_Recursive`
- Purpose: Recomputes node bounds after mesh modifications
- Calls: `Update_Min_Max`

### `Load_W3D`
- Purpose: Deserializes tree from W3D file format
- Calls: `Read_Poly_Indices`, `Read_Nodes`

## Globals
None

## Dependencies
- `aabtree.h`, `aabtreebuilder.h`, `tri.h`, `meshgeometry.h`
- `camera.h`, `coltest.h`, `inttest.h`, `colmathinlines.h`
- `w3d_file.h`, `chunkio.h`
- `CollisionMath` namespace for intersection tests
