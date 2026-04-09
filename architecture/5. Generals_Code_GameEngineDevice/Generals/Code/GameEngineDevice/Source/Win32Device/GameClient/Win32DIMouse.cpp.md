# Generals/Code/GameEngineDevice/Source/Win32Device/GameClient/Win32DIMouse.cpp

## Purpose
Implements DirectInput mouse handling for the Windows platform in the SAGE engine.

## Responsibilities
- Initializes and manages DirectInput mouse device
- Processes mouse input events (position, buttons, wheel)
- Handles mouse cursor visibility and clipping
- Manages mouse capture/release for window focus
- Maps DirectInput mouse data to internal format

## Key Types
- MOUSE_BUFFER_SIZE (Enum): Defines the mouse event buffer size (256)

## Key Functions
### openMouse
- Purpose: Creates and initializes DirectInput mouse device
- Calls: DirectInput8Create, CreateDevice, SetDataFormat, SetCooperativeLevel, SetProperty, Acquire, GetCapabilities

### closeMouse
- Purpose: Releases DirectInput mouse resources
- Calls: Unacquire, Release

### getMouseEvent
- Purpose: Retrieves a single mouse event from the device
- Calls: Poll, GetDeviceData, mapDirectInputMouse, Acquire

### mapDirectInputMouse
- Purpose: Converts DirectInput mouse data to internal format
- Calls: None

### update
- Purpose: Updates mouse position using Windows cursor
- Calls: Mouse::update, GetCursorPos, ScreenToClient, moveMouse

### setMouseLimits
- Purpose: Configures mouse movement boundaries
- Calls: Mouse::setMouseLimits, GetWindowRect, ClipCursor

### setCursor
- Purpose: Sets the visible mouse cursor
- Calls: Mouse::setCursor, SetCursor, LoadCursor

## Globals
- None

## Dependencies
- DirectInput headers (dinput.h)
- Windows API (windows.h)
- Common/Debug.h
- GameClient/Display.h
- Win32DIMouse.h
- WinMain.h
