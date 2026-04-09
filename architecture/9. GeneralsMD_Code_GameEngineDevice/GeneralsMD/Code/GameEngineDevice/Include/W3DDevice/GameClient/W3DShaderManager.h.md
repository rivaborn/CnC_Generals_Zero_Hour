# GeneralsMD/Code/GameEngineDevice/Include/W3DDevice/GameClient/W3DShaderManager.h

## Purpose
Manages complex rendering settings and custom shaders for the W3D2 engine, handling device-specific optimizations and hardware feature queries.

## Responsibilities
- Manages shader selection based on hardware capabilities
- Provides filter effects (motion blur, black & white, cross-fade)
- Handles render-to-texture operations
- Exposes hardware capability queries
- Manages texture stages for shaders

## Key Types
- **W3DShaderManager (Class)**: Core shader management system
- **ShaderTypes (Enum)**: Shader type identifiers (terrain, roads, shroud, etc.)
- **W3DFilterInterface (Class)**: Base interface for screen filters
- **ScreenMotionBlurFilter (Class)**: Motion blur effect implementation
- **ScreenBWFilter (Class)**: Black & white filter implementation
- **ScreenCrossFadeFilter (Class)**: Cross-fade transition effect

## Key Functions
### `init()`
- Purpose: Determines optimal shaders for current device
- Calls: Not inferable

### `setShader(ShaderTypes shader, Int pass)`
- Purpose: Enables specific shader pass
- Calls: Not inferable

### `filterPreRender(FilterTypes filter, Bool &skipRender, CustomScenePassModes &scenePassMode)`
- Purpose: Sets up filter at start of render
- Calls: Not inferable

### `startRenderToTexture()`
- Purpose: Sets render target to texture
- Calls: Not inferable

## Globals
- **m_Textures[8] (TextureClass*)**: Textures assigned to shader stages
- **m_currentChipset (ChipsetType)**: Last detected video card chipset
- **m_currentVendor (GraphicsVenderID)**: Last detected card vendor
- **m_driverVersion (__int64)**: Driver version of last chipset
- **m_renderingToTexture (Bool)**: Flag for render-to-texture state

## Dependencies
- `WW3D2/Texture.h`
- Forward reference to `TextureClass`
- External enums: `FilterTypes`, `CustomScenePassModes`, `StaticGameLODLevel`, `ChipsetType`, `CpuType`, `GraphicsVenderID`
- Direct3D 8 interfaces (`IDirect3DTexture8`, `IDirect3DSurface8`)
