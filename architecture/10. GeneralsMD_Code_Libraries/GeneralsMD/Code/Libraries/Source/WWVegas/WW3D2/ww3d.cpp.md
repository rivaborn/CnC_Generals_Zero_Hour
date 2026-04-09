# GeneralsMD/Code/Libraries/Source/WWVegas/WW3D2/ww3d.cpp

## Purpose
Core 3D rendering engine initialization, device management, and rendering control for the SAGE engine.

## Responsibilities
- Initialize and shutdown the 3D subsystem
- Manage render devices and resolutions
- Control rendering state (texturing, sorting, etc.)
- Handle movie capture and screenshots
- Manage debug resources and materials

## Key Types
- `WW3D` (Class): Main 3D engine interface
- `ShaderClass` (Class): Shader configuration
- `VertexMaterialClass` (Class): Material properties
- `StaticSortListClass` (Class): Sorting list for render objects
- `PrelitModeEnum` (Enum): Lighting mode options
- `MeshDrawModeEnum` (Enum): Mesh rendering modes

## Key Functions
### `Init`
- Purpose: Initialize the WW3D library
- Calls: `DX8Wrapper::Init`, `Allocate_Debug_Resources`, `DazzleRenderObjClass::Init_From_INI`

### `Shutdown`
- Purpose: Shutdown the WW3D library
- Calls: `DX8Wrapper::Shutdown`, `Release_Debug_Resources`, `AnimatedSoundMgrClass::Shutdown`

### `Set_Render_Device`
- Purpose: Set the current render device and resolution
- Calls: `DX8Wrapper::Set_Render_Device`

### `Begin_Render`
- Purpose: Start rendering a new frame
- Calls: `DX8Wrapper::Begin_Render`

### `Render`
- Purpose: Render a 3D scene or object
- Calls: `DX8Wrapper::Render`, `TheDX8MeshRenderer.Render`

### `End_Render`
- Purpose: Complete rendering for the current frame
- Calls: `DX8Wrapper::End_Render`

### `Update_Movie_Capture`
- Purpose: Capture the current frame for movie recording
- Calls: `DX8Wrapper::_Get_DX8_Front_Buffer`

### `Set_Texture_Reduction`
- Purpose: Adjust texture reduction settings
- Calls: `_Invalidate_Textures`

## Globals
- `DAZZLE_INI_FILENAME` (const char*): Dazzle configuration file name
- `_Hwnd` (HWND): Window handle for rendering
- `_TextureReduction` (int): Texture reduction factor
- `_TextureMinDim` (int): Minimum texture dimension
- `_LargeTextureExtraReductionEnabled` (bool): Flag for extra large texture reduction

## Dependencies
- Key includes: `ww3d.h`, `dx8wrapper.h`, `shader.h`, `vertexmaterial.h`, `textureloader.h`, `dazzle.h`
- External symbols: `DX8Wrapper`, `TheDX8MeshRenderer`, `WW3DAssetManager`, `DX8TextureManagerClass`
