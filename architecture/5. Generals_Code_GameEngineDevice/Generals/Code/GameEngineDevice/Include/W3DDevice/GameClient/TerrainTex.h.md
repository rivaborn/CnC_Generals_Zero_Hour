# Generals/Code/GameEngineDevice/Include/W3DDevice/GameClient/TerrainTex.h

## Purpose
Defines terrain texture classes for rendering heightmaps and special effects in the SAGE engine.

## Responsibilities
- Manage terrain texture generation and updates
- Handle alpha blending for terrain edges
- Support light mapping and scorch effects
- Implement cloud map rendering with animation

## Key Types
- **WorldHeightMap (Class)**: Reference to heightmap data
- **TerrainTextureClass (Class)**: Base terrain texture using heightmap data
- **AlphaTerrainTextureClass (Class)**: Terrain texture with alpha blending
- **AlphaEdgeTextureClass (Class)**: Texture for terrain edge effects
- **LightMapTerrainTextureClass (Class)**: Lightmap texture for terrain
- **ScorchTextureClass (Class)**: Texture for scorch marks/effects
- **CloudMapTerrainTextureClass (Class)**: Animated cloud layer texture

## Key Functions
### `update(WorldHeightMap *htMap)`
- Purpose: Updates texture pixels from heightmap data
- Calls: `update256()`

### `Apply(unsigned int stage)`
- Purpose: Applies texture to a rendering stage
- Calls: Not inferable (virtual implementation in subclasses)

## Globals
- **TILE_OFFSET (const int)**: Defines tile offset value (8)

## Dependencies
- `WW3D2/Texture.h` (TextureClass inheritance)
- `WWMATH/Matrix3d.h`
- `common/AsciiString.h`
- `WorldHeightMap` (forward declaration)
