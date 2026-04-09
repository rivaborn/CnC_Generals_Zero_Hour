# Generals/Code/GameEngine/Source/GameClient/View.cpp

## Purpose
Manages the game's view/camera system, handling positioning, zooming, and rendering transformations.

## Responsibilities
- Controls camera position, angle, and zoom
- Manages view boundaries and screen-to-world projections
- Handles camera locking and view synchronization
- Provides serialization for network sync (Xfer)
- Maintains tactical view singleton

## Key Types
- View (Class): Core view/camera management class
- ViewLocation (Struct): Stores view position/rotation/zoom state

## Key Functions
### View::init
- Purpose: Initializes default view parameters
- Calls: None

### View::lookAt
- Purpose: Centers the view on a world coordinate
- Calls: setPosition

### View::scrollBy
- Purpose: Shifts the view by a delta
- Calls: None

### View::xfer
- Purpose: Serializes view state for network sync
- Calls: getAngle, setAngle, getPosition, lookAt

## Globals
- TheTacticalView (View*): Singleton reference to the main tactical view

## Dependencies
- PreRTS.h, GameEngine.h, Xfer.h, View.h, Drawable.h
- Uses Coord3D, Coord2D, ICoord2D, Xfer, ViewLocation
- TheGlobalData (external global)
