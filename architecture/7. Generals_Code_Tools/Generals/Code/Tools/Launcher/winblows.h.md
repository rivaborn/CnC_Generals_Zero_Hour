# Generals/Code/Tools/Launcher/winblows.h

## Purpose
Header file for Windows-specific launcher functionality in the Generals/Zero Hour toolchain.

## Responsibilities
- Declares Windows API dependencies and global launcher state
- Provides message printing utility for Windows messages
- Bridges Windows-specific code with the main launcher logic

## Key Types
- None

## Key Functions
### main
- Purpose: Entry point for the launcher application.
- Calls: Not inferable (implementation in another file).

### Print_WM
- Purpose: Formats and prints Windows message information.
- Calls: Not inferable (implementation in another file).

## Globals
- Global_instance (HINSTANCE): Stores the application instance handle.
- Global_commandline (LPSTR): Holds the command-line arguments.
- Global_commandshow (int): Stores the initial show state of the window.

## Dependencies
- `<windows.h>`: Core Windows API.
- `<windowsx.h>`: Extended Windows macros.
- `<stdlib.h>`: Standard C library.
- `wstypes.h`: Custom types header (likely defines platform-specific types).
