# GeneralsMD/Code/GameEngine/Source/GameClient/GUI/Shell/Shell.cpp

## Purpose
Manages the shell menu system, including screen stacking, transitions, and UI layout handling.

## Responsibilities
- Manages a stack of window layouts for menu screens
- Handles screen push/pop operations with shutdown/initialization
- Manages animations and transitions between screens
- Provides access to special menu layouts (save/load, options, replay)
- Coordinates with IME (input method editor) and GameSpy overlay

## Key Types
- Shell (Class): Main shell manager singleton
- WindowLayout (Class): Represents a menu screen layout
- AnimateWindowManager (Class): Manages screen animations
- ShellMenuSchemeManager (Class): Handles menu scheme management

## Key Functions
### push
- Purpose: Push a new menu screen onto the stack
- Calls: GameSpyCloseAllOverlays, WindowLayout::runShutdown, shutdownComplete

### pop
- Purpose: Pop the top menu screen from the stack
- Calls: GameSpyCloseAllOverlays, WindowLayout::runShutdown

### update
- Purpose: Update all active menu screens
- Calls: WindowLayout::runUpdate, AnimateWindowManager::update, ShellMenuSchemeManager::update

### shutdownComplete
- Purpose: Handle completion of screen shutdown operations
- Calls: doPush, doPop, AnimateWindowManager::reset

### showShellMap
- Purpose: Show/hide the shell map overlay
- Calls: GameMessage::MSG_CLEAR_GAME_DATA, GameMessage::MSG_NEW_GAME

## Globals
- TheShell (Shell*): The shell singleton instance

## Dependencies
- PreRTS.h, Common/RandomValue.h, GameClient/Shell.h, GameClient/WindowLayout.h
- GameClient/GameWindowManager.h, GameClient/GameWindowTransitions.h
- GameClient/IMEManager.h, GameClient/AnimateWindowManager.h
- GameClient/ShellMenuScheme.h, GameLogic/GameLogic.h
- GameNetwork/GameSpyOverlay.h, GameNetwork/GameSpy/PeerDefsImplementation.h
- <rts/profile.h>
