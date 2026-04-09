# Generals/Code/Tools/MapCacheBuilder/Source/WinMain.cpp

## Purpose
Entry point for the standalone MapCache Builder tool, initializing subsystems and processing command-line arguments to update map cache.

## Responsibilities
- Initialize game subsystems (file systems, data stores, audio, etc.)
- Parse command-line arguments for map paths
- Build/update map cache
- Cleanup resources on exit

## Key Types
- `SubsystemInterfaceList` (Class): Manages initialization/shutdown of game subsystems
- `NameKeyGenerator` (Class): Generates unique name keys
- `FileSystem` (Class): Abstract file system interface
- `MapCache` (Class): Handles map cache operations

## Key Functions
### `initSubsystem`
- Purpose: Register a subsystem with the subsystem list
- Calls: `_TheSubsystemList.initSubsystem`

### `strtrim`
- Purpose: Trim whitespace from a string in-place
- Calls: `strcpy`, `strlen`

### `nextParam`
- Purpose: Parse next parameter from a string using delimiters
- Calls: `strpbrk`, `strtrim`

### `WinMain`
- Purpose: Application entry point
- Calls: `DEBUG_INIT`, `initMemoryManager`, `initSubsystem`, `TheMapCache->updateCache`, `_TheSubsystemList.shutdownAll`, `shutdownMemoryManager`, `DEBUG_SHUTDOWN`

## Globals
- `ApplicationHInstance` (HINSTANCE): Application instance handle
- `ApplicationHWnd` (HWND): Dummy window handle
- `gAppPrefix` (char*): Application prefix string
- `g_strFile` (const Char*): Default string file path
- `g_csfFile` (const Char*): Default CSF file path
- `_TheSubsystemList` (SubsystemInterfaceList): Global subsystem list

## Dependencies
- Windows API (`windows.h`)
- Game framework headers (`BaseType.h`, `Debug.h`, etc.)
- Subsystem interfaces (`SubSystemInterface.h`)
- File system implementations (`Win32LocalFileSystem.h`, `Win32BIGFileSystem.h`)
- Game data stores (`Science.h`, `Weapon.h`, etc.)
- Audio system (`MilesAudioManager.h`)
