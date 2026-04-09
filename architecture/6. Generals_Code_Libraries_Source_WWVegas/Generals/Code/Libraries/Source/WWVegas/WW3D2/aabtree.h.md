# Generals/Code/Libraries/Source/WWVegas/WW3D2/aabtree.h

## Purpose
Defines the AABTreeClass for hierarchical culling and collision detection in 3D meshes.

## Responsibilities
- Manages axis-aligned bounding box tree structure
- Performs ray and box collision tests
- Generates active polygon tables (APT) for culling
- Handles mesh geometry references and tree updates

## Key Types
- **AABTreeClass (Class)**: Main tree structure for collision detection
- **CullNodeStruct (Struct)**: Tree node containing bounding box and child/polygon references
- **OBBoxAPTContextStruct (Struct)**: Context for oriented box APT generation
- **OBBoxRayAPTContextStruct (Struct)**: Context for oriented box + ray APT generation

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

## Globals
- **AABTREE_LEAF_FLAG (const)**: Bit flag for leaf node identification

## Dependencies
- `MeshClass`, `CameraClass`, `RayCollisionTestClass`, etc. (forward declarations)
- `Vector3`, `OBBoxClass`, `SimpleDynVecClass`
- `ChunkLoadClass` for serialization
- `AABTreeBuilderClass` for tree construction
