# Generals/Code/Libraries/Source/WWVegas/WW3D2/ww3d.cpp

## Purpose
Core 3D rendering engine initialization, device management, and frame rendering for the SAGE engine.

## Responsibilities
- Initialize/shutdown Direct3D and related subsystems
- Manage render devices, resolutions, and display modes
- Control rendering state (texturing, sorting, debugging)
- Handle movie capture and screenshots
- Maintain global rendering settings and statistics

## Key Types
- `WW3D` (Class): Main engine interface with static methods
- `FrameGrabClass` (Pointer): Movie capture handler
- `RefRenderObjListClass` (Array): Static sort lists for rendering
- `VertexMaterialClass` (Pointer): Debug material
- `ShaderClass` (Static): Default debug shaders

## Key Functions
### `Init`
- Purpose: Initialize Direct3D, enumerate devices, and set up rendering systems
- Calls: `DX8Wrapper::Init`, `Allocate_Debug_Resources`, `DazzleRenderObjClass::Init_From_INI`

### `Shutdown`
- Purpose: Clean up all WW3D resources and release assets
- Calls: `DX8Wrapper::Shutdown`, `DX8TextureManagerClass::Shutdown`, `Release_Debug_Resources`

### `Set_Render_Device`
- Purpose: Configure the current render device and resolution
- Calls: `DX8Wrapper::Set_Render_Device`

### `Begin_Render` / `End_Render`
- Purpose: Mark start/end of frame rendering
- Calls: `TheDX8MeshRenderer.Flush`, `TheDX8TextureManager.Flush`

### `Update_Movie_Capture`
- Purpose: Capture current frame for movie recording
- Calls: `DX8Wrapper::_Get_DX8_Front_Buffer`, `Movie->Grab`

## Globals
- `DAZZLE_INI_FILENAME` (const char*): Path to Dazzle configuration file
- `_Hwnd` (HWND): Window handle for rendering
- `_TextureReduction` (int): Texture quality reduction factor
- `_TextureMinMipLevels` (int): Minimum mipmap levels for textures

## Dependencies
- Direct3D 8 wrapper (`dx8wrapper.h`)
- Texture management (`dx8texman.h`)
- Mesh rendering (`dx8renderer.h`)
- Asset management (`assetmgr.h`)
- File I/O (`file.h`, `ini.h`)
- Debug utilities (`wwdebug.h`)
- Dazzle effects (`dazzle.h`)
