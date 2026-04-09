# Generals/Code/Libraries/Source/WWVegas/WW3D2/shattersystem.cpp

## Purpose
Implements a mesh shattering system using BSP trees to clip and fragment 3D models for visual effects.

## Responsibilities
- Defines data structures for vertices, polygons, and BSP nodes
- Implements polygon clipping against BSP trees
- Manages mesh fragmentation and dynamic mesh creation
- Handles material properties during shattering

## Key Types
- **MeshMtlParamsClass (Class)**: Stores material parameters for mesh shattering
- **VertexClass (Class)**: Temporary vertex representation during clipping
- **PolygonClass (Class)**: Temporary polygon representation during clipping
- **BSPClass (Class)**: Node in BSP clipping tree
- **ShatterSystem (Class)**: Main system class for mesh shattering

## Key Functions
### ShatterSystem::Shatter
- Purpose: Shatters a mesh into fragments using BSP clipping
- Calls: Clip_Polygon, Process_Clip_Pools, Get_Bounding_Sphere, Transform, etc.

### BSPClass::Clip_Polygon
- Purpose: Clips a polygon against the BSP node's plane
- Calls: PolygonClass::Split, BSPClass::Clip_Polygon (recursive)

### Process_Clip_Pools
- Purpose: Converts clipped polygons into dynamic meshes
- Calls: DynamicMeshClass constructor, Begin_Tri_Fan, Location_Inline, etc.

## Globals
- **ShatterPatterns (SimpleDynVecClass<BSPClass*>)**: Array of BSP trees for clipping
- **ClipPools (PolygonClass[])**: Arrays of polygons for each leaf
- **MeshFragments (SimpleDynVecClass<DynamicMeshClass*>)**: Resultant clipped meshes
- **TmpVertPositions (SimpleVecClass<Vector3>)**: Workspace for vertex positions
- **TmpVertNormals (SimpleVecClass<Vector3>)**: Workspace for vertex normals

## Dependencies
- mesh.h, meshmdl.h, dynamesh.h, htree.h, plane.h, simplevec.h
- assetmgr.h, vp.h, meshmatdesc.h, wwstring.h
- DX8Wrapper for color conversion
