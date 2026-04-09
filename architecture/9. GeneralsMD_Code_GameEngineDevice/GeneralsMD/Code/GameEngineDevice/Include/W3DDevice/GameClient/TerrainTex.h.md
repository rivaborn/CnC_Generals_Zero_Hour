# GeneralsMD/Code/GameEngineDevice/Include/W3DDevice/GameClient/TerrainTex.h

## Purpose
Defines terrain texture classes for rendering height maps and special effects in the game engine.

## Responsibilities
- Manage terrain texture rendering
- Handle alpha blending for terrain edges
- Support light mapping and scorch effects
- Implement cloud map animations

## Key Types
- **WorldHeightMap (Class)**: Reference to height map data.
- **TerrainTextureClass (Class)**: Base terrain texture with LOD support.
- **AlphaTerrainTextureClass (Class)**: Texture with alpha blending.
- **AlphaEdgeTextureClass (Class)**: Specialized alpha texture for terrain edges.
- **LightMapTerrainTextureClass (Class)**: Light map texture for terrain.
- **ScorchTextureClass (Class)**: Texture for scorch marks.
- **CloudMapTerrainTextureClass (Class)**: Animated cloud map texture.

## Key Functions
### `update()`
- Purpose: Updates texture pixels from height map data.
- Calls: Not inferable.

### `updateFlat()`
- Purpose: Updates flat terrain texture region.
- Calls: Not inferable.

### `setLOD()`
- Purpose: Sets texture detail level.
- Calls: Not inferable.

### `restore()`
- Purpose: Restores cloud map state.
- Calls: Not inferable.

## Globals
- **TILE_OFFSET (const int)**: Tile offset constant.

## Dependencies
- `TextureClass` (base class)
- `WorldHeightMap` (external reference)
- `Matrix3d` (for transformations)
- `AsciiString` (for texture names)
- `W3DMPO_GLUE` macro (for engine integration)
