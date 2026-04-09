# Generals/Code/GameEngineDevice/Source/W3DDevice/GameClient/TerrainTex.cpp

## Purpose
Implements custom terrain texturing for the game's 3D engine, handling terrain tiles, alpha edges, clouds, and scorch effects.

## Responsibilities
- Manages terrain texture rendering with tile-based approach
- Handles special cases for low-end hardware (256x256 textures)
- Implements alpha blending for terrain edges
- Provides animated cloud textures with sliding effect
- Manages scorch mark textures

## Key Types
- **TerrainTextureClass (Class)**: Base terrain texture handler with tile borders
- **AlphaEdgeTextureClass (Class)**: Handles alpha blending for terrain edges
- **CloudMapTerrainTextureClass (Class)**: Animated cloud texture with sliding effect
- **ScorchTextureClass (Class)**: Manages scorch mark textures

## Key Functions
### TerrainTextureClass::update
- Purpose: Updates texture with tile data and applies 4-pixel borders
- Calls: D3DTexture->GetSurfaceLevel, surface_level->LockRect, D3DXFilterTexture

### AlphaEdgeTextureClass::update
- Purpose: Updates alpha edge texture with edge tile data
- Calls: D3DTexture->GetSurfaceLevel, surface_level->LockRect, D3DXFilterTexture

### CloudMapTerrainTextureClass::Apply
- Purpose: Applies cloud texture with sliding animation effect
- Calls: TextureClass::Apply, DX8Wrapper::Set_DX8_Texture_Stage_State, DX8Wrapper::_Get_DX8_Transform

### ScorchTextureClass::Apply
- Purpose: Applies scorch texture with proper filtering settings
- Calls: TextureClass::Apply, DX8Wrapper::Set_DX8_Texture_Stage_State

## Globals
- **TheWritableGlobalData (GlobalDataClass)**: Accesses texture reduction settings
- **TheGlobalData (GlobalDataClass)**: Accesses texture filtering preferences

## Dependencies
- W3DDevice/GameClient/TerrainTex.h
- W3DDevice/GameClient/WorldHeightMap.h
- W3DDevice/GameClient/TileData.h
- common/GlobalData.h
- WW3D2/dx8wrapper.h
- d3dx8tex.h
