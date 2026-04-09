# GeneralsMD/Code/Libraries/Source/WWVegas/WWLib/win.h

## Purpose
Header file that includes Windows API headers and defines global variables for the game's window and instance handles.

## Responsibilities
- Includes Windows headers with warning suppression
- Defines global window and instance handles
- Provides debug-only error printing function

## Key Types
None

## Key Functions
### Print_Win32Error
- Purpose: Prints Windows API error messages (debug only)
- Calls: Not inferable

## Globals
- ProgramInstance (HINSTANCE): Stores the application instance handle
- MainWindow (HWND): Stores the main game window handle
- GameInFocus (bool): Tracks whether the game window has focus

## Dependencies
- `<windows.h>`: Core Windows API
- `_DEBUG` macro: Controls error printing availability
