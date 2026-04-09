# GeneralsMD/Code/Libraries/Source/WWVegas/WW3D2/meshmdl.cpp

## Purpose
Implements the MeshModelClass, handling 3D mesh geometry, materials, and rendering for the SAGE engine.

## Responsibilities
- Manages mesh geometry (vertices, polygons, normals)
- Handles material descriptions and texture replacement
- Supports n-patch rendering and gap filling for smooth surfaces
- Provides shadow rendering capabilities
- Maintains temporary buffers for vertex transformations

## Key Types
- **TriangleSide (Class)**: Represents a triangle edge with ordered vertices for hashing
- **SideIndexInfo (Class)**: Stores vertex indices and polygon index for edge tracking
- **MeshModelClass**: Core class for 3D mesh models
- **GapFillerClass**: Handles gap filling for n-patch rendering

## Key Functions
### MeshModelClass::Shadow_Render
- Purpose: Renders mesh shadows using a black-and-white renderer
- Calls: get_deformed_screenspace_vertices, rinfo.BWRenderer methods

### MeshModelClass::Init_For_NPatch_Rendering
- Purpose: Prepares mesh for n-patch rendering by detecting hard edges
- Calls: LocationHash/DuplicateLocationHash/SideHash operations, GapFiller methods

### GapFillerClass::Add_Polygon
- Purpose: Adds gap-filling polygons for n-patch rendering
- Calls: mmc->Get_Vertex_Array, mmc->Get_Polygon_Array

## Globals
- **_TempVertexBuffer (DynamicVectorClass<Vector3>)**: Temporary storage for deformed vertices
- **_TempNormalBuffer (DynamicVectorClass<Vector3>)**: Temporary storage for vertex normals
- **_TempTransformedVertexBuffer (DynamicVectorClass<Vector4>)**: Temporary storage for transformed vertices
- **_TempClipFlagBuffer (DynamicVectorClass<unsigned long>)**: Temporary storage for clipping flags
- **LocationHash (HashTemplateClass<Vector3, unsigned>)**: Tracks unique vertex locations
- **DuplicateLocationHash (HashTemplateClass<Vector3, unsigned>)**: Tracks duplicate vertex locations
- **SideHash (HashTemplateClass<TriangleSide,SideIndexInfo>)**: Tracks triangle edges for gap detection

## Dependencies
- meshmdl.h, matinfo.h, aabtree.h, htree.h, vp.h, visrasterizer.h
- dx8polygonrenderer.h, bwrender.h, camera.h, dx8renderer.h, hashtemplate.h
- External symbols: W3DNEW, W3DNEWARRAY, REF_PTR_SET/RELEASE, TheDX8MeshRenderer
