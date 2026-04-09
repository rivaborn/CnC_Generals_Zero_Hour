# GeneralsMD/Code/Libraries/Source/WWVegas/WW3D2/pointgr.cpp

## Purpose
Manages point-based rendering (particles, sprites) in the SAGE engine, handling vertex transformation, shading, and DirectX 8 rendering.

## Responsibilities
- Manages point group rendering (triangles/quads)
- Handles vertex transformation and compression
- Supports billboarding, texturing, and shading
- Implements volume particle rendering for depth effects
- Manages static index buffers for rendering

## Key Types
- **PointGroupClass** (Class): Main class for point group rendering
- **PointMaterialClass** (Static): Shared vertex material for points
- **Vector3/Vector4/Vector2** (Structs): Math types for positions/colors/UVs
- **DX8IndexBufferClass** (Class): DirectX 8 index buffer wrapper
- **SortingIndexBufferClass** (Class): Sorting-aware index buffer

## Key Functions
### PointGroupClass::RenderVolumeParticle
- Purpose: Renders particles with depth attenuation for volume effects
- Calls: Update_Arrays, DX8Wrapper::Set_Transform, DX8Wrapper::Draw_Triangles, SortingRendererClass::Insert_Triangles

### PointGroupClass::Update_Arrays
- Purpose: Updates vertex arrays for rendering
- Calls: Not inferable (truncated)

### PointGroupClass::_Shutdown
- Purpose: Cleans up static resources
- Calls: REF_PTR_RELEASE, Clear()

## Globals
- **GroundMultiplierX/Y** (Vector3): Ground plane multipliers
- **VertexLoc/Diffuse/UV** (VectorClass): Temporary vertex data
- **Tris/Quads** (DX8IndexBufferClass*): Static index buffers
- **SortingTris/SortingQuads** (SortingIndexBufferClass*): Sorting index buffers
- **PointMaterial** (VertexMaterialClass*): Shared material

## Dependencies
- DirectX 8 headers (D3DXMath, dx8wrapper)
- SAGE engine components (WW3D, VP, Matrix4)
- Rendering utilities (SortingRenderer, Statistics)
- Math libraries (Vector, SimpleVec)
