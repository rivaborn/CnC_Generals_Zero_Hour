# Generals/Code/GameEngineDevice/Source/W3DDevice/GameClient/W3DTerrainTracks.cpp

## Purpose
Manages rendering of vehicle tracks on terrain in the SAGE engine.

## Responsibilities
- Creates and updates track segments for moving objects
- Manages track fading and expiration
- Handles track capping for objects entering/exiting fog of war
- Optimizes track rendering using dynamic vertex buffers

## Key Types
- **TerrainTracksRenderObjClass** (Class): Represents a single track mark with edge management
- **TerrainTracksRenderObjClassSystem** (Class): Manages all track marks system-wide
- **edgeInfo** (Struct): Stores track segment geometry and UVs
- **None** (Enums)

## Key Functions
### computeTrackSpacing
- Purpose: Calculates spacing between track segments
- Calls: Not inferable from snippet

### TerrainTracksRenderObjClassSystem::update
- Purpose: Updates all active track marks (fading, expiration)
- Calls: WW3D::Get_Sync_Time(), releaseTrack()

### TerrainTracksRenderObjClassSystem::flush
- Purpose: Renders all active track marks
- Calls: DX8Wrapper::Set_Material(), DX8Wrapper::Set_Shader(), DX8Wrapper::Draw_Triangles()

### TerrainTracksRenderObjClass::addEdgeToTrack
- Purpose: Adds a new track segment when object moves
- Calls: TheTerrainLogic->getGroundHeight(), TheTerrainLogic->getLayerHeight()

## Globals
- **TheTerrainTracksRenderObjClassSystem** (TerrainTracksRenderObjClassSystem*): Singleton for track drawing system

## Dependencies
- W3DDevice/GameClient/W3DTerrainTracks.h
- W3DDevice/GameClient/heightmap.h
- Common/PerfTimer.h
- common/GlobalData.h
- texture.h
- colmath.h
- assetmgr.h
- WW3D2/DX8Wrapper.h
- GameLogic/TerrainLogic.h
- GameClient/Drawable.h
