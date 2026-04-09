# Generals/Code/GameEngine/Source/Common/GameEngine.cpp

## Purpose
This file implements the Game Engine singleton, which manages initialization, updating, and execution of various subsystems in the Command & Conquer Generals game engine.

## Responsibilities
- Initialize and manage game subsystems.
- Handle game loop execution.
- Update game logic and client components.
- Manage frame rate limiting.
- Process command-line arguments.
- Convert TGA files to DDS format if necessary.

## Key Types
- None

## Key Functions
### initSubsystem
- Purpose: Initializes a subsystem with given parameters.
- Calls: `initSubsystem` method of `TheSubsystemList`.

### updateTGAtoDDS
- Purpose: Converts TGA files to DDS format if they are newer than the existing DDS files.
- Calls: `openFile`, `getFileListInDirectory`, `getFileInfo`, `write`, `close`, `system`.

### GameEngine::init
- Purpose: Initializes the game engine by setting up various subsystems and configurations.
- Calls: Multiple `initSubsystem` calls, `load`, `parseCommandLine`, `createFileSystem`, etc.

### GameEngine::update
- Purpose: Updates the game logic and client components.
- Calls: `UPDATE` methods of various subsystems like `TheRadar`, `TheAudio`, `TheGameClient`, etc.

### GameEngine::execute
- Purpose: The main loop of the game engine, which runs until the game exits.
- Calls: `update`, `Sleep`, `timeGetTime`.

## Globals
- TheGameEngine (GameEngine*): Singleton instance of the game engine.
- TheSubsystemList (SubsystemInterfaceList*): List of subsystems managed by the game engine.
- ApplicationHInstance (HINSTANCE): Handle to the application instance.
- _Module (CComModule): COM module for the application.
- DX8Wrapper_IsWindowed (bool): Indicates if the game is running in windowed mode.
- ApplicationHWnd (HWND): Handle to the main application window.
- TheSystemIsUnicode (Bool): Indicates if the system uses Unicode.

## Dependencies
- Key includes: `Common/ActionManager.h`, `Common/AudioAffect.h`, `GameLogic/GameLogic.h`, `GameClient/GameClient.h`, `GameNetwork/NetworkInterface.h`, etc.
- External symbols used: `timeBeginPeriod`, `timeEndPeriod`, `MessageBox`, `MessageBoxW`, `system`, `strstr`, etc.
