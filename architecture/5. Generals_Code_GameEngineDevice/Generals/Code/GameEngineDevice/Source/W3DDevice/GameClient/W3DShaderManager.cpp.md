# Generals/Code/GameEngineDevice/Source/W3DDevice/GameClient/W3DShaderManager.cpp

## Purpose
Manages shader and filter systems for the W3D rendering engine, handling hardware feature detection and shader selection.

## Responsibilities
- Manages shader/filter initialization and selection based on hardware capabilities
- Provides render-to-texture functionality for post-processing effects
- Implements specific shader types (terrain, shroud, cloud, road)
- Handles hardware feature detection (chipset, CPU, memory)
- Manages shader state and rendering passes

## Key Types
- W3DShaderInterface (Class): Base interface for custom shaders
- ShroudTextureShader (Class): Shader for fog-of-war effects
- MaskTextureShader (Class): Shader for texture masking
- TerrainShader2Stage (Class): Two-pass terrain shader
- TerrainShader8Stage (Class): Eight-pass terrain shader
- TerrainShaderPixelShader (Class): Pixel shader for terrain
- CloudTextureShader (Class): Shader for cloud rendering
- RoadShaderPixelShader (Class): Pixel shader for roads
- RoadShader2Stage (Class): Two-pass road shader

## Key Functions
### filterSetup
- Purpose: Sets up view filters before rendering
- Calls: W3DFilters[filter]->setup(mode)

### testMinimumRequirements
- Purpose: Tests system meets minimum hardware requirements
- Calls: getChipset(), CPUDetectClass methods, RunBenchmark

### add
- Purpose: Helper function for CPU benchmarking
- Calls: None

## Globals
- W3DFilters (W3DFilterInterface*): Array of filter implementations
- W3DShaders (W3DShaderInterface*): Array of shader implementations
- W3DShadersPassCount (Int*): Pass counts for each shader
- screenBWFilter (ScreenBWFilter): Black & white filter instance
- screenCrossFadeFilter (ScreenCrossFadeFilter): Cross-fade filter instance
- screenMotionBlurFilter (ScreenMotionBlurFilter): Motion blur filter instance
- shroudTextureShader (ShroudTextureShader): Shroud shader instance
- maskTextureShader (MaskTextureShader): Mask shader instance
- terrainShader2Stage (TerrainShader2Stage): 2-stage terrain shader
- terrainShader8Stage (TerrainShader8Stage): 8-stage terrain shader
- terrainShaderPixelShader (TerrainShaderPixelShader): Pixel shader terrain
- cloudTextureShader (CloudTextureShader): Cloud shader instance
- roadShaderPixelShader (RoadShaderPixelShader): Pixel shader for roads
- roadShader2Stage (RoadShader2Stage): 2-stage road shader
- MasterShaderList (W3DShaderInterface*): List of all shader implementations
- MasterFilterList (W3DFilterInterface*): List of all filter implementations

## Dependencies
- dx8wrapper.h, assetmgr.h, BaseType.h, File.h, FileSystem.h
- W3DShaderManager.h, W3DShroud.h, HeightMap.h, W3DCustomScene.h
- view.h, CommandXlat.h, display.h, Water.h, GameLogic.h
- GlobalData.h, GameLOD.h, d3dx8tex.h, dx8caps.h
- Benchmark.h, CPUDetectClass
