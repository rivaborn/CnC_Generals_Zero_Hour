# Generals/Code/GameEngineDevice/Include/Win32Device/GameClient/Win32DIMouse.h

## Purpose
Declares the DirectInputMouse class, a Win32 DirectInput implementation for mouse input handling.

## Responsibilities
- Manages DirectInput mouse device initialization and cleanup
- Updates mouse state and maps DirectInput data to internal format
- Handles mouse capture/release and cursor management
- Provides mouse position and event querying

## Key Types
- **DirectInputMouse (Class)**: Win32 DirectInput mouse device implementation

## Key Functions
### DirectInputMouse::init
- Purpose: Initialize the DirectInput mouse device
- Calls: openMouse

### DirectInputMouse::update
- Purpose: Update mouse state from DirectInput
- Calls: getMouseEvent, mapDirectInputMouse

### DirectInputMouse::getMouseEvent
- Purpose: Retrieve mouse events from DirectInput device
- Calls: Not inferable

### DirectInputMouse::mapDirectInputMouse
- Purpose: Convert DirectInput mouse data to internal MouseIO format
- Calls: Not inferable

### DirectInputMouse::capture
- Purpose: Capture mouse input
- Calls: Not inferable

### DirectInputMouse::releaseCapture
- Purpose: Release mouse capture
- Calls: Not inferable

## Globals
- None

## Dependencies
- `<dinput.h>` (DirectInput headers)
- `GameClient/Mouse.h` (base Mouse class)
- `LPDIRECTINPUT8`, `LPDIRECTINPUTDEVICE8` (DirectInput interfaces)
