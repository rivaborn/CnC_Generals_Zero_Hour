# GeneralsMD/Code/GameEngineDevice/Source/W3DDevice/GameClient/Water/W3DWater.cpp

## Purpose
Handles rendering of water surfaces, including reflections, waves, and ripples in the SAGE engine.

## Responsibilities
- Manages water mesh rendering with dynamic vertex buffers
- Handles skybox and reflection rendering
- Implements water shaders and texture management
- Processes water tracks and wakes
- Manages time-of-day water settings

## Key Types
- **MaterMeshVertexFormat (Class)**: Vertex format for water mesh rendering
- **WaterRenderObjClass (Class)**: Main water rendering system class
- **WaterSettings (Struct)**: Contains water texture and color settings per time of day

## Key Functions
### `doSkyBoxSet`
- Purpose: Enables/disables skybox rendering
- Calls: `TheWritableGlobalData->m_drawSkyBox` assignment

### `wobble`
- Purpose: Applies wobble effect to water vertices
- Calls: Not inferable from snippet

### `setupJbaWaterShader`
- Purpose: Configures shader states for water rendering
- Calls: `DX8Wrapper::Set_Shader`, `DX8Wrapper::Set_Material`, texture state functions

## Globals
- **zFillAlphaShader (ShaderClass)**: Shader for alpha blending
- **blendStagesShader (ShaderClass)**: Shader for detail blending
- **TheWaterRenderObj (WaterRenderObjClass*)**: Global water rendering instance
- **wireframeForDebug (Bool)**: Debug wireframe rendering flag

## Dependencies
- Key includes: `W3DWater.h`, `heightmap.h`, `W3DShroud.h`, `texture.h`, `assetmgr.h`
- External symbols: `DX8Wrapper`, `TheGlobalData`, `TheTerrainRenderObject`, `W3DShaderManager`
