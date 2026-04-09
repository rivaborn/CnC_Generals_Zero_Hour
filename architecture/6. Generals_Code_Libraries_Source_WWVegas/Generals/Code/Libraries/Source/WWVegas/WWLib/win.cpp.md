# Generals/Code/Libraries/Source/WWVegas/WWLib/win.cpp

## Purpose
Handles Windows-specific initialization and error reporting for the game.

## Responsibilities
- Manages global Windows handles (HINSTANCE, HWND)
- Tracks game focus state
- Provides Win32 error message formatting (debug only)

## Key Types
None

## Key Functions
### Print_Win32Error
- Purpose: Formats and logs Win32 error messages in debug builds
- Calls: FormatMessage, WWDEBUG_SAY, LocalFree

## Globals
- ProgramInstance (HINSTANCE): Stores the application instance handle
- MainWindow (HWND): Stores the main application window handle
- GameInFocus (bool): Tracks whether the game window has focus

## Dependencies
- "always.h", "win.h", "wwdebug.h"
- Windows API: HINSTANCE, HWND, FormatMessage, LocalFree, FORMAT_MESSAGE_* flags
- WWDEBUG_SAY (external debug logging function)
