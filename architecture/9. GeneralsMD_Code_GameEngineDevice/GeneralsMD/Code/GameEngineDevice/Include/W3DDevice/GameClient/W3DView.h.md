# GeneralsMD/Code/GameEngineDevice/Include/W3DDevice/GameClient/W3DView.h

## Purpose
Defines the W3DView class, a game view window implementation for the W3D engine, handling camera controls and rendering.

## Responsibilities
- Manages 3D camera and 2D overlay camera
- Handles camera movements (rotation, zoom, pitch, waypoint paths)
- Provides screen/world coordinate transformations
- Implements view filtering and special effects
- Supports camera locking and constraints

## Key Types
- **Drawable (Class)**: Base class for pickable game objects
- **TMoveAlongWaypointPathInfo (Struct)**: Stores waypoint path movement data
- **TRotateCameraInfo (Struct)**: Contains rotation camera movement parameters
- **TPitchCameraInfo (Struct)**: Holds pitch camera movement data
- **TZoomCameraInfo (Struct)**: Manages zoom camera movement parameters
- **W3DView (Class)**: Main view class implementing View interface

## Key Functions
### `drawView()`
- Purpose: Renders the view
- Calls: `draw()`, `updateView()`

### `updateView()`
- Purpose: Updates camera and object transforms per frame
- Calls: `updateCameraMovements()`, `setCameraTransform()`

### `moveCameraAlongWaypointPath()`
- Purpose: Initiates camera movement along a waypoint path
- Calls: `setupWaypointPath()`

### `updateCameraMovements()`
- Purpose: Processes ongoing camera movements
- Calls: `rotateCameraOneFrame()`, `zoomCameraOneFrame()`, `pitchCameraOneFrame()`, `moveAlongWaypointPath()`

### `worldToScreenTriReturn()`
- Purpose: Transforms world coordinates to screen coordinates
- Calls: None

## Globals
- **TheW3DFrameLengthInMsec (Int)**: Default frame length in milliseconds (33ms = 30fps)

## Dependencies
- `View.h` (base class)
- `Camera.h` (W3D2 camera class)
- `ParabolicEase.h` (easing functions)
- `STLTypedefs.h` (STL type definitions)
- `SubsystemInterface` (game subsystem interface)
