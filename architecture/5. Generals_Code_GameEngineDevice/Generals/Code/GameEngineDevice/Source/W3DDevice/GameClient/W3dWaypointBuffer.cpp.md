# Generals/Code/GameEngineDevice/Source/W3DDevice/GameClient/W3dWaypointBuffer.cpp

## Purpose
Handles rendering of waypoints and rally points in the game scene.

## Responsibilities
- Renders waypoint paths for selected units in waypoint plotting mode
- Draws rally point lines and markers for locally controlled objects
- Manages waypoint node visualization (hockey puck models)
- Handles line rendering with textured segments
- Implements box wrapping logic for rally point paths

## Key Types
- `W3DWaypointBuffer` (Class): Main class managing waypoint rendering
- `SegmentedLineClass` (Pointer): Handles line rendering with textures
- `RenderInfoClass` (Reference): Contains rendering context information

## Key Functions
### `drawWaypoints`
- Purpose: Renders waypoints and rally points based on current game state
- Calls: `WW3D::Render`, `m_line->Set_Points`, `m_line->Render`, `ai->friend_getWaypointGoalPathSize`, `ai->friend_getCurrentGoalPathIndex`, `ai->friend_getGoalPathPosition`, `exitInterface->getExitPosition`, `exitInterface->getNaturalRallyPoint`, `exitInterface->getRallyPoint`

### `freeWaypointBuffers`
- Purpose: Releases waypoint rendering buffers
- Calls: None

## Globals
- `MAX_DISPLAY_NODES` (const int): Maximum number of waypoints to display (512)

## Dependencies
- Key includes: `W3DWaypointBuffer.h`, `assetmgr.h`, `texture.h`, `Common/GlobalData.h`, `GameClient/Drawable.h`, `GameClient/GameClient.h`, `GameClient/InGameUI.h`, `GameLogic/Object.h`, `GameLogic/Module/AIUpdate.h`, `W3DDevice/GameClient/TerrainTex.h`, `W3DDevice/GameClient/HeightMap.h`, `WW3D2/Camera.h`, `WW3D2/DX8Wrapper.h`, `WW3D2/DX8Renderer.h`, `WW3D2/Mesh.h`, `WW3D2/MeshMdl.h`, `WW3D2/Segline.h`
- External symbols: `WW3DAssetManager`, `TheInGameUI`, `KINDOF_IGNORED_IN_GUI`
