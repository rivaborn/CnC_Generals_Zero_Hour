# GeneralsMD/Code/Libraries/Source/WWVegas/WWLib/win.cpp

## Purpose
Provides Windows-specific utility functions and global variables for the game engine.

## Responsibilities
- Manages global Windows handles (HINSTANCE, HWND)
- Tracks game focus state
- Provides debug error reporting for Win32 errors

## Key Types
None

## Key Functions
### Print_Win32Error
- Purpose: Formats and logs Win32 error messages in debug builds
- Calls: FormatMessage, LocalFree, WWDEBUG_SAY

## Globals
- ProgramInstance (HINSTANCE): Stores the application instance handle
- MainWindow (HWND): Stores the main window handle
- GameInFocus (bool): Tracks whether the game window has focus

## Dependencies
- always.h, win.h, wwdebug.h
- Windows API: HINSTANCE, HWND, FormatMessage, LocalFree
- WWDEBUG_SAY macro
