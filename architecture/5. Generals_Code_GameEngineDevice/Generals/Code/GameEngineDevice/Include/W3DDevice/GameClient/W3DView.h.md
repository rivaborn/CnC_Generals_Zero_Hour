# Generals/Code/GameEngineDevice/Include/W3DDevice/GameClient/W3DView.h

## Purpose
Defines the W3DView class, a 3D game view implementation for the SAGE engine, handling camera control, rendering, and view manipulation.

## Responsibilities
- Manages 3D camera and view transformations
- Handles camera movements (rotation, zoom, pitch, waypoint paths)
- Provides screen/world coordinate conversion
- Implements view filtering and special effects
- Supports object picking and region queries

## Key Types
- **Drawable (Class)**: Base class for pickable game objects
- **TMoveAlongWaypointPathInfo (struct)**: Stores waypoint path movement data
- **TRotateCameraInfo (struct)**: Tracks camera rotation parameters
- **TPitchCameraInfo (struct)**: Manages camera pitch interpolation
- **TZoomCameraInfo (struct)**: Handles camera zoom transitions
- **W3DView (Class)**: Main view class implementing View interface

## Key Functions
### `updateCameraMovements`
- Purpose: Updates camera movement state
- Calls: `rotateCameraOneFrame`, `zoomCameraOneFrame`, `pitchCameraOneFrame`, `moveAlongWaypointPath`

### `moveAlongWaypointPath`
- Purpose: Advances camera along a predefined waypoint path
- Calls: `setupWaypointPath`

### `rotateCameraOneFrame`
- Purpose: Performs one frame of camera rotation
- Calls: None visible

### `buildCameraTransform`
- Purpose: Calculates camera transformation matrix
- Calls: None visible

### `calcCameraConstraints`
- Purpose: Recalculates valid camera movement boundaries
- Calls: None visible

## Globals
- **TheW3DFrameLengthInMsec (Int)**: Stores frame timing in milliseconds

## Dependencies
- `View.h` (base class)
- `Camera.h` (W3D2 camera class)
- `Common/STLTypedefs.h` (STL types)
- `SubsystemInterface` (engine subsystem interface)
