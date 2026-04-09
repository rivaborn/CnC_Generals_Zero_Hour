# Generals/Code/Tools/ImagePacker/Source/WinMain.cpp

## Purpose
Entry point for the ImagePacker tool, initializing the application and managing the main dialog.

## Responsibilities
- Initialize debugging and memory management
- Create and initialize the ImagePacker instance
- Load and display the main dialog
- Clean up resources on exit

## Key Types
- None

## Key Functions
### WinMain
- Purpose: Application entry point that initializes the ImagePacker tool and runs the main dialog.
- Calls: `DEBUG_INIT`, `initMemoryManager`, `new ImagePacker`, `TheImagePacker->init`, `DialogBox`, `delete TheImagePacker`, `shutdownMemoryManager`, `DEBUG_SHUTDOWN`

## Globals
- ApplicationHInstance (HINSTANCE): Stores the application instance handle.
- ApplicationHWnd (HWND): Placeholder window handle to satisfy linked game libraries.
- g_strFile (const Char*): Path to the Generals.str file.
- g_csfFile (const Char*): Path template for Generals.csf file.

## Dependencies
- `<windows.h>`: Windows API functions and types.
- `<stdlib.h>`: Standard library functions.
- `Lib/BaseType.h`: Base type definitions.
- `Common/GameMemory.h`: Memory management utilities.
- `Common/Debug.h`: Debugging utilities.
- `ImagePacker.h`: ImagePacker class definition.
- `Resource.h`: Resource IDs.
- `WindowProc.h`: Window procedure for the dialog.
