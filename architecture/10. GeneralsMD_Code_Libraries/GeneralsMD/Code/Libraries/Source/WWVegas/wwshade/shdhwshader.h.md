# GeneralsMD/Code/Libraries/Source/WWVegas/wwshade/shdhwshader.h

## Purpose
Header file defining hardware shader classes for Direct3D 8, including vertex and pixel shaders.

## Responsibilities
- Declares base `ShdHWShader` class and derived `ShdHWVertexShader`/`ShdHWPixelShader` classes
- Provides shader creation, destruction, and management interfaces
- Handles shader preprocessing and assembly from files
- Manages hardware shader usage state

## Key Types
- **ShdHWShader (Class)**: Base class for hardware shaders, manages shader handle and utility methods
- **ShdHWVertexShader (Class)**: Vertex shader implementation with lighting support
- **ShdHWPixelShader (Class)**: Pixel shader implementation
- **RenderInfoClass (Class)**: External rendering context (not defined here)
- **Vector4 (Class)**: External 4D vector type (not defined here)

## Key Functions
### ShdHWShader::Preprocess_And_Assemble_Shader_From_File
- Purpose: Preprocesses and assembles shader code from a file
- Calls: `Shell_Run`

### ShdHWVertexShader::Create (file_name, declaration)
- Purpose: Creates a vertex shader from a file
- Calls: `Preprocess_And_Assemble_Shader_From_File`

### ShdHWVertexShader::Create (shader_code, declaration)
- Purpose: Creates a vertex shader from pre-compiled code
- Calls: `D3DXAssembleShader`

### ShdHWVertexShader::Light (rinfo, ambient, diffuse, specular)
- Purpose: Sets up lighting constants for vertex shader
- Calls: `D3DDevice->SetVertexShaderConstant`

### ShdHWPixelShader::Create (
