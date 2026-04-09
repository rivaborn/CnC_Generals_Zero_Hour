# GeneralsMD/Code/GameEngineDevice/Source/Win32Device/GameClient/Win32DIKeyboard.cpp

## Purpose
Implements Windows DirectInput keyboard interface for the game engine.

## Responsibilities
- Initializes and manages DirectInput keyboard device
- Handles keyboard input events and state tracking
- Provides keyboard state queries (e.g., caps lock)
- Manages device acquisition/reacquisition on focus changes

## Key Types
- `DirectInputKeyboard` (Class): Main keyboard interface implementation
- `ErrorLookup` (Struct): Maps HRESULT codes to error strings
- `(anonymous enum)` (Enum): Defines `KEYBOARD_BUFFER_SIZE` constant

## Key Functions
### `printReturnCode`
- Purpose: Debug helper to log DirectInput error codes
- Calls: None

### `openKeyboard`
- Purpose: Initializes DirectInput keyboard device
- Calls: `closeKeyboard`, `DirectInput8Create`, `CreateDevice`, `SetDataFormat`, `SetCooperativeLevel`, `SetProperty`, `Acquire`

### `closeKeyboard`
- Purpose: Releases DirectInput keyboard resources
- Calls: `Unacquire`, `Release`

### `getKey`
- Purpose: Retrieves single keyboard event from DirectInput
- Calls: `Acquire`, `GetDeviceData`

### `init`
- Purpose: Initializes keyboard subsystem
- Calls: `Keyboard::init`, `openKeyboard`

### `update`
- Purpose: Updates keyboard state per frame
- Calls: `Keyboard::update`

### `getCapsState`
- Purpose: Checks caps lock state
- Calls: `GetKeyState`, `BitTest`

## Globals
- `errorLookup` (ErrorLookup[]): Static array mapping HRESULT codes to strings

## Dependencies
- Windows.h, dinput.h (implicit)
- Common/Debug.h, Common/Language.h
- GameClient/KeyDefs.h, GameClient/Keyboard.h
- Win32Device/GameClient/Win32DIKeyboard.h
- WinMain.h (for ApplicationHInstance/HWnd)
