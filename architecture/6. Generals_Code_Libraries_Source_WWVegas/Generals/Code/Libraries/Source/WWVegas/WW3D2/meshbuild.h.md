# Generals/Code/Libraries/Source/WWVegas/WW3D2/meshbuild.h

## Purpose
Header file defining the `MeshBuilderClass` for processing 3D meshes, including vertex/face management, mesh optimization, and bounding volume computation.

## Responsibilities
- Define mesh processing pipeline (vertex/face splitting, sorting, strip optimization)
- Manage vertex and face data structures
- Compute mesh statistics and bounding volumes
- Support multi-pass rendering with texture/shader channels

## Key Types
- **WorldInfoClass (Class)**: Abstract base for providing external world data (normals, smoothing flags)
- **MeshBuilderClass (Class)**: Main mesh processing class
- **VertClass (Class)**: Vertex data structure (position, normals, texture coords, colors)
- **FaceClass (Class)**: Triangle face data structure (vertices, materials, attributes)
- **MeshStatsStruct (Struct)**: Statistics about processed mesh (texture usage, strip counts)
- **WingedEdgeStruct (Struct)**: Internal edge data for strip optimization
- **WingedEdgePolyStruct (Struct)**: Internal polygon edge references

## Key Functions
### MeshBuilderClass::Build_Mesh
- Purpose: Process input faces into optimized mesh
- Calls: Optimize_Mesh, Strip_Optimize_Mesh, Remove_Degenerate_Faces, Compute_Mesh_Stats

### MeshBuilderClass::Optimize_Mesh
- Purpose: Optimize vertex and face data
- Calls: Compute_Face_Normals, Compute_Vertex_Normals

### MeshBuilderClass::Strip_Optimize_Mesh
- Purpose: Convert triangles into strips for rendering efficiency
- Calls: WingedEdge-related operations

## Globals
None

## Dependencies
- `vector2.h`, `vector3.h`, `bittype.h` (math types)
- `always.h` (assertions)
- Standard C++ containers (vector, etc.)
