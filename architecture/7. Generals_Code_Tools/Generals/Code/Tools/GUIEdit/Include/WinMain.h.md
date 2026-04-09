# Generals/Code/Tools/GUIEdit/Include/WinMain.h

## Purpose
Header file for the GUIEdit tool's WinMain functionality, defining global handles and mouse interface.

## Responsibilities
- Declares global window and instance handles for the application
- Provides access to the Win32 mouse interface
- Defines a timer constant for window pulsing
- Includes necessary Windows and custom headers

## Key Types
None

## Key Functions
None

## Globals
- ApplicationHWnd (HWND): application main window handle
- ApplicationHInstance (HINSTANCE): application main instance handle
- TheWin32Mouse (Win32Mouse*): the mouse for win processing

## Dependencies
- `<windows.h>`: Windows API headers
- `"Win32Device/GameClient/Win32Mouse.h"`: Custom Win32 mouse interface
- `TIMER_EDIT_WINDOW_PULSE`: Timer constant for window pulsing
