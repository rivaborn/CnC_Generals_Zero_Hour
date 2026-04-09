# Generals/Code/GameEngineDevice/Include/W3DDevice/GameClient/HeightMap.h

## Purpose
Header for the terrain rendering system in the SAGE engine, defining the `HeightMapRenderObjClass` and related types.

## Responsibilities
- Declares terrain rendering object and associated buffers
- Defines scorch marks, roads, bridges, and terrain features
- Manages heightmap data structures and rendering parameters
- Provides terrain collision and visibility testing

## Key Types
- `HeightMapRenderObjClass` (Class): Main terrain render object handling drawing, lighting, and collision
- `TBounds` (Struct): Bounding box coordinates
- `TScorch` (Struct): Scorch mark data (location, radius, type)
- `shoreLineTileInfo` (Struct): Shore line tile blending data
- `MAX_SCORCH_VERTEX`/`MAX_SCORCH_INDEX`/`MAX_SCORCH_MARKS` (Enums): Scorch mark limits

## Key Functions
### `initHeightData`
- Purpose: Initialize terrain rendering resources
- Calls: Not inferable

### `Render`
- Purpose: Render the terrain and associated elements
- Calls: Not inferable

### `Cast_Ray`
- Purpose: Perform ray collision testing against terrain
- Calls: Not inferable

### `updateScorches`
- Purpose: Update scorch mark vertex/index buffers
- Calls: Not inferable

## Globals
- `TheTerrainRenderObject` (HeightMapRenderObjClass*): Global terrain render object instance

## Dependencies
- `rendobj.h`, `w3d_file.h`, `dx8vertexbuffer.h`, `shader.h`, `WorldHeightMap.h`
- `DX8VertexBufferClass`, `DX8IndexBufferClass`, `TextureClass`, `W3DDynamicLight`
