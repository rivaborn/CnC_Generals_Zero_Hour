# Generals/Code/GameEngineDevice/Source/W3DDevice/GameClient/Water/W3DWater.cpp

## Purpose
Handles rendering of water surfaces, including reflections, waves, and ripples in the SAGE engine.

## Responsibilities
- Manages water mesh rendering with vertex buffers and shaders
- Handles skybox and skybody rendering for water reflections
- Implements wave simulation and water surface distortion
- Manages water transparency and feathering effects
- Handles water track system for vehicle wake effects

## Key Types
- **MaterMeshVertexFormat (Class)**: Vertex format for water mesh (XYZNDUV2 or XYZDUV2)
- **WaterRenderObjClass (Class)**: Main water rendering system class
- **WaterSettings (Struct)**: Contains water texture and sky settings per time of day

## Key Functions
### `setupJbaWaterShader`
- Purpose: Sets up shader states for water rendering
- Calls: `DX8Wrapper::Set_Shader`, `DX8Wrapper::Set_Material`, `DX8Wrapper::Set_DX8_Texture_Stage_State`

### `wobble`
- Purpose: Applies wave distortion to water vertices
- Calls: Not inferable from snippet

### `doSkyBoxSet`
- Purpose: Enables/disables skybox rendering
- Calls: `TheWritableGlobalData->m_drawSkyBox` assignment

## Globals
- **zFillAlphaShader (ShaderClass)**: Shader for alpha blending
- **blendStagesShader (ShaderClass)**: Shader for detail blending
- **TheWaterRenderObj (WaterRenderObjClass*)**: Global water rendering object
- **wireframeForDebug (Bool)**: Debug flag for wireframe rendering

## Dependencies
- Key includes: `W3DWater.h`, `heightmap.h`, `W3DShroud.h`, `texture.h`, `assetmgr.h`
- External symbols: `DX8Wrapper`, `TheGlobalData`, `TheTerrainRenderObject`, `TheWaterTransparency`
- Shader manager: `W3DShaderManager`
