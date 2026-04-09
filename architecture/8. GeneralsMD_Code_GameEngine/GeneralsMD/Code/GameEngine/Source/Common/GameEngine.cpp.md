# GeneralsMD/Code/GameEngine/Source/Common/GameEngine.cpp

## Purpose
Core game engine singleton implementation managing initialization, updates, and shutdown of subsystems.

## Responsibilities
- Manages game engine lifecycle (init/update/execute/shutdown)
- Initializes subsystems (file systems, audio, networking, etc.)
- Handles frame rate limiting and game loop
- Manages TGA-to-DDS texture conversion
- Coordinates message stream and game state

## Key Types
- `GameEngine` (Class): Main engine singleton
- `SubsystemInterfaceList` (Class): Manages subsystem initialization/reset
- `DeepCRCSanityCheck` (Class): CRC verification subsystem (DEBUG only)

## Key Functions
### `init(int argc, char *argv[])`
- Purpose: Initializes all game subsystems and loads configuration
- Calls: `initSubsystem`, `updateTGAtoDDS`, `parseCommandLine`, subsystem inits

### `update()`
- Purpose: Main game loop update processing
- Calls: `TheRadar->UPDATE`, `TheAudio->UPDATE`, `TheGameClient->UPDATE`, `TheGameLogic->UPDATE`

### `execute()`
- Purpose: Main game execution loop with frame rate control
- Calls: `update()`, `PerfGather` methods, `TheTacticalView` methods

### `updateTGAtoDDS()`
- Purpose: Converts outdated TGA textures to DDS format
- Calls: `TheLocalFileSystem` methods, `system()`

## Globals
- `TheGameEngine` (GameEngine*): Main engine singleton instance
- `TheSubsystemList` (SubsystemInterfaceList*): Subsystem manager
- `ApplicationHInstance` (HINSTANCE): Application instance handle
- `DX8Wrapper_IsWindowed` (bool): Windowed mode flag
- `TheSystemIsUnicode` (Bool): Unicode system detection

## Dependencies
- Game subsystems: `GameLogic`, `GameClient`, `Audio`, `Network`
- File systems: `LocalFileSystem`, `ArchiveFileSystem`
- Configuration: `INI`, `GlobalData`, `CommandLine`
- Utilities: `MessageStream`, `PerfTimer`, `Debug`
- External: Windows API, DirectX wrappers
