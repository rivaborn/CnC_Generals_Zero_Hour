# GeneralsMD/Code/Libraries/Source/WWVegas/WW3D2/dynamesh.cpp

## Purpose
Implements dynamic mesh rendering for the SAGE engine, supporting runtime geometry modification and rendering.

## Responsibilities
- Manages dynamic mesh geometry (vertices, polygons, materials)
- Handles vertex/index buffer updates for DirectX 8
- Supports multi-texture, multi-material rendering
- Provides screen-space mesh utilities
- Implements vertex stripping/fanning for polygon construction

## Key Types
- **DynamicMeshModel (Class)**: Core dynamic mesh geometry container
- **DynamicMeshClass (Class)**: High-level dynamic mesh interface
- **DynamicScreenMeshClass (Class)**: Screen-space dynamic mesh variant
- **MaterialRemapperClass (Class)**: Material remapping utility

## Key Functions
### DynamicMeshModel::Render
- Purpose: Renders dynamic mesh with current geometry and materials
- Calls: DX8Wrapper::Set_Vertex_Buffer, DX8Wrapper::Draw_Triangles, SortingRendererClass::Insert_Triangles

### DynamicMeshClass::End_Vertex
- Purpose: Finalizes current vertex and creates polygons when enough vertices are accumulated
- Calls: Model->Set_Material, Model->Set_Texture, Model->Set_Counts

### DynamicMeshClass::Set_Texture
- Purpose: Sets texture for current polygon batch
- Calls: Peek_Material_Info()->Get_Texture, Model->Initialize_Texture_Array

## Globals
- None

## Dependencies
- dx8vertexbuffer.h, dx8indexbuffer.h, dx8wrapper.h
- sortingrenderer.h, rinfo.h, camera.h, dx8fvf.h
- DirectX 8 types (D3DTS_WORLD)
- WW3D engine utilities (WWASSERT, NEW_REF)
