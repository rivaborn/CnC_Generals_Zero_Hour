# GeneralsMD/Code/Libraries/Source/WWVegas/WW3D2/meshbuild.h

## Purpose
Header file defining the `MeshBuilderClass` for processing 3D meshes, including vertex/face management, mesh optimization, and bounding volume computation.

## Responsibilities
- Define mesh processing pipeline (vertex/face handling, optimization)
- Provide interface for mesh statistics and world information
- Support mesh building with configurable passes and texture stages
- Manage vertex/face arrays and their attributes

## Key Types
- **WorldInfoClass (Class)**: Abstract base for world information (shared vertex normals, smoothing flags)
- **MeshBuilderClass (Class)**: Main mesh processing class (state management, optimization, bounding volumes)
- **VertClass (Class)**: Vertex data structure (position, normals, texture coords, colors, attributes)
- **FaceClass (Class)**: Face/triangle data structure (vertices, texture/shader indices, plane data)
- **MeshStatsStruct (Struct)**: Mesh statistics (texture/shader usage, strip counts, UV splits)
- **WingedEdgeStruct (Struct)**: Helper for strip optimization (edge/polygon references)
- **WingedEdgePolyStruct (Struct)**: Polygon edge references for strip optimization

## Key Functions
### `Build_Mesh`
- Purpose: Process input faces into optimized mesh (strips, vertex welding)
- Calls: `Remove_Degenerate_Faces`, `Optimize_Mesh`, `Compute_Mesh_Stats`

### `Optimize_Mesh`
- Purpose: Optimize mesh topology (vertex welding, strip generation)
- Calls: `Strip_Optimize_Mesh`, `Compute_Vertex_Normals`

### `Compute_Tangent_Basis`
- Purpose: Calculate tangent/bitangent vectors for per-pixel lighting
- Calls: Not inferable (implementation in .cpp)

### `Set_World_Info`
- Purpose: Attach world information for shared vertex normals
- Calls: None

## Globals
- **MAX_PASSES (Enum)**: Maximum render passes (4)
- **MAX_STAGES (Enum)**: Maximum texture stages per pass (8)

## Dependencies
- `vector2.h`, `vector3.h`, `bittype.h` (math types)
- `always.h` (asserts, macros)
- `WorldInfoClass` (abstract base, defined here)
