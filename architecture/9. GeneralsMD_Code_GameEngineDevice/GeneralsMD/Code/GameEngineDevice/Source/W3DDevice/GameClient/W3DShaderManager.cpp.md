# GeneralsMD/Code/GameEngineDevice/Source/W3DDevice/GameClient/W3DShaderManager.cpp

## Purpose
Manages shader and filter systems for the W3D rendering pipeline, handling hardware feature detection and shader selection.

## Responsibilities
- Manages shader/filter initialization and validation
- Handles render-to-texture operations
- Implements various shader types (terrain, shroud, cloud, etc.)
- Provides shader selection based on hardware capabilities
- Manages pixel shaders and texture stages

## Key Types
- W3DShaderInterface (Class): Base interface for custom shaders
- ScreenDefaultFilter (Class): Default screen filter implementation
- ShroudTextureShader (Class): Shader for fog-of-war shroud effects
- TerrainShader2Stage (Class): Two-stage terrain shader
- FlatTerrainShaderPixelShader (Class): Pixel shader for flat terrain
- GraphicsVenderID (Enum): Graphics vendor identification

## Key Functions
### filterSetup
- Purpose: Sets up filter rendering parameters
- Calls: DX8Wrapper state setting functions

### testMinimumRequirements
- Purpose: Tests if hardware meets minimum requirements
- Calls: DX8Wrapper capability queries

### add
- Purpose: Adds a shader/filter to the manager
- Calls: Internal shader/filter registration

## Globals
- W3DFilters (W3DFilterInterface*): Array of filter implementations
- W3DShaders (W3DShaderInterface*): Array of shader implementations
- W3DShadersPassCount (Int*): Pass counts for each shader
- m_currentShader (ShaderTypes): Currently active shader type
- m_currentFilter (FilterTypes): Currently active filter type
- m_renderingToTexture (Bool): Flag for render-to-texture operation
- m_renderTexture (IDirect3DTexture8*): Texture used for render-to-texture

## Dependencies
- dx8wrapper.h: Direct3D 8 wrapper
- W3DShaderManager.h: Shader manager interface
- DX8Caps.h: Direct3D 8 capabilities
- d3dx8tex.h: Direct3D 8 texture utilities
- Various game-specific headers (view.h, display.h, etc.)
