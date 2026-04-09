# Generals/Code/Tools/WW3D/pluglib/win.h

## Purpose
Header file for Windows-specific declarations and global variables used in the WW3D plugin library.

## Responsibilities
- Includes Windows headers with warning suppression
- Declares global application state variables
- Provides debug-only error printing function
- Defines platform-specific includes for non-Windows builds

## Key Types
None

## Key Functions
### Print_Win32Error
- Purpose: Debug-only function to print Windows error messages
- Calls: None

## Globals
- ProgramInstance (HINSTANCE): Stores the application instance handle
- MainWindow (HWND): Stores the main application window handle
- GameInFocus (bool): Tracks whether the game window has focus

## Dependencies
- `<windows.h>`: Core Windows API
- `<unistd.h>`: Unix API for non-Windows builds
- `_WINDOWS` macro: Controls platform-specific code paths
