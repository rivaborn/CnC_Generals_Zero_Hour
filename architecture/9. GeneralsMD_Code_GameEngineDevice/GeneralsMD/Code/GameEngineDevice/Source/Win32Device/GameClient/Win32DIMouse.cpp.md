# GeneralsMD/Code/GameEngineDevice/Source/Win32Device/GameClient/Win32DIMouse.cpp

## Purpose
Implements DirectInput mouse handling for the Windows platform in the SAGE engine.

## Responsibilities
- Initializes and manages DirectInput mouse device
- Processes mouse input events (position, buttons, wheel)
- Handles mouse capture/release and cursor visibility
- Manages mouse movement within window boundaries

## Key Types
- `DirectInputMouse` (Class): DirectInput mouse device wrapper
- `MOUSE_BUFFER_SIZE` (Enum): Buffer size constant (256)

## Key Functions
### `openMouse`
- Purpose: Creates and initializes DirectInput mouse device
- Calls: `DirectInput8Create`, `CreateDevice`, `SetDataFormat`, `SetCooperativeLevel`, `SetProperty`, `Acquire`, `GetCapabilities`

### `closeMouse`
- Purpose: Releases DirectInput mouse resources
- Calls: `Unacquire`, `Release`

### `getMouseEvent`
- Purpose: Retrieves single mouse event from device buffer
- Calls: `Poll`, `GetDeviceData`, `mapDirectInputMouse`, `Acquire`

### `mapDirectInputMouse`
- Purpose: Converts DirectInput mouse data to internal format
- Calls: None

### `update`
- Purpose: Updates mouse position using Windows cursor
- Calls: `Mouse::update`, `GetCursorPos`, `ScreenToClient`, `moveMouse`

### `setMouseLimits`
- Purpose: Confines mouse to client area in windowed mode
- Calls: `Mouse::setMouseLimits`, `GetWindowRect`, `ClipCursor`

### `setCursor`
- Purpose: Changes system cursor appearance
- Calls: `Mouse::setCursor`, `SetCursor`, `LoadCursor`

## Globals
- `ApplicationHInstance` (HINSTANCE): Global application instance
- `ApplicationHWnd` (HWND): Global application window handle

## Dependencies
- DirectInput headers (`dinput.h` implied)
- Windows API (`windows.h`)
- Engine headers: `Debug.h`, `Display.h`, `Win32DIMouse.h`, `WinMain.h`
