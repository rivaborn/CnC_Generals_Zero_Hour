# Generals/Code/Tools/Launcher/main.cpp

## Purpose
Launcher application for Command & Conquer Generals that applies patches before starting the game executable.

## Responsibilities
- Apply patches from the "Patches" folder before launching the game
- Handle game process creation and monitoring
- Manage configuration via launcher.cfg file
- Support optional second launcher for copy protection
- Create a primary window for UI

## Key Types
- Process (struct): Represents a process to be launched (directory, command, args)
- ConfigFile (class): Handles reading configuration from launcher.cfg
- Wstring (class): Used for string operations in config

## Key Functions
### RunGame
- Purpose: Launches the game after applying patches and handles patch updates
- Calls: Apply_Patch, Create_Process, Wait_Process, Find_Patch, Delete_Patches

### RunLauncher
- Purpose: Launches a secondary launcher process
- Calls: Create_Process

### CreatePrimaryWin
- Purpose: Creates a topmost window for the launcher UI
- Calls: RegisterClass, CreateWindowEx

### myChdir
- Purpose: Changes current directory to the specified path
- Calls: _splitpath, _makepath, _chdrive, chdir

## Globals
- UPDATE_RETVAL (const int): Special return value indicating patch check is needed
- Global_instance (HINSTANCE): Windows application instance handle
- IDI_GENERALS (int): Resource ID for the game icon

## Dependencies
- dialog.h, patch.h, findpatch.h, process.h (custom headers)
- wdebug.h, monod.h, filed.h, configfile.h (custom headers)
- Windows.h (Windows API)
- COPY_PROTECT (conditional include for Protect.h)
