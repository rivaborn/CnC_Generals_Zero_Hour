# GeneralsMD/Code/Libraries/Source/WWVegas/WWLib/_xmouse.h

## Purpose
Header file providing inline wrapper functions for mouse cursor management in the SAGE engine.

## Responsibilities
- Declares global mouse cursor pointer
- Provides inline wrappers for mouse operations
- Exposes mouse state and position queries

## Key Types
- None

## Key Functions
### Hide_Mouse
- Purpose: Hides the mouse cursor
- Calls: MouseCursor->Hide_Mouse()

### Show_Mouse
- Purpose: Shows the mouse cursor
- Calls: MouseCursor->Show_Mouse()

### Conditional_Hide_Mouse
- Purpose: Hides mouse cursor conditionally based on rectangle
- Calls: MouseCursor->Conditional_Hide_Mouse(rect)

### Conditional_Show_Mouse
- Purpose: Shows mouse cursor if previously hidden
- Calls: MouseCursor->Conditional_Show_Mouse()

### Get_Mouse_State
- Purpose: Returns current mouse button state
- Calls: MouseCursor->Get_Mouse_State()

### Set_Mouse_Cursor
- Purpose: Sets mouse cursor appearance and hotspot
- Calls: MouseCursor->Set_Cursor(hotx, hoty, cursor, shape)

### Get_Mouse_X
- Purpose: Returns current mouse X coordinate
- Calls: MouseCursor->Get_Mouse_X()

### Get_Mouse_Y
- Purpose: Returns current mouse Y coordinate
- Calls: MouseCursor->Get_Mouse_Y()

## Globals
- MouseCursor (Mouse*): Global pointer to the mouse cursor object

## Dependencies
- xmouse.h (included)
- Mouse class (external, not defined here)
- Rect struct (external)
- ShapeSet class (external)
