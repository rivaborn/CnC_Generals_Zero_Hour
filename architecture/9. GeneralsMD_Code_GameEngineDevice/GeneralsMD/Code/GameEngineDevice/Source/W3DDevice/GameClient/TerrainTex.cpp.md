# GeneralsMD/Code/GameEngineDevice/Source/W3DDevice/GameClient/TerrainTex.cpp

## Purpose
Handles terrain texture rendering and management in the SAGE engine, including tile-based texturing, alpha blending, and special effects like clouds and scorch marks.

## Responsibilities
- Manages terrain texture classes (TerrainTextureClass, AlphaEdgeTextureClass, CloudMapTerrainTextureClass, ScorchTextureClass)
- Updates texture data from height maps and tile data
- Handles texture filtering and mipmapping
- Implements special texture effects (cloud movement, alpha blending)

## Key Types
- **TerrainTextureClass (Class)**: Base terrain texture handler with tile-based rendering
- **AlphaEdgeTextureClass (Class)**: Manages alpha blending for terrain edges
- **CloudMapTerrainTextureClass (Class)**: Handles animated cloud textures over terrain
- **ScorchTextureClass (Class)**: Manages scorch mark textures

## Key Functions
### TerrainTextureClass::update
- Purpose: Updates texture data from height map tiles with 4-pixel borders
- Calls: Peek_D3D_Texture(), GetSurfaceLevel(), LockRect(), D3DXFilterTexture()

### AlphaEdgeTextureClass::update
- Purpose: Updates alpha edge texture data for terrain blending
- Calls: Peek_D3D_Texture(), LockRect(), D3DXFilterTexture()

### CloudMapTerrainTextureClass::Apply
- Purpose: Applies cloud texture with sliding animation effect
- Calls: TextureClass::Apply(), GetTickCount()

### ScorchTextureClass::Apply
- Purpose: Applies scorch texture with proper filtering settings
- Calls: TextureClass::Apply(), DX8Wrapper texture state functions

## Globals
- **TheWritableGlobalData (GlobalDataClass)**: Accesses texture reduction settings

## Dependencies
- W3DDevice/GameClient/TerrainTex.h
- W3DDevice/GameClient/WorldHeightMap.h
- W3DDevice/GameClient/TileData.h
- common/GlobalData.h
- WW3D2/dx8wrapper.h
- d3dx8tex.h
