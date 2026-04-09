# Generals/Code/Tools/WorldBuilder/include/HandScrollTool.h

## Purpose
Defines the HandScrollTool class, a scrolling tool for the WorldBuilder editor.

## Responsibilities
- Handles mouse input for panning the view
- Manages scroll state and hysteresis
- Implements tool activation/deactivation
- Tracks mouse movement for smooth scrolling

## Key Types
- **HandScrollTool (Class)**: Scrolling tool implementation.
- **(anonymous enum) (Enum)**: Defines hysteresis threshold (3 pixels).
- **HYSTERESIS (Enum)**: Constant for mouse movement threshold.

## Key Functions
### HandScrollTool
- Purpose: Constructor for HandScrollTool.
- Calls: None

### ~HandScrollTool
- Purpose: Destructor for HandScrollTool.
- Calls: None

### mouseDown
- Purpose: Initiates scrolling when mouse button is pressed.
- Calls: None

### mouseMoved
- Purpose: Handles view scrolling during mouse movement.
- Calls: None

### mouseUp
- Purpose: Ends scrolling when mouse button is released.
- Calls: None

### activate
- Purpose: Activates the tool in the WorldBuilder interface.
- Calls: None

### followsTerrain
- Purpose: Indicates whether the tool follows terrain (returns false).
- Calls: None

## Globals
- **m_prevPt2d (CPoint)**: Previous mouse position for scroll calculation.
- **m_downPt2d (CPoint)**: Mouse position when scroll started.
- **m_scrolling (Bool)**: Flag indicating active scrolling state.
- **m_mouseDownTime (UINT)**: Timestamp when mouse was pressed.

## Dependencies
- **Tool.h**: Base class for WorldBuilder tools
- **CPoint**: Windows point structure
- **WbView**: WorldBuilder view class
- **CWorldBuilderDoc**: WorldBuilder document class
-
