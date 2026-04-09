# Generals/Code/Libraries/Source/WWVegas/WW3D2/meshmdl.cpp

## Purpose
Implements the MeshModelClass for 3D mesh rendering, including skinning, material handling, and gap-filling for n-patch rendering.

## Responsibilities
- Manages mesh geometry, materials, and rendering state
- Handles vertex skinning and deformation via bone hierarchies
- Supports texture and material replacement
- Implements gap-filling for n-patch rendering to handle hard edges
- Provides shadow rendering capabilities

## Key Types
- **MeshModelClass (Class)**: Main mesh model container with geometry and material data
- **TriangleSide (Class)**: Represents a triangle edge for gap detection (sorted by vertex positions)
- **SideIndexInfo (Class)**: Stores vertex indices and polygon index for triangle edges
- **GapFillerClass (Class)**: Manages gap-filling polygons for n-patch rendering

## Key Functions
### MeshModelClass::get_deformed_vertices
- Purpose: Deforms vertices using bone transformations from an HTree
- Calls: htree->Get_Transform, Matrix3D::Transform_Vector

### MeshModelClass::Shadow_Render
- Purpose: Renders mesh shadows using a 2D bitmap renderer
- Calls: get_deformed_screenspace_vertices, rinfo.BWRenderer->Set_Vertex_Locations, rinfo.BWRenderer->Render_Triangles

### MeshModelClass::Init_For_NPatch_Rendering
- Purpose: Detects hard edges and generates gap-filling polygons
- Calls: LocationHash/DuplicateLocationHash/SideHash operations, GapFillerClass methods

### Whatever
- Purpose: Not inferable (likely a helper for polygon processing)
- Calls: Not inferable

## Globals
- **_TempVertexBuffer (DynamicVectorClass<Vector3>)**: Temporary storage for deformed vertices
- **_TempNormalBuffer (DynamicVectorClass<Vector3>)**: Temporary storage for deformed normals
- **_TempTransformedVertexBuffer (DynamicVectorClass<Vector4>)**: Temporary storage for transformed vertices
- **_TempClipFlagBuffer (DynamicVectorClass<unsigned long>)**: Temporary storage for clipping flags
- **LocationHash (HashTemplateClass<Vector3, unsigned>)**: Tracks unique vertex positions
- **DuplicateLocationHash (HashTemplateClass<Vector3, unsigned>)**: Tracks duplicate vertex positions
- **SideHash (HashTemplateClass<TriangleSide, SideIndexInfo>)**: Tracks triangle edges for gap detection

## Dependencies
- meshmdl.h, matinfo.h, aabtree.h, htree.h, vp.h, visrasterizer.h, dx8polygonrenderer.h, bwrender.h, camera.h, dx8renderer.h, hashtemplate.h
- DynamicVectorClass, Vector3/4, Matrix3D/4, HashTemplateClass, W3DNEW/W3DNEWARRAY macros
- TheDX8MeshRenderer (global renderer instance)
