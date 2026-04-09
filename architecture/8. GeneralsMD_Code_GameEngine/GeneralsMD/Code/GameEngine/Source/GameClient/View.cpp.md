# GeneralsMD/Code/GameEngine/Source/GameClient/View.cpp

## Purpose
Manages the game's view/camera system, handling positioning, zooming, and rendering transformations.

## Responsibilities
- Maintains view position, angle, pitch, and zoom
- Handles camera locking and scrolling
- Provides screen-to-world coordinate conversion
- Manages view state serialization/deserialization
- Controls tactical view singleton

## Key Types
- View (Class): Core view/camera management class
- ViewLocation (Struct): Stores view position/orientation for serialization

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

### View::getScreenCornerWorldPointsAtZ
- Purpose: Projects screen corners to world space at given Z
- Calls: getOrigin, screenToWorldAtZ

### View::xfer
- Purpose: Serializes/deserializes view state
- Calls: getAngle, setAngle, getPosition, lookAt

## Globals
- TheTacticalView (View*): Singleton reference to the main tactical view
- View::m_idNext (UnsignedInt): Counter for generating unique view IDs

## Dependencies
- PreRTS.h, GameEngine.h, Xfer.h, View.h, Drawable.h
- Uses Coord3D, Coord2D, ICoord2D, Xfer, ViewLocation types
- References TheGlobalData for camera height limits
