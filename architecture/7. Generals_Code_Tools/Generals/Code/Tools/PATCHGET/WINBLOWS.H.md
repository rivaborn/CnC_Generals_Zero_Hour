# Generals/Code/Tools/PATCHGET/WINBLOWS.H

## Purpose
Header file for Windows-specific utilities in the PATCHGET tool.

## Responsibilities
- Declares Windows API dependencies and global variables
- Provides utility function for printing window messages
- Bridges Windows-specific code with the tool's main logic

## Key Types
None

## Key Functions
### Print_WM
- Purpose: Formats and prints a Windows message (WM) for debugging.
- Calls: None

## Globals
- Global_instance (HINSTANCE): Stores the application instance handle.
- Global_commandline (LPSTR): Holds the command-line arguments.
- Global_commandshow (int): Stores the initial show state of the window.

## Dependencies
- `<windows.h>`: Core Windows API.
- `<windowsx.h>`: Extended Windows macros.
- `<stdlib.h>`: Standard C library functions.
- `wstypes.h`: Custom types for the tool.
