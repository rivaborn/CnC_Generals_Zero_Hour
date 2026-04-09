# Generals/Code/Libraries/Source/WWVegas/WW3D2/meshgeometry.cpp

## Purpose
Handles mesh geometry data structures, loading W3D files, and collision detection for 3D models.

## Responsibilities
- Manages mesh geometry (vertices, polygons, normals)
- Loads W3D file format chunks
- Performs collision detection (ray, box, sphere)
- Computes bounding volumes and plane equations
- Handles mesh scaling and transformation

## Key Types
- **MeshGeometryClass (Class)**: Core mesh geometry container
- **Vector3 (Struct)**: 3D vector representation
- **Vector4 (Struct)**: 4D vector (used for plane equations)
- **ShareBufferClass (Template)**: Reference-counted buffer management

## Key Functions
### Load_W3D
- Purpose: Loads mesh data from W3D file format
- Calls: read_chunks, read_vertices, read_vertex_normals, read_triangles, read_user_text, read_vertex_influences, read_vertex_shade_indices, read_aabtree

### Cast_Ray
- Purpose: Computes ray intersection with mesh
- Calls: cast_ray_brute_force

### Cast_AABox
- Purpose: Tests axis-aligned box intersection
- Calls: cast_aabox_identity, cast_aabox_z90, cast_aabox_z180, cast_aabox_z270, cast_aabox_brute_force

### Compute_Plane_Equations
- Purpose: Recalculates plane equations for all polygons
- Calls: Compute_Plane

### Generate_Culling_Tree
- Purpose: Creates spatial partitioning structure for collision
- Calls: AABTreeClass methods

## Globals
- **_PlaneEQArray (SimpleVecClass<Vector4>)**: Optimization buffer for plane equations
- **_VNormArray (SimpleVecClass<Vector3>)**: Optimization buffer for vertex normals

## Dependencies
- Key includes: meshgeometry.h, aabtree.h, chunkio.h, aabox.h, obbox.h, sphere.h, plane.h, wwdebug.h, wwmemlog.h, w3d_file.h, vp.h
- External symbols: W3D_CHUNK_*, W3D_MAKE_VERSION, W3D_MESH_FLAG_*, WW3DErrorType, ChunkLoadClass, AABTreeClass, ShareBufferClass
