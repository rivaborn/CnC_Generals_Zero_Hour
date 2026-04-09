# Generals/Code/Libraries/Source/WWVegas/WW3D2/mesh.h

## Purpose
Defines the `MeshClass` and related structures for 3D mesh rendering in the SAGE engine.

## Responsibilities
- Declares the `MeshClass` which handles mesh rendering, collision detection, and bounding volumes.
- Defines utility functions for mesh manipulation (e.g., `Set_MeshModel_Flag`).
- Provides forward declarations for mesh-related classes and structs.

## Key Types
- **MeshClass (Class)**: Main mesh rendering class, inherits from `W3DMPO` and `RenderObjClass`.
- **MeshBuilderClass (Class)**: Used for mesh construction (forward declared).
- **MeshModelClass (Class)**: Represents mesh model data (forward declared).
- **MaterialInfoClass (Class)**: Contains material information (forward declared).
- **LightEnvironmentClass (Class)**: Manages lighting for meshes.
- **VertexFormatXYZNDUV2 (Struct)**: Vertex format with position, normal, and UV coordinates.

## Key Functions
### `Set_MeshModel_Flag`
- Purpose: Recursively sets flags on mesh models within a render object.
- Calls: Not inferable (implementation not shown).

## Globals
- **Legacy_Meshes_Fogged (bool)**: Static flag indicating whether legacy meshes use fog.

## Dependencies
- Key includes: `always.h`, `rendobj.h`, `bittype.h`, `w3derr.h`, `LightEnvironment.h`.
- External symbols: `W3DMPO`, `RenderObjClass`, `DynamicVectorClass`, `StringClass`, `Vector3`, `Vector2`.
