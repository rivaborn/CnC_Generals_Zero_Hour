# GeneralsMD/Code/GameEngine/Include/GameClient/Mouse.h

## Purpose
Defines the mouse input system interface for the SAGE engine, including cursor management and tooltip display.

## Responsibilities
- Manages mouse input state (position, buttons, wheel)
- Handles cursor rendering and switching
- Provides tooltip and cursor text display
- Tracks mouse events and drag detection
- Configures mouse behavior via INI settings

## Key Types
- **MouseButtonState (Enum)**: Mouse button states (Up, Down, DoubleClick)
- **MouseIO (Struct)**: Mouse input data (position, buttons, wheel, events)
- **CursorInfo (Class)**: Cursor appearance and behavior properties
- **Mouse (Class)**: Core mouse subsystem interface
- **MouseCursor (Enum)**: Cursor types (NORMAL, ARROW, CROSS, etc.)
- **RedrawMode (Enum)**: Cursor rendering methods (Windows, W3D, Polygon, DX8)

## Key Functions
### `update()`
- Purpose: Updates mouse state from device input
- Calls: `updateMouseData()`, `processMouseEvent()`, `checkForDrag()`

### `draw()`
- Purpose: Renders the mouse cursor and associated text/tooltips
- Calls: `drawTooltip()`, `drawCursorText()`

### `setCursorTooltip()`
- Purpose: Sets the tooltip text and display parameters
- Calls: None (direct member variable access)

### `isClick()`
- Purpose: Determines if a mouse click occurred between two points
- Calls: None

## Globals
- **TheMouse (Mouse*)**: Singleton instance of the mouse subsystem

## Dependencies
- `Lib/BaseType.h`, `Common/SubsystemInterface.h`, `Common/AsciiString.h`, `Common/UnicodeString.h`
- `DisplayString` (forward reference)
- `RGBAColorInt`, `RGBColor`, `ICoord2D`, `UnsignedInt`, `Int`, `Bool`, `Real` (base types)
