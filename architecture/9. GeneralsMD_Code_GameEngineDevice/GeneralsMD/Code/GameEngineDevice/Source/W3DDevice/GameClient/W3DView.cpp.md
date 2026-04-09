# GeneralsMD/Code/GameEngineDevice/Source/W3DDevice/GameClient/W3DView.cpp

## Purpose
Implements the W3DView class, handling 3D camera positioning, rendering, and view management in the SAGE engine.

## Responsibilities
- Manages 3D/2D camera systems
- Handles camera movement, rotation, zooming, and shaking
- Processes view transformations and rendering
- Supports scripted camera paths and waypoints
- Implements screen-to-world coordinate conversion

## Key Types
- W3DView (Class): Main view management class for 3D rendering
- CameraShakeType (Enum): Defines types of camera shake effects
- RotateCameraInfo/PitchCameraInfo/ZoomCameraInfo (Structs): Camera animation data

## Key Functions
### normAngle
- Purpose: Normalizes an angle to Â±PI range
- Calls: None

### getHeightAroundPos
- Purpose: Calculates maximum terrain height around a position
- Calls: TheTerrainLogic->getGroundHeight

### shake
- Purpose: Applies camera shake effect from an epicenter
- Calls: GameClientRandomValueReal

### screenToWorldAtZ
- Purpose: Converts screen coordinates to world space at a given Z
- Calls: getPickRay, Vector3::Find_X_At_Z, Vector3::Find_Y_At_Z

### rotateCameraOneFrame/zoomCameraOneFrame/pitchCameraOneFrame
- Purpose: Animates camera rotation/zoom/pitch over time
- Calls: WWMath::Lerp, WWMath::Acos, normAngle

### moveAlongWaypointPath
- Purpose: Moves camera along predefined waypoint path
- Calls: WWMath::Sqrt, setPosition, minf/maxf

## Globals
- TheW3DFrameLengthInMsec (Int): Frame timing in milliseconds
- MAX_REQUEST_CACHE_SIZE (const Int): Maximum location request cache size
- DRAWABLE_OVERSCAN (const Real): 3D world overscan amount

## Dependencies
- WW3D2/DX8Renderer.h, Camera.h, Light.h
- GameClient headers (Drawable, GameClient, etc.)
- GameLogic headers (AI, GameLogic, etc.)
- W3DDevice headers (W3DAssetManager, W3DScene, etc.)
- D3dx8math.h for math operations
