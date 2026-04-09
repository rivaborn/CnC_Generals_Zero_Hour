# GeneralsMD/Code/GameEngineDevice/Source/Win32Device/Common/Win32GameEngine.cpp

## Purpose
Implements the Win32-specific game engine class, handling Windows message processing and game loop updates.

## Responsibilities
- Manages Windows message pump and OS service calls
- Handles game engine initialization and reset
- Processes Windows messages during game updates
- Manages audio focus when alt-tabbing
- Controls game loop behavior during minimization

## Key Types
- Win32GameEngine (Class): Main game engine class for Win32 platform
- None (other types)

## Key Functions
### Win32GameEngine::Win32GameEngine()
- Purpose: Constructor that sets error mode to prevent blue screens
- Calls: SetErrorMode()

### Win32GameEngine::init()
- Purpose: Initializes the game engine by calling parent class init
- Calls: GameEngine::init()

### Win32GameEngine::update()
- Purpose: Updates game engine state and handles Windows message processing
- Calls: GameEngine::update(), serviceWindowsOS(), TheLAN->setIsActive(), TheLAN->update(), TheAudio->setVolume()

### Win32GameEngine::serviceWindowsOS()
- Purpose: Processes Windows messages to prevent OS service backups
- Calls: PeekMessage(), GetMessage(), TranslateMessage(), DispatchMessage()

## Globals
- TheMessageTime (DWORD): Stores timestamp of last processed Windows message

## Dependencies
- windows.h: Windows API headers
- Win32Device/Common/Win32GameEngine.h: Header for this class
- Common/PerfTimer.h: Performance timing utilities
- GameNetwork/LANAPICallbacks.h: LAN networking callbacks
- GameEngine, GameClient, GameLogic singletons
- TheLAN, TheAudio, TheGameEngine, TheGameLogic global objects
- Application
