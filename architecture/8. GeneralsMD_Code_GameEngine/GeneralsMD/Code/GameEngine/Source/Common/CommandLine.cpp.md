# GeneralsMD/Code/GameEngine/Source/Common/CommandLine.cpp

## Purpose
Handles parsing command-line arguments for the game, modifying runtime behavior via global settings.

## Responsibilities
- Registers command-line flags and their handlers
- Validates and processes map paths
- Modifies game settings (audio, video, shadows, etc.)
- Supports debug/build-time options (CRC, stats, etc.)

## Key Types
- **FuncPtr (Class)**: Function pointer type for command-line handlers.
- **CommandLineParam (Struct)**: Maps flag names to handler functions.
- **None** for other types.

## Key Functions
### parseNoLogOrCrash
- Purpose: Handles `-NoLogOrCrash` flag (no-op in release builds).
- Calls: `DEBUG_CRASH`

### parseWin
- Purpose: Enables windowed mode.
- Calls: `TheWritableGlobalData->m_windowed = true`

### parseNoAudio
- Purpose: Disables all audio subsystems.
- Calls: Modifies `TheWritableGlobalData` audio flags.

### parseMod
- Purpose: Loads a mod from a path (file or directory).
- Calls: `TheLocalFileSystem->doesFileExist`, `_stat`

### parseCommandLine
- Purpose: Main entry point; iterates args and dispatches to handlers.
- Calls: `DEBUG_LOG`, `params[param].func`, `TheArchiveFileSystem->loadMods`

## Globals
- **TheDebugIgnoreSyncErrors (Bool)**: Controls sync error handling.
- **DX8Wrapper_PreserveFPU (Int)**: FPU state preservation flag.
- **F_NOCASE (UnsignedByte)**: Case-insensitivity flag.
- **params (CommandLineParam[])**: Array of flag-handler pairs.

## Dependencies
- **Includes**: `PreRTS.h`, `CommandLine.h`, `ArchiveFileSystem.h`, `LocalFileSystem.h`, `Version.h`, `TerrainVisual.h`, `GameText.h`
- **Externals**: `TheWritableGlobalData`, `TheGlobalData`, `TheLocalFileSystem`, `TheArchiveFileSystem`, `TheVersion`, `DebugSetFlags`, `DEBUG_LOG`, `DEBUG_CRASH`
