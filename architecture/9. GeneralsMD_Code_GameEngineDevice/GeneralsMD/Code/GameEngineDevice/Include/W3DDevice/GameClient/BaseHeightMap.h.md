# GeneralsMD/Code/GameEngineDevice/Include/W3DDevice/GameClient/BaseHeightMap.h

## Purpose
Header defining the `BaseHeightMapRenderObjClass`, a custom W3D render object for terrain rendering, lighting, and collision tests.

## Responsibilities
- Manages terrain rendering (heightmap, textures, lighting)
- Handles scorch marks, trees, props, and terrain bibs
- Processes shroud, roads, and bridges
- Performs ray casting and line-of-sight checks
- Updates terrain LOD and visibility

## Key Types
- `BaseHeightMapRenderObjClass` (Class): Core terrain render object with lighting, scorch, and geometry handling.
- `TScorch` (Struct): Stores scorch mark location, radius, and type.
- `shoreLineTileInfo` (Struct): Holds shoreline tile vertex and texture data.
- `shoreLineTileSortInfo` (Struct): Optimizes shoreline tile sorting for rendering.
- `TBounds` (Struct): Defines 2D bounding box (min/max X/Y).
- `HeightSampleType` (Typedef): Unsigned byte for heightmap data.

## Key Functions
### `initHeightData`
- Purpose: Allocates resources for rendering the heightmap.
- Calls: Not inferable (virtual, implementation in derived class).

### `updateScorches`
- Purpose: Updates scorch vertex/index buffers for rendering.
- Calls: Not inferable (implementation in derived class).

### `addScorch`
- Purpose: Adds a scorch mark to the terrain.
- Calls: Not inferable (implementation in derived class).

### `Cast_Ray`
- Purpose: Performs ray collision testing against the terrain.
- Calls: Not inferable (implementation in derived class).

### `getHeightMapHeight`
- Purpose: Returns height and normal at a given point.
- Calls: Not inferable (implementation in derived class).

## Globals
- `TheTerrainRenderObject` (BaseHeightMapRenderObjClass*): Global pointer to the terrain render object.

## Dependencies
- `rendobj.h`, `w3d_file.h`, `dx8vertexbuffer.h`, `dx8indexbuffer.h`, `dx8wrapper.h`, `shader.h`, `vertmaterial.h`
- `WorldHeightMap.h`, `Lib/BaseType.h`, `common/GameType.h`
- `DX8_CleanupHook`, `Snapshot`, `RenderObjClass`, `TextureClass`, `ShaderClass`, `VertexMaterialClass`
