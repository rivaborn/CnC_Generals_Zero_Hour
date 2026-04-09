# Generals/Code/GameEngineDevice/Source/Win32Device/Common/Win32GameEngine.cpp

## Purpose
Implements the Win32-specific game engine class, handling Windows message processing and game loop integration.

## Responsibilities
- Manages Windows message pump and OS service calls
- Extends base GameEngine functionality for Win32
- Handles window minimization/alt-tab behavior in multiplayer
- Maintains error mode settings during engine lifetime

## Key Types
- Win32GameEngine (Class): Win32-specific game engine implementation
- None

## Key Functions
### Win32GameEngine()
- Purpose: Constructor that sets error mode to prevent blue screens
- Calls: SetErrorMode()

### ~Win32GameEngine()
- Purpose: Destructor that restores previous error mode
- Calls: SetErrorMode()

### init()
- Purpose: Initializes the Win32 game engine
- Calls: GameEngine::init()

### reset()
- Purpose: Resets the Win32 game engine
- Calls: GameEngine::reset()

### update()
- Purpose: Updates game engine and handles Windows message processing
- Calls: GameEngine::update(), IsIconic(), Sleep(), serviceWindowsOS(), TheLAN->setIsActive(), TheLAN->update(), TheGameEngine->getQuitting(), TheGameLogic->isInInternetGame(), TheGameLogic->isInLanGame()

### serviceWindowsOS()
- Purpose: Processes Windows messages to prevent OS service backup
- Calls: PeekMessage(), GetMessage(), TranslateMessage(), DispatchMessage()

## Globals
- TheMessageTime (DWORD): Stores timestamp of last processed Windows message

## Dependencies
- windows.h: Windows API headers
- Win32GameEngine.h: Header for this class
- PerfTimer.h: Performance timing utilities
- LANAPICallbacks.h: LAN
