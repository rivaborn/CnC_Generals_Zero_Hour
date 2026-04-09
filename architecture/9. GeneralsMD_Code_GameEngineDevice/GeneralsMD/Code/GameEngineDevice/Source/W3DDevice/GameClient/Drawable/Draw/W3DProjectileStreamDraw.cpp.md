# GeneralsMD/Code/GameEngineDevice/Source/W3DDevice/GameClient/Drawable/Draw/W3DProjectileStreamDraw.cpp

## Purpose
Handles rendering of textured lines between projectile positions in the game world.

## Responsibilities
- Manages segmented line rendering between projectile positions
- Handles texture tiling and scrolling effects for projectile trails
- Updates line visibility based on shroud state
- Cleans up and recreates lines as projectiles move

## Key Types
- `W3DProjectileStreamDrawModuleData` (Class): Stores configuration data for projectile stream rendering
- `W3DProjectileStreamDraw` (Class): Main draw module class that manages line rendering
- `SegmentedLineClass` (External): Line rendering object used to draw projectile trails

## Key Functions
### `doDrawModule`
- Purpose: Renders projectile streams by creating/updating segmented lines between projectile positions
- Calls: `getAllPoints`, `makeOrUpdateLine`, `W3DDisplay::m_3DScene->Remove_Render_Object`, `W3DDisplay::m_3DScene->Add_Render_Object`

### `makeOrUpdateLine`
- Purpose: Creates or updates a segmented line with the given points and texture properties
- Calls: `SegmentedLineClass` methods (`Set_Points`, `Set_Texture`, etc.), `W3DDisplay::m_3DScene->Add_Render_Object`

### `setFullyObscuredByShroud`
- Purpose: Handles visibility changes when the area becomes shrouded/unshrouded
- Calls: `SegmentedLineClass::Remove`, `W3DDisplay::m_3DScene->Add_Render_Object`

## Globals
- `W3DDisplay::m_3DScene` (W3DScene*): Reference to the 3D scene for adding/removing render objects

## Dependencies
- `Common/Xfer.h`, `GameClient/Drawable.h`, `GameLogic/Object.h`
- `W3DDevice/GameClient/Module/W3DProjectileStreamDraw.h`
- `W3DDevice/GameClient/W3DDisplay.h`, `W3DDevice/GameClient/W3DScene.h`
- `WW3D2/AssetMgr.h`, `WW3D2/Segline.h`, `WWMath/Vector3.h`
