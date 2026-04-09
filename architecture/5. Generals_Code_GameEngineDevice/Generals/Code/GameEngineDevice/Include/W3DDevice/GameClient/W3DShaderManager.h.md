# Generals/Code/GameEngineDevice/Include/W3DDevice/GameClient/W3DShaderManager.h

## Purpose
Manages complex rendering settings and custom shaders for the W3D2 engine, handling device-specific optimizations and hardware feature queries.

## Responsibilities
- Manages custom shaders for terrain, roads, clouds, and special effects
- Handles screen filters (motion blur, black & white, cross-fade)
- Provides hardware capability detection (GPU/CPU performance)
- Manages render-to-texture operations for special effects
- Maintains texture stages for shader access

## Key Types
- **W3DShaderManager (Class)**: Core shader management system
- **ShaderTypes (Enum)**: Shader type identifiers (terrain, roads, clouds, etc.)
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
- Purpose: Sets up screen filters before rendering
- Calls: Not inferable

### `startRenderToTexture()`
- Purpose: Redirects rendering to a texture
- Calls: Not inferable

## Globals
- **m_Textures[8] (TextureClass*)**: Textures assigned to shader stages
- **m_currentChipset (ChipsetType)**: Last detected video card chipset
- **m_renderingToTexture (Bool)**: Flag for render-to-texture state
- **m_renderTexture (IDirect3DTexture8*)**: Texture used for render targets

## Dependencies
- `WW3D2/Texture.h` (TextureClass)
- External enums: FilterTypes, CustomScenePassModes, StaticGameLODLevel, ChipsetType, CpuType
- Direct3D 8 interfaces (IDirect3DSurface8, IDirect3DTexture8)
