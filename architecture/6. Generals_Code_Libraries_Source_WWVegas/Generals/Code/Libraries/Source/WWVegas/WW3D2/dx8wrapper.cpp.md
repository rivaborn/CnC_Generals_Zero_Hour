# Generals/Code/Libraries/Source/WWVegas/WW3D2/dx8wrapper.cpp

## Purpose
Direct3D 8 wrapper for the SAGE engine, handling device initialization, rendering states, textures, and resource management.

## Responsibilities
- Manages Direct3D 8 device creation and state tracking
- Handles texture and render target management
- Provides utility functions for lighting, gamma control, and device validation
- Tracks rendering statistics and performance metrics
- Implements thread safety checks for Direct3D calls

## Key Types
- DX8Wrapper (Class): Main wrapper for Direct3D 8 functionality
- RenderStateStruct (Struct): Tracks current render state
- RenderDeviceDescClass (Class): Describes available render devices

## Key Functions
### Log_DX8_ErrorCode
- Purpose: Logs Direct3D error codes and asserts failure
- Calls: D3DXGetErrorStringA, WWDEBUG_SAY, WWASSERT

### Non_Fatal_Log_DX8_ErrorCode
- Purpose: Logs non-fatal Direct3D errors with file/line info
- Calls: D3DXGetErrorStringA, WWDEBUG_SAY

### F2DW
- Purpose: Converts float to DWORD (bitcast)
- Calls: None

### DX8_Assert
- Purpose: Thread safety assertion for Direct3D calls
- Calls: ThreadClass::_Get_Current_Thread_ID, WWASSERT

## Globals
- DEFAULT_RESOLUTION_WIDTH (int): Default screen width (640)
- DEFAULT_RESOLUTION_HEIGHT (int): Default screen height (480)
- DEFAULT_BIT_DEPTH (int): Default color depth (32)
- DEFAULT_TEXTURE_BIT_DEPTH (int): Default texture depth (16)
- DX8Wrapper_IsWindowed (bool): Windowed mode flag
- DX8Wrapper_PreserveFPU (int): FPU preservation flag
- _Hwnd (HWND): Main window handle
- _DX8SingleThreaded (bool): Single-threaded mode flag
- number_of_DX8_calls (unsigned): Counter for Direct3D calls
- _PresentParameters (D3DPRESENT_PARAMETERS): Device presentation settings
- _RenderDeviceNameTable (DynamicVectorClass<StringClass>): Available device names
- _RenderDeviceShortNameTable (DynamicVectorClass<StringClass>): Short device names
- _RenderDeviceDescriptionTable (DynamicVectorClass<RenderDeviceDescClass>): Device descriptions

## Dependencies
- Direct3D 8 headers (D3D8, D3DX8)
- WW3D engine components (ww3d.h, camera.h, etc.)
- SAGE utility classes (ThreadClass, WWString, etc.)
- Rendering-specific modules (dx8renderer.h, dx8texman.h)
