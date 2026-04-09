# Generals/Code/Libraries/Source/WWVegas/WWLib/win.h

## Purpose
Header file that includes Windows API headers and defines global variables for the game's window and instance handles.

## Responsibilities
- Includes Windows headers with warning suppression
- Defines global window and instance handles
- Provides debug error printing for Win32 errors

## Key Types
None

## Key Functions
### Print_Win32Error
- Purpose: Prints Win32 error messages in debug builds
- Calls: Not inferable

## Globals
- ProgramInstance (HINSTANCE): Stores the application instance handle
- MainWindow (HWND): Stores the main window handle
- GameInFocus (bool): Tracks whether the game window has focus

## Dependencies
- `<windows.h>`: Core Windows API
- `_DEBUG` macro: Controls debug functionality
- `HINSTANCE`, `HWND`: Windows handle types
