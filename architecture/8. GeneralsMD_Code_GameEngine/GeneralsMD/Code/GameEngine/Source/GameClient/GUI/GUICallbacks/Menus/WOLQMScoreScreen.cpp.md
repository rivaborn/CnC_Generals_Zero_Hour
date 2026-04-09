# GeneralsMD/Code/GameEngine/Source/GameClient/GUI/GUICallbacks/Menus/WOLQMScoreScreen.cpp

## Purpose
Handles the QuickMatch score screen UI in the Westwood Online (WOL) integration, including initialization, input handling, and system callbacks.

## Responsibilities
- Manages WOL QuickMatch score screen lifecycle (init/shutdown)
- Handles keyboard/input events for the score screen
- Processes window system messages (focus, selection)
- Maintains references to UI elements (parent window, buttons)

## Key Types
- None (procedural file with global functions)

## Key Functions
### WOLQMScoreScreenInit
- Purpose: Initializes the score screen UI elements and layout
- Calls: TheNameKeyGenerator->nameToKey, TheWindowManager->winGetWindowFromId, layout->hide, TheWindowManager->winSetFocus

### WOLQMScoreScreenShutdown
- Purpose: Cleans up and hides the score screen
- Calls: layout->hide, TheShell->shutdownComplete

### WOLQMScoreScreenUpdate
- Purpose: Updates the score screen state (currently empty implementation)
- Calls: None

### WOLQMScoreScreenInput
- Purpose: Handles keyboard input for the score screen
- Calls: TheWindowManager->winSendSystemMsg

### WOLQMScoreScreenSystem
- Purpose: Processes window system messages (focus, selection, etc.)
- Calls: None (commented-out WOL calls)

## Globals
- parentWOLQMScoreID (NameKeyType): ID for the parent window
- buttonDisconnectID (NameKeyType): ID for disconnect button
- buttonQuickmatchID (NameKeyType): ID for QuickMatch button
- parentWOLQMScore (GameWindow*): Pointer to parent window
- buttonDisconnect (GameWindow*): Pointer to disconnect button
- buttonQuickmatch (GameWindow*): Pointer to QuickMatch button

## Dependencies
- GameEngine.h, WindowLayout.h, Gadget.h, Shell.h, KeyDefs.h, GameWindowManager.h
- Uses TheNameKeyGenerator, TheWindowManager, TheShell global instances
- Commented references to WOL (Westwood Online) API (WOL.h/WOLmenus.h)
