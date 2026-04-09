# Generals/Code/Libraries/Source/WWVegas/WWLib/keyboard.cpp

## Purpose
Handles keyboard and mouse input processing for the game, including buffer management and Windows message handling.

## Responsibilities
- Manages keyboard input buffer (queue)
- Processes Windows messages for keyboard/mouse events
- Converts key codes to ASCII
- Tracks mouse button states and coordinates
- Provides blocking/non-blocking input retrieval

## Key Types
- `WWKeyboardClass` (Class): Main keyboard input handler
- `Stop_Execution` (Function): Debug/breakpoint function

## Key Functions
### `Buff_Get`
- Purpose: Retrieves a key from the buffer, updating mouse coordinates if applicable
- Calls: `Fetch_Element`, `Is_Mouse_Key`

### `Put_Key_Message`
- Purpose: Translates and inserts a key message into the buffer with modifier state
- Calls: `Put`, `Is_Mouse_Key`

### `Put_Mouse_Message`
- Purpose: Stores mouse events (button + coordinates) into the buffer
- Calls: `Put_Key_Message`, `Put`, `Available_Buffer_Room`, `Is_Mouse_Key`

### `Message_Handler`
- Purpose: Processes Windows messages for keyboard/mouse input
- Calls: `Put_Key_Message`, `Put_Mouse_Message`, `Stop_Execution`

### `To_ASCII`
- Purpose: Converts key code to ASCII considering shift/ctrl/alt state
- Calls: `MapVirtualKey`, `ToAscii`

## Globals
- `MouseQX` (int): Queued mouse X coordinate
- `MouseQY` (int): Queued mouse Y coordinate
- `Head` (int): Buffer read position
- `Tail` (int): Buffer write position
- `KeyState` (unsigned char[256]): Keyboard modifier state

## Dependencies
- Windows API: `GetKeyState`, `MapVirtualKey`, `ToAscii`, `DefWindowProc`
- External: `MouseCursor` (pointer), `Windows_Message_Handler` (function)
- Includes: `always.h`, `_xmouse.h`, `keyboard.h`, `msgloop.h`
