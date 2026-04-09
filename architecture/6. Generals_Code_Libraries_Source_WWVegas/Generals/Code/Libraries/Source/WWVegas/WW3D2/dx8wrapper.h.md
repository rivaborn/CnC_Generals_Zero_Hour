# Generals/Code/Libraries/Source/WWVegas/WW3D2/dx8wrapper.h

## Purpose
Header file defining the DX8Wrapper class, a wrapper for Direct3D 8 rendering API, managing state changes and resource handling.

## Responsibilities
- Encapsulates Direct3D 8 device management
- Tracks render state changes (matrices, textures, materials, etc.)
- Provides utility functions for color conversion and resource creation
- Manages deferred render state application

## Key Types
- **DX8Wrapper (Class)**: Main wrapper class for Direct3D 8 functionality
- **RenderStateStruct (Struct)**: Stores current render state (textures, lights, matrices, etc.)
- **ChangedStates (Enum)**: Bit flags for tracking state changes
- **BUFFER_TYPE_DX8 (Enum)**: Vertex/index buffer type flags

## Key Functions
### Set_Render_State
- Purpose: Applies a complete render state from a RenderStateStruct
- Calls: REF_PTR_SET, Add_Engine_Ref

### Apply_Render_State_Changes
- Purpose: Applies deferred render state changes to the device
- Calls: DX8CALL, SetTransform, SetMaterial, SetTexture, SetLight

### Convert_Color
- Purpose: Converts Vector3/Vector4 colors to 32-bit integer format
- Calls: None (inline assembly)

## Globals
- **MAX_TEXTURE_STAGES (const unsigned)**: Maximum number of texture stages (2)
- **number_of_DX8_calls (unsigned)**: Counter for DX8 API calls
- **_DX8SingleThreaded (bool)**: Flag for single-threaded DX8 access

## Dependencies
- Key includes: "d3d8.h", "matrix4.h", "shader.h", "texture.h"
- External symbols: D3D device/interface functions, WW3DFormat, ThreadClass
