# GeneralsMD/Code/Libraries/Source/WWVegas/WWLib/wwmouse.cpp

## Purpose
Handles mouse input, cursor rendering, and position tracking for the game.

## Responsibilities
- Manages mouse cursor visibility and positioning
- Handles cursor shape changes and animations
- Processes mouse movement via OS callbacks
- Maintains background buffer for cursor drawing
- Confines mouse to game window boundaries

## Key Types
- `WWMouseClass` (Class): Main mouse handler with cursor rendering and input tracking
- `Rect` (Struct): Rectangle definition for mouse boundaries
- `ShapeSet` (Pointer): Reference to cursor shape data

## Key Functions
### `Callback_Process_Mouse`
- Purpose: OS callback for periodic mouse processing
- Calls: `Process_Mouse`

### `WWMouseClass::Process_Mouse`
- Purpose: Updates mouse position and redraws cursor
- Calls: `Get_Bounded_Position`, `Update_Mouse_Position`

### `WWMouseClass::Set_Cursor`
- Purpose: Changes cursor shape and hotspot
- Calls: `Block_Mouse`, `Low_Hide_Mouse`, `Low_Show_Mouse`, `Unblock_Mouse`

### `WWMouseClass::Capture_Mouse`
- Purpose: Takes control of mouse from OS
- Calls: `Block_Mouse`, `Hide_Mouse`, `Show_Mouse`, `Unblock_Mouse`

### `WWMouseClass::Release_Mouse`
- Purpose: Returns mouse control to OS
- Calls: `Block_Mouse`, `Hide_Mouse`, `Show_Mouse`, `Unblock_Mouse`

## Globals
- `_MousePtr` (WWMouseClass*): Persistent pointer to current mouse handler instance

## Dependencies
- `Surface`, `BSurface`, `ShapeSet`, `Rect`, `Point2D` classes
- Windows API: `timeSetEvent`, `timeKillEvent`, `GetCursorPos`, `SetCursorPos`, `ShowCursor`
- Other: `Blit_Block`, `InterlockedIncrement`, `InterlockedDecrement`
