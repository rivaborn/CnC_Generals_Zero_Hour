# Generals/Code/Tools/WorldBuilder/include/wbview3d.h

## Purpose
Header file defining the `WbView3d` class, which encapsulates the 3D view and rendering logic for the WorldBuilder tool.

## Responsibilities
- Manages 3D scene rendering, camera control, and view transformations
- Handles object selection, lighting, and map visualization
- Provides methods for converting between view and document coordinates
- Manages DirectX resources and device reset handling

## Key Types
- **WbView3d (Class)**: Main 3D view class for WorldBuilder
- **BodyDamageType (Enum)**: Damage state type for objects
- **WorldHeightMap (Class)**: Height map representation
- **LayerClass (Class)**: Layer management
- **IntersectionClass (Class)**: Object intersection handling
- **W3DAssetManager (Class)**: Asset management
- **SkeletonSceneClass (Class)**: Scene graph management
- **CameraClass (Class)**: Camera control
- **WBHeightMap (Class)**: Height map rendering
- **LightClass (Class)**: Light management
- **MapObject (Class)**: Map object representation
- **DrawObject (Class)**: Drawing object interface
- **CWorldBuilderView (Class)**: Main view interface
- **BuildListInfo (Class)**: Build list information
- **TransRenderObj (Class)**: Transparent render object
- **ID3DXFont (Class)**: DirectX font interface

## Key Functions
### OnDraw
- Purpose: Overridden to draw the 3D view
- Calls: `render()`, `drawLabels()`

### render
- Purpose: Renders the 3D scene
- Calls: `setupCamera()`, `updateLights()`, `updateScorches()`

### viewToDocCoords
- Purpose: Converts view coordinates to document coordinates
- Calls: None

### docToViewCoords
- Purpose: Converts document coordinates to view coordinates
- Calls: None

### updateHeightMapInView
- Purpose: Updates the height map in the view
- Calls: None

### invalObjectInView
- Purpose: Invalidates an object in the view
- Calls: None

### setDefaultCamera
- Purpose: Sets the default camera position
- Calls: None

### rotateCamera
- Purpose: Rotates the camera
- Calls: None

### pitchCamera
- Purpose: Pitches the camera
- Calls: None

### picked3dObjectInView
- Purpose: Picks a 3D object at the given view point
- Calls: None

### resetRenderObjects
- Purpose: Removes all render objects
- Calls: None

### redraw
- Purpose: Redraws the view
- Calls: `OnDraw()`

## Globals
