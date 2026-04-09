# GeneralsMD/Code/Libraries/Source/WWVegas/WWLib/keyboard.cpp

## Purpose
Handles keyboard and mouse input processing for the game, including buffering, translation, and system message handling.

## Responsibilities
- Manages keyboard input buffer (queue)
- Processes Windows messages for keyboard/mouse events
- Converts key codes to ASCII
- Tracks mouse button states and coordinates
- Provides blocking/non-blocking input retrieval

## Key Types
- `WWKeyboardClass` (Class): Main keyboard input handler
- `Buffer` (unsigned short[256]): Circular buffer for input events
- `KeyState` (unsigned char[256]): Tracks modifier key states

## Key Functions
### `Buff_Get`
- Purpose: Retrieves next key from buffer, updating mouse coords if mouse event
- Calls: `Fetch_Element`, `Is_Mouse_Key`

### `Put_Key_Message`
- Purpose: Translates and inserts key press/release into buffer with modifier bits
- Calls: `Put`, `Is_Mouse_Key`, `GetKeyState`

### `Message_Handler`
- Purpose: Processes Windows messages (WM_KEYDOWN/UP, WM_*BUTTONDOWN/UP/DBLCLK)
- Calls: `Put_Key_Message`, `Put_Mouse_Message`, `Stop_Execution`

### `To_ASCII`
- Purpose: Converts key code to ASCII using Windows API
- Calls: `MapVirtualKey`, `ToAscii`

### `Fill_Buffer_From_System`
- Purpose: Processes pending Windows messages into keyboard buffer
- Calls: `Windows_Message_Handler`

## Globals
- `MouseCursor` (Not inferable): Used for coordinate conversion
- `Stop_Execution` (function): Debug/emergency stop handler

## Dependencies
- Windows API: `GetKeyState`, `MapVirtualKey`, `ToAscii`, `DefWindowProc`
- External: `Windows_Message_Handler`, `MouseCursor` object
- Includes: `always.h`, `_xmouse.h`, `keyboard.h`, `msgloop.h`
