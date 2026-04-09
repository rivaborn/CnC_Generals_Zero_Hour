# Generals/Code/GameEngineDevice/Source/Win32Device/GameClient/Win32DIKeyboard.cpp

## Purpose
Implements Windows DirectInput keyboard interface for the game engine.

## Responsibilities
- Initializes and manages DirectInput keyboard device
- Handles keyboard input events and state tracking
- Provides keyboard state queries (e.g., caps lock)
- Manages device acquisition/reacquisition on focus changes

## Key Types
- `ErrorLookup` (Struct): Maps DirectInput HRESULT codes to human-readable strings
- `DirectInputKeyboard` (Class): Main keyboard interface implementation

## Key Functions
### `printReturnCode`
- Purpose: Debug helper to log DirectInput error codes
- Calls: None

### `openKeyboard`
- Purpose: Initializes DirectInput keyboard device and sets up input buffer
- Calls: `DirectInput8Create`, `CreateDevice`, `SetDataFormat`, `SetCooperativeLevel`, `SetProperty`, `Acquire`

### `closeKeyboard`
- Purpose: Releases DirectInput keyboard resources
- Calls: `Unacquire`, `Release`

### `getKey`
- Purpose: Retrieves single keyboard event from DirectInput buffer
- Calls: `Acquire`, `GetDeviceData`

### `init`
- Purpose: Initializes keyboard subsystem
- Calls: `Keyboard::init`, `openKeyboard`

### `update`
- Purpose: Updates keyboard state per frame
- Calls: `Keyboard::update`

### `getCapsState`
- Purpose: Checks caps lock state
- Calls: `GetKeyState`

## Globals
- `errorLookup` (ErrorLookup[]): Static array mapping DirectInput error codes to strings

## Dependencies
- Windows.h, dinput.h (implicit)
- Common/Debug.h, Common/Language.h
- GameClient/KeyDefs.h, GameClient/Keyboard.h
- Win32Device/GameClient/Win32DIKeyboard.h
- WinMain.h
