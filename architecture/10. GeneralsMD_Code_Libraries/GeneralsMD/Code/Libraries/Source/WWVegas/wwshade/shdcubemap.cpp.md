# GeneralsMD/Code/Libraries/Source/WWVegas/wwshade/shdcubemap.cpp

## Purpose
Manages cube map shader definitions and rendering for the SAGE engine, handling texture loading and material properties.

## Responsibilities
- Defines cube map shader class with ambient/diffuse/specular colors
- Handles save/load persistence for shader parameters
- Sets up Direct3D states for cube map rendering
- Manages vertex stream formatting for cube map geometry

## Key Types
- ShdCubeMapDefClass (Class): Cube map shader definition with texture and color parameters
- Shd6CubeMapClass (Class): Runtime shader implementation for DirectX 6
- (anonymous enum) (Enum): Chunk IDs for save/load operations
- CHUNKID_VARIABLES (Enum): Main chunk ID for shader variables
- VARID_TEXTURE_NAME (Enum): Texture name variable ID
- VARID_AMBIENT_COLOR (Enum): Ambient color variable ID
- VARID_DIFFUSE_COLOR (Enum): Diffuse color variable ID
- VARID_SPECULAR_COLOR (Enum): Specular color variable ID

## Key Functions
### ShdCubeMapDefClass::Save
- Purpose: Serializes shader parameters to chunk format
- Calls: ShdDefClass::Save, WRITE_MICRO_CHUNK_WWSTRING, WRITE_MICRO_CHUNK

### ShdCubeMapDefClass::Load
- Purpose: Deserializes shader parameters from chunk format
- Calls: ShdDefClass::Load, READ_MICRO_CHUNK_WWSTRING, READ_MICRO_CHUNK

### Shd6CubeMapClass::Apply_Shared
- Purpose: Configures shared Direct3D states for cube map rendering
- Calls: DX8Wrapper::Set_DX8_Texture_Stage_State, DX8Wrapper::Set_Vertex_Shader, DX8Wrapper::Set_DX8_Render_State, DX8Wrapper::Set_DX8_Material

### Shd6CubeMapClass::Apply_Instance
- Purpose: Sets per-instance texture for cube map rendering
- Calls: DX8Wrapper::Set_Texture

### Shd6CubeMapClass::Copy_Vertex_Stream
- Purpose: Formats vertex data for cube map rendering
- Calls: None

## Globals
- View_Projection_Matrix (Matrix4x4): Static matrix for view/projection transformations

## Dependencies
- Direct3D 8 headers (d3dx8math.h, dx8fvf.h, dx8wrapper.h)
- WW3D asset management (assetmgr.h)
- Shader system headers (shdclassids.h, shddeffactory.h, shdinterface.h, shdhwshader.h)
- Persistence system (
