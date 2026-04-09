# GeneralsMD/Code/Libraries/Source/WWVegas/wwshade/shdhwshader.cpp

## Purpose
Handles Direct3D hardware shader creation, management, and lighting setup for vertex and pixel shaders.

## Responsibilities
- Preprocess and assemble shader files
- Create and destroy vertex/pixel shaders (hardware/software fallback)
- Set up lighting constants for shaders
- Execute shell commands for shader preprocessing

## Key Types
- **ShdHWShader (Class)**: Base class for shader handling
- **ShdHWVertexShader (Class)**: Manages vertex shaders with lighting support
- **ShdHWPixelShader (Class)**: Manages pixel shaders

## Key Functions
### `Shell_Run`
- Purpose: Execute hidden shell command for shader preprocessing
- Calls: `CreateProcess`, `WaitForSingleObject`, `CloseHandle`

### `Preprocess_And_Assemble_Shader_From_File`
- Purpose: Preprocess and assemble shader from file
- Calls: `Shell_Run`, `D3DXAssembleShaderFromFile`

### `ShdHWVertexShader::Create` (file version)
- Purpose: Create vertex shader from file with hardware/software fallback
- Calls: `Preprocess_And_Assemble_Shader_From_File`, `DX8Wrapper::_Get_D3D_Device8()->CreateVertexShader`

### `ShdHWVertexShader::Light`
- Purpose: Apply lighting constants to vertex shader
- Calls: `DX8Wrapper::Set_Vertex_Shader_Constant`, `DX8Wrapper::Get_Render_State`

## Globals
- **ShdHWVertexShader::Using_Hardware (bool)**: Tracks hardware shader usage status

## Dependencies
- `shdhwshader.h`, `dx8wrapper.h`, `rinfo.h`, `shdhw_constants.h`
- Direct3D 8 interfaces (`LPD3DXBUFFER`, `D3DXAssembleShader`)
- Windows API (`CreateProcess`, `STARTUPINFO`, etc.)
- `Vector4`, `RenderInfoClass`, `LightEnvironmentClass`
