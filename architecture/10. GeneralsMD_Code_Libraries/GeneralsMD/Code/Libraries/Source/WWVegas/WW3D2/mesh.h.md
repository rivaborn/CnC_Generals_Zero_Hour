# GeneralsMD/Code/Libraries/Source/WWVegas/WW3D2/mesh.h

## Purpose
Defines the `MeshClass` and related structures for 3D mesh rendering in the SAGE engine.

## Responsibilities
- Declares the `MeshClass` which handles mesh rendering, collision detection, and bounding volumes.
- Defines interfaces for mesh loading, material management, and decal support.
- Provides utility functions for mesh model flag manipulation.

## Key Types
- **MeshClass (Class)**: Main mesh rendering object, inherits from `W3DMPO` and `RenderObjClass`.
- **MeshBuilderClass (Class)**: Used for mesh construction (forward declared).
- **MaterialInfoClass (Class)**: Contains material data for meshes (forward declared).
- **MeshModelClass (Class)**: Represents the mesh model data (forward declared).
- **LightEnvironmentClass (Class)**: Handles lighting for meshes (forward declared).
- **VertexFormatXYZNDUV2 (Struct)**: Vertex format definition for mesh vertices.

## Key Functions
### `Set_MeshModel_Flag`
- Purpose: Recursively sets flags on mesh models within a render object hierarchy.
- Calls: Not inferable (implementation not shown).

## Globals
- **Legacy_Meshes_Fogged (bool)**: Static flag indicating whether legacy .w3d files use fog.

## Dependencies
- Key includes: `always.h`, `rendobj.h`, `bittype.h`, `w3derr.h`, `LightEnvironment.h`
- External symbols: `W3DMPO`, `RenderObjClass`, `RayCollisionTestClass`, `AABoxCollisionTestClass`, etc.
