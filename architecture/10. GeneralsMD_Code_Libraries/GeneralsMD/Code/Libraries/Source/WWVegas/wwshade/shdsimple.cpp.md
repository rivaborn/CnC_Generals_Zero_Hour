# GeneralsMD/Code/Libraries/Source/WWVegas/wwshade/shdsimple.cpp

## Purpose
Implements a simple shader class for the SAGE engine, handling texture and material rendering with ambient/diffuse lighting.

## Responsibilities
- Defines shader parameters (texture, ambient/diffuse colors)
- Implements save/load functionality for shader definitions
- Manages Direct3D material and texture states
- Provides vertex stream copying for rendering

## Key Types
- ShdSimpleDefClass (Class): Shader definition with texture and color parameters
- Shd6SimpleClass (Class): Runtime shader implementation for DirectX 6
- (anonymous enum) (Enum): Chunk IDs for save/load
  - CHUNKID_VARIABLES: Container for shader variables
  - VARID_TEXTURE_NAME: Texture filename variable
  - VARID_AMBIENT_COLOR: Ambient color variable
  - VARID_DIFFUSE_COLOR: Diffuse color variable

## Key Functions
### ShdSimpleDefClass::Save
- Purpose: Serializes shader definition to chunk stream
- Calls: ShdDefClass::Save, WRITE_MICRO_CHUNK_WWSTRING, WRITE_MICRO_CHUNK

### ShdSimpleDefClass::Load
- Purpose: Deserializes shader definition from chunk stream
- Calls: ShdDefClass::Load, READ_MICRO_CHUNK_WWSTRING, READ_MICRO_CHUNK

### Shd6SimpleClass::Apply_Shared
- Purpose: Sets up shared Direct3D states for shader rendering
- Calls: DX8Wrapper::Set_DX8_Texture_Stage_State, DX8Wrapper::Set_Vertex_Shader, DX8Wrapper::Set_DX8_Render_State

### Shd6SimpleClass::Apply_Instance
- Purpose: Applies per-instance Direct3D material and texture
- Calls: DX8Wrapper::Set_DX8_Material, DX8Wrapper::Set_Texture

### Shd6SimpleClass::Copy_Vertex_Stream
- Purpose: Copies vertex data into shader-specific format
- Calls: None (direct memory operations)

## Globals
- Shd6SimpleClass::View_Projection_Matrix (Matrix4x4): Shared view-projection matrix

## Dependencies
- Direct3D 8 headers (d3dx8math.h)
- Engine-specific headers (dx8fvf.h, dx8wrapper.h, assetmgr.h)
- Shader system headers (shdsimple.h, shdclassids.h, shddeffactory.h, shdinterface.h, shdhwshader.h)
- Persistence headers (persistfactory.h, wwhack.h)
- WW3DAssetManager for texture loading
