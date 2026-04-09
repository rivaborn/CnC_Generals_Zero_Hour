# GeneralsMD/Code/Libraries/Source/WWVegas/WW3D2/mesh.cpp

## Purpose
Implements the MeshClass, handling 3D mesh rendering, collision detection, and asset management in the SAGE engine.

## Responsibilities
- Manages mesh geometry, materials, and rendering
- Handles collision detection (ray, box, sphere)
- Supports mesh cloning, scaling, and transformation
- Integrates with the W3D asset system
- Provides decal and skinning functionality

## Key Types
- **MeshClass**: Main mesh class handling rendering and collision
- **MeshModelClass** (external): Underlying mesh model data
- **MaterialInfoClass** (external): Material and texture management
- **RayCollisionTestClass** (external): Ray collision testing structure

## Key Functions
### MeshClass::Cast_Ray
- Purpose: Tests ray intersection with the mesh
- Calls: Model->Cast_Ray, Matrix3D transformations

### MeshClass::Cast_AABox
- Purpose: Tests axis-aligned box collision with the mesh
- Calls: Model->Cast_World_Space_AABox

### MeshClass::Cast_OBBox
- Purpose: Tests oriented bounding box collision
- Calls: Model->Cast_OBBox, Matrix3D transformations

### Set_MeshModel_Flag
- Purpose: Recursively sets flags on mesh models in a render object hierarchy
- Calls: Get_Sub_Object, Release_Ref

## Globals
- **MeshDebugIdCount** (unsigned): Debug ID counter for meshes
- **temp_apt** (SimpleDynVecClass<uint32>): Temporary allocation pool
- **_TempVertexBuffer** (DynamicVectorClass<Vector3>): Temporary vertex storage for decals

## Dependencies
- Key includes: mesh.h, w3d_file.h, assetmgr.h, w3derr.h, vertmaterial.h, shader.h, matinfo.h
- External symbols: MeshModelClass, MaterialInfoClass, RenderObjClass, Matrix3D, Vector3
- Rendering: DX8PolygonRenderer, DX8IndexBuffer, DX8Renderer
- Collision: RayCollisionTestClass, AABoxCollisionTestClass, OBBoxCollisionTestClass
