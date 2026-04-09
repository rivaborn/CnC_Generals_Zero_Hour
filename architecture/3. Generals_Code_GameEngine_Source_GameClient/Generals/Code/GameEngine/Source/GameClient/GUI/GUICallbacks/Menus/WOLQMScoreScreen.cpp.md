# Generals/Code/GameEngine/Source/GameClient/GUI/GUICallbacks/Menus/WOLQMScoreScreen.cpp

## Purpose
Handles the QuickMatch score screen UI, including initialization, input handling, and system callbacks.

## Responsibilities
- Manages score screen window layout and controls
- Handles user input (keyboard and button clicks)
- Processes system messages for the score screen
- Initializes and shuts down the score screen UI

## Key Types
- None

## Key Functions
### WOLQMScoreScreenInit
- Purpose: Initializes the score screen UI and sets up window references
- Calls: TheNameKeyGenerator->nameToKey, TheWindowManager->winGetWindowFromId, layout->hide, TheWindowManager->winSetFocus

### WOLQMScoreScreenShutdown
- Purpose: Shuts down the score screen UI
- Calls: layout->hide, TheShell->shutdownComplete

### WOLQMScoreScreenUpdate
- Purpose: Updates the score screen state (currently empty implementation)
- Calls: None

### WOLQMScoreScreenInput
- Purpose: Handles keyboard input for the score screen
- Calls: TheWindowManager->winSendSystemMsg

### WOLQMScoreScreenSystem
- Purpose: Processes system messages for the score screen
- Calls: None

## Globals
- parentWOLQMScoreID (NameKeyType): ID for the parent score screen window
- buttonDisconnectID (NameKeyType): ID for the disconnect button
- buttonQuickmatchID (NameKeyType): ID for the quickmatch button
- parentWOLQMScore (GameWindow*): Pointer to the parent score screen window
- buttonDisconnect (GameWindow*): Pointer to the disconnect button
- buttonQuickmatch (GameWindow*): Pointer to the quickmatch button

## Dependencies
- PreRTS.h, Common/GameEngine.h, GameClient/WindowLayout.h, GameClient/Gadget.h, GameClient/Shell.h, GameClient/KeyDefs.h, GameClient/GameWindowManager.h, GameClient/GadgetListBox.h, GameClient/GadgetTextEntry.h
