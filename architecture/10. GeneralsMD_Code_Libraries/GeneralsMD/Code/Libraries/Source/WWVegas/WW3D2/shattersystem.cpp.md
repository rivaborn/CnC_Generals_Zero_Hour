# GeneralsMD/Code/Libraries/Source/WWVegas/WW3D2/shattersystem.cpp

## Purpose
Implements a mesh shattering system for breaking 3D models into fragments using BSP trees.

## Responsibilities
- Manages BSP-based mesh clipping and fragmentation
- Handles vertex/polygon splitting and material preservation
- Creates dynamic mesh fragments from shattered pieces
- Mainages temporary vertex buffers and clipping pools

## Key Types
- **MeshMtlParamsClass (Class)**: Stores material parameters for mesh passes
- **VertexClass (Class)**: Temporary vertex representation during clipping
- **PolygonClass (Class)**: Temporary polygon representation during clipping
- **BSPClass (Class)**: Node in BSP clipping tree for mesh shattering
- **ShatterSystem (Class)**: Main system class for mesh shattering operations

## Key Functions
### ShatterSystem::Shatter
- Purpose: Shatters a mesh into fragments using BSP clipping
- Calls: Clip_Polygon, Process_Clip_Pools, _get_temp_vertex_position_array, _get_temp_vertex_normal_array

### BSPClass::Clip_Polygon
- Purpose: Recursively clips a polygon against BSP planes
- Calls: PolygonClass::Split, Clip_Polygon (recursive)

### PolygonClass::Split
- Purpose: Splits a polygon against a clipping plane
- Calls: VertexClass::Intersect_Plane, VertexClass::Which_Side

## Globals
- **ShatterPatterns (SimpleDynVecClass<BSPClass*>)**: Array of BSP trees for clipping
- **ClipPools (PolygonClass[])**: Arrays of polygons for each leaf
- **MeshFragments (SimpleDynVecClass<DynamicMeshClass*>)**: Resultant clipped meshes
- **TmpVertPositions (SimpleVecClass<Vector3>)**: Workspace for vertex positions
- **TmpVertNormals (SimpleVecClass<Vector3>)**: Workspace for vertex normals

## Dependencies
- mesh.h, meshmdl.h, dynamesh.h, htree.h, plane.h, simplevec.h
- WWString.h, vp.h, meshmatdesc.h
- DX8Wrapper (for color conversion)
- Vector3, Vector4, Matrix3D classes
