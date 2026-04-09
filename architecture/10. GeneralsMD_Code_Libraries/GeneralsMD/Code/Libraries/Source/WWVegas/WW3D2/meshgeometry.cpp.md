# GeneralsMD/Code/Libraries/Source/WWVegas/WW3D2/meshgeometry.cpp

## Purpose
Implements the MeshGeometryClass for loading, managing, and manipulating 3D mesh data in the SAGE engine, including collision detection and rendering support.

## Responsibilities
- Load and parse W3D mesh files
- Manage mesh geometry data (vertices, polygons, normals)
- Perform collision detection (ray, box, sphere)
- Generate spatial acceleration structures (AABTree)
- Support skinning and deformation via bone hierarchies

## Key Types
- **MeshGeometryClass**: Main class for 3D mesh geometry
- **TriIndex**: Triangle vertex index structure
- **W3dTriStruct**: W3D triangle data structure

## Key Functions
### Load_W3D
- Purpose: Load mesh data from a W3D file
- Calls: read_vertices, read_vertex_normals, read_triangles, read_user_text, read_vertex_influences, read_vertex_shade_indices, read_aabtree

### Cast_Ray
- Purpose: Compute ray intersection with the mesh
- Calls: cast_ray_brute_force

### Generate_Culling_Tree
- Purpose: Generate an AABTree for spatial partitioning
- Calls: AABTreeClass constructor

### Scale
- Purpose: Scale the mesh geometry and update bounds
- Calls: AABTreeClass::Scale, Generate_Culling_Tree

### get_deformed_vertices
- Purpose: Compute vertex positions after skinning transformation
- Calls: HTreeClass::Get_Transform, Matrix3D::Transform_Vector

## Globals
- **_PlaneEQArray** (SimpleVecClass<Vector4>): Optimization buffer for plane equations
- **_VNormArray** (SimpleVecClass<Vector3>): Optimization buffer for vertex normals

## Dependencies
- aabtree.h, chunkio.h, aabox.h, obbox.h, sphere.h, plane.h, wwdebug.h, wwmemlog.h, w3d_file.h, vp.h, htree.h, matrix4.h, rinfo.h, camera.h
