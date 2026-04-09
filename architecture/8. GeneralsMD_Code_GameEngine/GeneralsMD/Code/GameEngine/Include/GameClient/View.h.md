# GeneralsMD/Code/GameEngine/Include/GameClient/View.h

## Purpose
Defines the `View` class and related types for rendering the game world in a window.

## Responsibilities
- Manages camera position, angle, pitch, and zoom
- Handles coordinate transformations between world and screen space
- Supports camera locking, shaking, and movement effects
- Provides picking and iteration over drawables in the view

## Key Types
- **View (Class)**: Main view/camera class for rendering the world
- **ViewLocation (Class)**: Stores view position, angle, pitch, and zoom for serialization
- **PickType (Enum)**: Types of objects to pick (terrain, selectables, etc.)
- **CameraShakeType (Enum)**: Intensity levels for camera shaking
- **WorldToScreenReturn (Enum)**: Return codes for world-to-screen transformations
- **CameraLockType (Enum)**: Follow or tether locking modes

## Key Functions
### `pickDrawable`
- Purpose: Picks a drawable at screen coordinates
- Calls: Not visible in header

### `worldToScreenTriReturn`
- Purpose: Transforms world coordinates to screen with detailed return status
- Calls: Not visible in header

### `lookAt`
- Purpose: Centers the view on a world coordinate
- Calls: Not visible in header

### `shake`
- Purpose: Applies camera shake effect
- Calls: Not visible in header

## Globals
- **TheTacticalView (View*)**: Global pointer to the main tactical view

## Dependencies
- `Common/GameType.h`, `Common/Snapshot.h`, `Lib/BaseType.h`, `WW3D2/ColType.h`
- `Drawable`, `ViewLocation`, `Thing`, `Waypoint`, `LookAtTranslator` (forward declarations)
