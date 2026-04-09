# GeneralsMD/Code/GameEngineDevice/Include/W3DDevice/GameClient/W3DTerrainTracks.h

## Purpose
Manages rendering of vehicle tracks on terrain in the SAGE engine.

## Responsibilities
- Handles creation, updating, and rendering of track marks
- Manages track object pooling and resource lifecycle
- Implements fading and capping of track segments
- Provides system-level control for track rendering

## Key Types
- **TerrainTracksRenderObjClass (Class)**: Individual track render object for a vehicle
- **edgeInfo (Struct)**: Stores per-edge data (position, UVs, alpha, timing)
- **TerrainTracksRenderObjClassSystem (Class)**: Manages all track objects and rendering

## Key Functions
### `init`
- Purpose: Allocates W3D resources and sets track dimensions
- Calls: Not inferable

### `addEdgeToTrack`
- Purpose: Adds a new segment to the track
- Calls: Not inferable

### `flush`
- Purpose: Renders all tracks requested for this frame
- Calls: Not inferable

### `update`
- Purpose: Updates edge states (fading, removal)
- Calls: Not inferable

## Globals
- **TheTerrainTracksRenderObjClassSystem (TerrainTracksRenderObjClassSystem*)**: Singleton instance of the track system

## Dependencies
- `rendobj.h`, `w3d_file.h`, `dx8vertexbuffer.h`, `dx8indexbuffer.h`, `shader.h`, `vertmaterial.h`
- `W3DMPO`, `RenderObjClass`, `TextureClass`, `SceneClass`, `Drawable`
