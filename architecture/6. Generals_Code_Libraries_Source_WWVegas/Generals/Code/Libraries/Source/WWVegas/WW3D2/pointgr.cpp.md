# Generals/Code/Libraries/Source/WWVegas/WW3D2/pointgr.cpp

## Purpose
Manages point-based rendering (particles, sprites) in the SAGE engine, handling vertex buffers, transformations, and rendering modes.

## Responsibilities
- Manages point group rendering (triangles/quads)
- Handles vertex transformations and buffering
- Supports billboarding, texturing, and shading
- Implements volume particle rendering for depth effects
- Maintains static rendering resources (index buffers, tables)

## Key Types
- `PointGroupClass` (Class): Main point group manager
- `GroundMultiplierX/Y` (Vector3): Ground-alignment vectors
- `VertexLoc/Diffuse/UV` (VectorClass): Temporary vertex data buffers
- `Tris/Quads` (DX8IndexBufferClass): Static index buffers
- `SortingTris/SortingQuads` (SortingIndexBufferClass): Sorting-aware index buffers

## Key Functions
### `PointGroupClass::RenderVolumeParticle`
- Purpose: Renders particles with depth attenuation for volumetric effects
- Calls: `Render`, `DX8Wrapper::Get/Set_Transform`, `Update_Arrays`, `DX8Wrapper::Set_Material/Shader/Texture`, `SortingRendererClass::Insert_Triangles`, `DX8Wrapper::Draw_Triangles`

### `PointGroupClass::Update_Arrays`
- Purpose: Updates vertex data arrays for rendering
- Calls: `VectorProcessorClass::CopyIndexed`, `Vector3::Subtract`, `Matrix4` operations

### `PointGroupClass::_Shutdown`
- Purpose: Cleans up static resources
- Calls: `REF_PTR_RELEASE` for buffers/materials

## Globals
- `GroundMultiplierX/Y` (Vector3): Ground-alignment vectors
- `VertexLoc/Diffuse/UV` (VectorClass): Temporary vertex data buffers
- `Tris/Quads` (DX8IndexBufferClass): Static index buffers
- `SortingTris/SortingQuads` (SortingIndexBufferClass): Sorting-aware index buffers
- `PointMaterial` (VertexMaterialClass): Shared material for points

## Dependencies
- `pointgr.h`, `vertmaterial.h`, `ww3d.h`, `aabox.h`, `statistics.h`, `simplevec.h`, `texture.h`, `vector.h`, `vp.h`, `matrix4.h`, `dx8wrapper.h`, `dx8vertexbuffer.h`, `dx8indexbuffer.h`, `rinfo.h`, `camera.h`, `dx8fvf.h`, `D3DXMath.h`, `sortingrenderer.h`
