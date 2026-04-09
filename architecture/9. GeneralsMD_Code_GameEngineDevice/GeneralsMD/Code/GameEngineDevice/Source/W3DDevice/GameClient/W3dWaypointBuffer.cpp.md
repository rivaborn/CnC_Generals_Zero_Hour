# GeneralsMD/Code/GameEngineDevice/Source/W3DDevice/GameClient/W3dWaypointBuffer.cpp

## Purpose
Handles rendering of waypoints and rally points in the game scene, used for path visualization and unit movement guidance.

## Responsibilities
- Renders waypoint paths for selected units in waypoint plotting mode
- Draws rally points for buildings with exit interfaces
- Handles special case for listening outposts revealing enemy paths
- Manages line and node rendering with proper culling and lighting

## Key Types
- **W3DWaypointBuffer (Class)**: Main class managing waypoint rendering
- **SegmentedLineClass (Pointer)**: Handles line rendering between waypoints
- **RenderInfoClass**: Contains rendering context and camera information

## Key Functions
### W3DWaypointBuffer::drawWaypoints
- Purpose: Renders waypoints and rally points based on current game state
- Calls: `setDefaultLineStyle`, `WW3D::Render`, `m_line->Set_Points`, `m_line->Render`

### W3DWaypointBuffer::setDefaultLineStyle
- Purpose: Configures the visual appearance of waypoint lines
- Calls: `m_line->Set_Texture`, `m_line->Set_Shader`, `m_line->Set_Width`, `m_line->Set_Color`

## Globals
- **MAX_DISPLAY_NODES (const int)**: Maximum number of waypoints that can be displayed (512)

## Dependencies
- Key includes: `W3DWaypointBuffer.h`, `assetmgr.h`, `texture.h`, `Common/GlobalData.h`, `GameClient/Drawable.h`, `GameLogic/Object.h`, `WW3D2/Camera.h`, `WW3D2/Segline.h`
- External symbols: `WW3DAssetManager`, `TheInGameUI`, `TheGameClient`, `WW3D::Render`
