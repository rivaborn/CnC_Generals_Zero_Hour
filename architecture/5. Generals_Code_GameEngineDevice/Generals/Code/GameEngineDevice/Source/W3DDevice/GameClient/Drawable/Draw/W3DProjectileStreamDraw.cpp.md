# Generals/Code/GameEngineDevice/Source/W3DDevice/GameClient/Drawable/Draw/W3DProjectileStreamDraw.cpp

## Purpose
Handles rendering of textured lines (streams) between projectile positions in the game world.

## Responsibilities
- Manages segmented line objects for projectile trails
- Updates line positions based on projectile movement
- Handles texture tiling and scrolling for visual effects
- Manages line visibility based on shroud state
- Cleans up resources when destroyed

## Key Types
- `W3DProjectileStreamDrawModuleData` (Class): Stores configuration data for projectile stream rendering
- `W3DProjectileStreamDraw` (Class): Main draw module class that handles rendering
- `SegmentedLineClass` (External): Line rendering object used for projectile trails

## Key Functions
### `doDrawModule`
- Purpose: Renders projectile streams by creating/updating segmented lines between projectile positions
- Calls: `getAllPoints`, `makeOrUpdateLine`, `W3DDisplay::m_3DScene->Remove_Render_Object`, `REF_PTR_RELEASE`

### `makeOrUpdateLine`
- Purpose: Creates new or updates existing segmented lines for projectile trails
- Calls: `NEW SegmentedLineClass`, `line->Set_Points`, `line->Set_Texture`, `line->Set_Shader`, `line->Set_Width`, `line->Set_Texture_Mapping_Mode`, `line->Set_Texture_Tile_Factor`, `line->Set_UV_Offset_Rate`, `W3DDisplay::m_3DScene->Add_Render_Object`

### `setFullyObscuredByShroud`
- Purpose: Handles visibility changes when shroud state changes
- Calls: `deadLine->Remove`, `W3DDisplay::m_3DScene->Add_Render_Object`

## Globals
- `MAX_PROJECTILE_STREAM` (const): Maximum number of projectile streams (20)

## Dependencies
- `Common/Xfer.h`, `GameClient/Drawable.h`, `GameLogic/Object.h`, `W3DDevice/GameClient/Module/W3DProjectileStreamDraw.h`, `W3DDevice/GameClient/W3DDisplay.h`, `W3DDevice/GameClient/W3DScene.h`, `WW3D2/AssetMgr.h`, `WW3D2/Segline.h`, `WWMath/Vector3.h`
- `WW3DAssetManager`, `SegmentedLineClass`, `ShaderClass`, `ProjectileStreamUpdate`, `NameKeyType`
