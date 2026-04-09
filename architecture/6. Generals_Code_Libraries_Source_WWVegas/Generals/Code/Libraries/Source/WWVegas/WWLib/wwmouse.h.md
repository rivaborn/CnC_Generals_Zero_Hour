# Generals/Code/Libraries/Source/WWVegas/WWLib/wwmouse.h

## Purpose
Defines the `WWMouseClass`, a mouse input and rendering handler for the C&C game engine.

## Responsibilities
- Manages mouse visibility, position, and cursor rendering
- Handles mouse capture/release for OS interaction
- Tracks mouse state and coordinates
- Renders mouse cursor on game surfaces

## Key Types
- `BSurface` (Class): Not inferable
- `WWMouseClass` (Class): Mouse input and rendering handler

## Key Functions
### `WWMouseClass::Process_Mouse`
- Purpose: Maintenance callback for mouse processing
- Calls: Not inferable

### `WWMouseClass::Set_Cursor`
- Purpose: Sets the game-drawn mouse imagery
- Calls: Not inferable

### `WWMouseClass::Hide_Mouse`
- Purpose: Hides the game-drawn mouse
- Calls: Not inferable

### `WWMouseClass::Show_Mouse`
- Purpose: Shows the game-drawn mouse
- Calls: Not inferable

### `WWMouseClass::Release_Mouse`
- Purpose: Releases mouse control to the OS
- Calls: Not inferable

### `WWMouseClass::Capture_Mouse`
- Purpose: Takes control of the mouse from the OS
- Calls: Not inferable

### `WWMouseClass::Get_Mouse_State`
- Purpose: Queries the mouse visibility state
- Calls: Not inferable

### `WWMouseClass::Set_Mouse_XY`
- Purpose: Sets the mouse location
- Calls: Not inferable

### `WWMouseClass::Draw_Mouse`
- Purpose: Renders the mouse onto a surface
- Calls: Not inferable

### `WWMouseClass::Erase_Mouse`
- Purpose: Erases the mouse from a surface
- Calls: Not inferable

### `WWMouseClass::Convert_Coordinate`
- Purpose: Converts OS screen coordinates to game coordinates
- Calls: Not inferable

### `WWMouseClass::Calc_Confining_Rect`
- Purpose: Recalculates the confining rectangle from the window
- Calls: Not inferable

## Globals
- None

## Dependencies
- `win.h`
- `xmouse.h`
- `Surface` (external)
- `ShapeSet` (external)
- `Rect` (external)
- `HWND` (external)
- `MMRESULT` (external)
