# GeneralsMD/Code/Libraries/Source/WWVegas/WW3D2/dx8wrapper.cpp

## Purpose
Wrapper for Direct3D 8 API, managing device initialization, rendering states, and resource handling for the SAGE engine.

## Responsibilities
- Direct3D 8 device creation and management
- Render state and texture stage state handling
- Error logging and debugging utilities
- Device capability querying and enumeration
- Shader and lighting system integration

## Key Types
- **DX8Wrapper (Class)**: Main wrapper for Direct3D 8 functionality
- **Direct3DCreate8Type (typedef)**: Function pointer type for Direct3DCreate8
- **RenderStateStruct (struct)**: Container for render state values

## Key Functions
### Log_DX8_ErrorCode
- Purpose: Logs Direct3D error codes and asserts failure
- Calls: D3DXGetErrorStringA, WWDEBUG_SAY, WWASSERT

### Non_Fatal_Log_DX8_ErrorCode
- Purpose: Logs Direct3D error codes without asserting
- Calls: D3DXGetErrorStringA, WWDEBUG_SAY

### F2DW
- Purpose: Converts float to DWORD (bitwise reinterpret)
- Calls: None

### DX8_Assert
- Purpose: Thread-safe assertion for DX8 operations
- Calls: ThreadClass::_Get_Current_Thread_ID, WWASSERT

## Globals
- **DEFAULT_RESOLUTION_WIDTH (int)**: Default screen width (640)
- **DEFAULT_RESOLUTION_HEIGHT (int)**: Default screen height (480)
- **DEFAULT_BIT_DEPTH (int)**: Default color depth (32)
- **DEFAULT_TEXTURE_BIT_DEPTH (int)**: Default texture depth (16)
- **DX8Wrapper_IsWindowed (bool)**: Windowed mode flag
- **DX8Wrapper_PreserveFPU (int)**: FPU preservation flag
- **_Hwnd (HWND)**: Main window handle
- **_DX8SingleThreaded (bool)**: Single-threaded mode flag
- **Direct3DCreate8Ptr (Direct3DCreate8Type)**: Pointer to Direct3DCreate8
- **D3D8Lib (HINSTANCE)**: Handle to D3D8.DLL

## Dependencies
- Direct3D 8 headers and D3DX8core.h
- WW3D engine components (WW3D, Camera, Matrix4, etc.)
- SAGE-specific utilities (WWString, Registry, Statistics)
- Thread management (ThreadClass)
- Shader system (SHDLib)
- Texture management (TextureLoader, DX8TexMan)
