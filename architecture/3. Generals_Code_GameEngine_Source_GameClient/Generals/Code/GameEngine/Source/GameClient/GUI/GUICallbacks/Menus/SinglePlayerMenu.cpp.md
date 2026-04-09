# Generals/Code/GameEngine/Source/GameClient/GUI/GUICallbacks/Menus/SinglePlayerMenu.cpp

## Purpose
Handles initialization, input, and system callbacks for the single-player menu in the game.

## Responsibilities
- Manages menu initialization and shutdown
- Handles keyboard and button input for menu navigation
- Controls menu animations and transitions
- Registers menu elements with the animation manager
- Processes window system messages for menu controls

## Key Types
- None

## Key Functions
### shutdownComplete
- Purpose: Finalizes menu shutdown by hiding the layout and notifying the shell.
- Calls: `layout->hide`, `TheShell->shutdownComplete`

### SinglePlayerMenuInit
- Purpose: Initializes the single-player menu, showing it and setting up animations.
- Calls: `TheShell->showShellMap`, `layout->hide`, `TheNameKeyGenerator->nameToKey`, `TheWindowManager->winGetWindowFromId`, `TheWindowManager->winSetFocus`, `TheShell->registerWithAnimateManager`

### SinglePlayerMenuShutdown
- Purpose: Handles menu shutdown, including animation reversal or immediate shutdown.
- Calls: `TheShell->reverseAnimatewindow`, `shutdownComplete`

### SinglePlayerMenuUpdate
- Purpose: Updates the menu state, checking if shutdown animations are complete.
- Calls: `TheShell->isAnimFinished`, `shutdownComplete`

### SinglePlayerMenuInput
- Purpose: Processes keyboard input for the menu, handling ESC key for back button simulation.
- Calls: `TheNameKeyGenerator->nameToKey`, `TheWindowManager->winGetWindowFromId`, `TheWindowManager->winSendSystemMsg`

### SinglePlayerMenuSystem
- Purpose: Handles system messages for the menu, including control selection and focus management.
- Calls: `TheNameKeyGenerator->nameToKey`, `TheShell->push`, `TheShell->pop`

## Globals
- `isShuttingDown` (Bool): Tracks if the menu is shutting down.
- `buttonPushed` (Bool): Prevents multiple button presses during transitions.

## Dependencies
- `PreRTS.h`, `Common/GameEngine.h`, `GameClient/AnimateWindowManager.h`, `GameClient/WindowLayout.h`, `GameClient/Gadget.h`, `GameClient/Shell.h`, `GameClient/KeyDefs.h`, `GameClient/GameWindowManager.h`
- `TheShell`, `TheNameKeyGenerator`, `TheWindowManager`
