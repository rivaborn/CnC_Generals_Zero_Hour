# Generals/Code/Libraries/Source/WWVegas/WW3D2/dynamesh.cpp

## Purpose
Implements dynamic mesh rendering functionality for the WW3D2 engine, including vertex/index buffer management and material handling.

## Responsibilities
- Manages dynamic mesh geometry (vertices, polygons)
- Handles material/texture assignment per vertex/polygon
- Renders dynamic meshes using DirectX 8
- Supports multi-texture and multi-material rendering
- Provides screen-space mesh utilities

## Key Types
- **DynamicMeshModel (Class)**: Core dynamic mesh geometry container
- **DynamicMeshClass (Class)**: High-level dynamic mesh interface
- **DynamicScreenMeshClass (Class)**: Screen-space dynamic mesh variant
- **MaterialInfoClass (Ref)**: Material information container
- **MeshMatDescClass (Ref)**: Mesh material descriptor

## Key Functions
### DynamicMeshModel::Render
- Purpose: Renders the dynamic mesh with current geometry and materials
- Calls: DX8Wrapper::Set_Vertex_Buffer, DX8Wrapper::Draw_Triangles, SortingRendererClass::Insert_Triangles

### DynamicMeshClass::End_Vertex
- Purpose: Finalizes current vertex and creates polygons when enough vertices are accumulated
- Calls: Model->Set_Material, Model->Set_Texture, Model->Set_Counts

### DynamicMeshClass::Set_Texture
- Purpose: Assigns a texture to the mesh (either single or per-polygon)
- Calls: Peek_Material_Info()->Get_Texture, Model->Set_Single_Texture

## Globals
- None

## Dependencies
- dx8vertexbuffer.h, dx8indexbuffer.h, dx8wrapper.h
- sortingrenderer.h, rinfo.h, camera.h, dx8fvf.h
- WW3D global state functions (Is_Sorting_Enabled, Are_Static_Sort_Lists_Enabled)
