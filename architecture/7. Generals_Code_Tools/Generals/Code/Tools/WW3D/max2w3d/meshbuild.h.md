# Generals/Code/Tools/WW3D/max2w3d/meshbuild.h

## Purpose
Header file defining the MeshBuilderClass for processing 3D meshes, including vertex/face management, mesh optimization, and bounding volume computation.

## Responsibilities
- Define mesh processing pipeline (vertex/face handling, optimization)
- Manage mesh statistics and material passes
- Provide bounding volume calculations
- Support skinning and texture coordinate management

## Key Types
- **WorldInfoClass (Class)**: Abstract base for external world information (normals, smoothing)
- **MeshBuilderClass (Class)**: Main mesh processing class
- **VertClass (Class)**: Vertex data structure with position, normals, texture coords, etc.
- **FaceClass (Class)**: Triangle face structure with vertex references and material data
- **MeshStatsStruct (Struct)**: Statistics about mesh processing (textures, strips, etc.)
- **WingedEdgeStruct (Struct)**: Helper for strip optimization
- **WingedEdgePolyStruct (Struct)**: Polygon edge reference

## Key Functions
### MeshBuilderClass::Build_Mesh
- Purpose: Process input faces into optimized mesh
- Calls: Optimize_Mesh, Strip_Optimize_Mesh, Remove_Degenerate_Faces, Compute_Mesh_Stats

### MeshBuilderClass::Optimize_Mesh
- Purpose: Optimize vertex and face data
- Calls: Compute_Face_Normals, Compute_Vertex_Normals

### MeshBuilderClass::Strip_Optimize_Mesh
- Purpose: Convert triangles into strips
- Calls: WingedEdge-related functions

## Globals
- None

## Dependencies
- "vector2.h", "vector3.h", "bittype.h"
- Uses Vector2, Vector3, uint32 types
- Assert for debugging checks
