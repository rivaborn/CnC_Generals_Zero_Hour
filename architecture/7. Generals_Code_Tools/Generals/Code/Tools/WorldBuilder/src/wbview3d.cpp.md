# Generals/Code/Tools/WorldBuilder/src/wbview3d.cpp

## Purpose
Implements the 3D view for the WorldBuilder map editor, handling rendering, camera control, and scene management.

## Responsibilities
- Manages 3D scene rendering and object placement
- Handles camera movement and view settings
- Provides UI for toggling rendering options (wireframe, shadows, etc.)
- Integrates with heightmap and terrain editing systems
- Supports object tracking and selection visualization

## Key Types
- **WbView3d (Class)**: Main view class handling 3D rendering and user interaction
- **SkeletonSceneClass (Class)**: Custom scene class for WorldBuilder preview
- **PlaceholderView (Class)**: Stub View implementation for shadow manager compatibility
- **DebugType (Enum)**: Debug message types (not shown in snippet)

## Key Functions
### `setObjTracking`
- Purpose: Updates tracking visualization for a map object
- Calls: `getModelNameAndScale`, `Create_Render_Obj`, `Set_Transform`

### `scrollInView`
- Purpose: Scrolls the view by specified amounts
- Calls: `constrainCenterPt`, `redraw`, `drawLabels`, `syncViewCenters`

### `OnViewShowwireframe`
- Purpose: Toggles wireframe rendering mode
- Calls: `WriteProfileInt`

### `OnViewShowshadows`
- Purpose: Toggles shadow rendering
- Calls: `Get_Device_Resolution`, `resetRenderObjects`, `removeAllShadows`

## Globals
- **theDynamicLight (W3DDynamicLight*)**: Dynamic light for sample rendering
- **theLightXOffset (Real)**: Light position offset
- **theLightYOffset (Real)**: Light position offset
- **theFlashCount (Int)**: Flash counter for lighting effects
- **bogusTacticalView (PlaceholderView)**: Stub view for shadow manager

## Dependencies
- Key includes: `ww3d.h`, `scene.h`, `camera.h`, `W3DDevice/GameClient/W3DAssetManager.h`, `WorldBuilderDoc.h`
- External symbols: `TheW3DShadowManager`, `TheGlobalData`, `TheWritableGlobalData`, `TheTerrainRenderObject`, `TheLayersList`, `TheTacticalView`
