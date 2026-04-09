# GeneralsMD/Code/Libraries/Source/WWVegas/wwshade/shdlegacyw3d.cpp

## Purpose
Handles legacy W3D shader definitions and rendering for the SAGE engine, including save/load functionality and DirectX 8 shader management.

## Responsibilities
- Manages legacy W3D shader definitions and their properties
- Handles serialization/deserialization of shader data
- Implements DirectX 8 shader rendering interface
- Provides vertex stream manipulation for rendering

## Key Types
- ShdLegacyW3DDefClass (Class): Legacy W3D shader definition class
- Shd6LegacyW3DClass (Class): DirectX 6 legacy shader implementation
- (anonymous enum) (Enum): Chunk IDs for save/load operations
- VARID_* (Enums): Variable IDs for shader properties

## Key Functions
### ShdLegacyW3DDefClass::Save
- Purpose: Saves shader definition to chunk stream
- Calls: ShdDefClass::Save, Save_Variables, WRITE_WWSTRING_CHUNK

### ShdLegacyW3DDefClass::Load
- Purpose: Loads shader definition from chunk stream
- Calls: ShdDefClass::Load, Load_Variables

### Shd6LegacyW3DClass::Apply_Instance
- Purpose: Applies per-instance shader states for rendering
- Calls: DX8Wrapper::Set_Shader, DX8Wrapper::Set_Vertex_Shader, DX8Wrapper::Set_Material, DX8Wrapper::Set_Texture

### Shd6LegacyW3DClass::Copy_Vertex_Stream
- Purpose: Copies vertex data to destination buffer with proper formatting
- Calls: FVFInfoClass methods

## Globals
- None

## Dependencies
- DirectX 8 headers (d3dx8math.h, dx8fvf.h, dx8wrapper.h)
- WWVegas framework (assetmgr.h, editable.h, chunkio.h, etc.)
- Shader system headers (shdlegacyw3d.h, shdclassids.h, etc.)
