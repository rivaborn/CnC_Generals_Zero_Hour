# GeneralsMD/Code/Libraries/Source/WWVegas/WWLib/wwmouse.h

## Purpose
Defines the `WWMouseClass`, a mouse management system for the C&C game engine, handling cursor rendering, input processing, and visibility control.

## Responsibilities
- Manages mouse cursor rendering and input
- Handles mouse capture/release and visibility states
- Tracks mouse position and confining rectangles
- Maintains background buffers for mouse drawing/erasing

## Key Types
- `BSurface` (Class): Not inferable (forward declaration)
- `WWMouseClass` (Class): Mouse management system for the game engine

## Key Functions
### `WWMouseClass::Process_Mouse`
- Purpose: Maintenance callback for mouse processing
- Calls: Not inferable

### `WWMouseClass::Set_Cursor`
- Purpose: Sets the game-drawn mouse imagery
- Calls: Not inferable

### `WWMouseClass::Hide_Mouse`
- Purpose: Hides the game-drawn mouse cursor
- Calls: Not inferable

### `WWMouseClass::Show_Mouse`
- Purpose: Shows the game-drawn mouse cursor
- Calls: Not inferable

### `WWMouseClass::Draw_Mouse`
- Purpose: Renders the mouse onto an alternate surface
- Calls: Not inferable

### `WWMouseClass::Convert_Coordinate`
- Purpose: Converts OS screen coordinates to game coordinates
- Calls: Not inferable

## Globals
None

## Dependencies
- `win.h`, `xmouse.h` (includes)
- `Surface`, `ShapeSet`, `Rect`, `HWND`, `MMRESULT` (external types)
- `Mouse` (base class)
- `InterlockedIncrement`, `InterlockedDecrement` (Windows API)
