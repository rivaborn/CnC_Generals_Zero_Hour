# GeneralsMD/Code/Libraries/Source/WWVegas/WW3D2/aabtree.h

## Purpose
Defines the AABTreeClass for hierarchical culling and collision detection in 3D meshes.

## Responsibilities
- Manages axis-aligned bounding box tree structure
- Performs collision tests (ray, AABox, OBBox)
- Generates active polygon tables (APT) for culling
- Supports mesh scaling and bounding box updates

## Key Types
- **AABTreeClass (Class)**: Main tree structure for mesh culling/collision
- **CullNodeStruct (Struct)**: Tree node containing bounding box and child/polygon references
- **OBBoxAPTContextStruct (Struct)**: Context for OBBox APT generation
- **OBBoxRayAPTContextStruct (Struct)**: Context for OBBox+ray APT generation
- **BoxRayAPTContextStruct (Class)**: Context for box-ray APT generation

## Key Functions
### `Cast_Ray`
- Purpose: Test ray collision against mesh
- Calls: `Cast_Ray_Recursive`

### `Cast_AABox`
- Purpose: Test axis-aligned box collision
- Calls: `Cast_AABox_Recursive`

### `Generate_APT`
- Purpose: Generate active polygon table for culling
- Calls: `Generate_OBBox_APT_Recursive`

### `Update_Bounding_Boxes`
- Purpose: Recalculate node bounding boxes
- Calls: `Update_Bounding_Boxes_Recursive`

## Globals
- `AABTREE_LEAF_FLAG (const)`: Bit flag marking leaf nodes

## Dependencies
- `MeshClass`, `CameraClass`, `RayCollisionTestClass`, etc. (forward declarations)
- `Vector3`, `OBBoxClass`, `AABTreeBuilderClass` (includes)
- `RefCountClass`, `W3DMPO` (inheritance)
