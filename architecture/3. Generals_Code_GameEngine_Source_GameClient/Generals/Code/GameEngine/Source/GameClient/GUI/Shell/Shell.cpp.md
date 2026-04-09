# Generals/Code/GameEngine/Source/GameClient/GUI/Shell/Shell.cpp

## Purpose
Manages the shell menu system, including screen stacking, transitions, and UI layout handling.

## Responsibilities
- Manages a stack of window layouts for menu screens
- Handles screen push/pop operations with shutdown/initialization
- Manages animations and transitions between screens
- Provides access to special menu layouts (save/load, options, replay)
- Coordinates with input and game state during menu operations

## Key Types
- Shell (Class): Main shell manager singleton
- WindowLayout (Class): Represents a menu screen layout
- AnimateWindowManager (Class): Handles screen transition animations
- ShellMenuSchemeManager (Class): Manages menu appearance schemes

## Key Functions
### push
- Purpose: Initiates pushing a new menu screen onto the stack
- Calls: shutdownComplete, runShutdown

### pop
- Purpose: Initiates popping the top menu screen from the stack
- Calls: runShutdown, shutdownComplete

### update
- Purpose: Updates all active menu screens and animations
- Calls: runUpdate, update (on sub-managers)

### shutdownComplete
- Purpose: Handles completion of screen shutdown operations
- Calls: doPush, doPop, reset

### doPush/doPop
- Purpose: Actually performs the push/pop operations after shutdown
- Calls: linkScreen, unlinkScreen, runInit

## Globals
- TheShell (Shell*): The shell singleton instance

## Dependencies
- WindowLayout.h, GameWindowManager.h, ShellMenuScheme.h
- GameLogic.h, GameNetwork/GameSpyOverlay.h
- IMEManager.h, AnimateWindowManager.h
- GameWindowTransitions.h, PreRTS.h
