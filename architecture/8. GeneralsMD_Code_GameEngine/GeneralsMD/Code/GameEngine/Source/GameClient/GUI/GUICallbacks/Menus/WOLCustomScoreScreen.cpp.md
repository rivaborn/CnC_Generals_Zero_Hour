# GeneralsMD/Code/GameEngine/Source/GameClient/GUI/GUICallbacks/Menus/WOLCustomScoreScreen.cpp

## Purpose
Handles the custom match score screen UI in Westwood Online (WOL) mode, including initialization, input handling, and system callbacks.

## Responsibilities
- Initializes and shuts down the WOL custom score screen
- Manages keyboard and window input for the score screen
- Handles system messages for the score screen window
- Maintains references to UI elements (buttons, parent window)

## Key Types
- **None**: File contains only functions and global variables

## Key Functions
### WOLCustomScoreScreenInit
- Purpose: Initializes the WOL custom score screen UI elements and sets focus
- Calls: `TheNameKeyGenerator->nameToKey`, `TheWindowManager->winGetWindowFromId`, `layout->hide`, `TheWindowManager->winSetFocus`

### WOLCustomScoreScreenShutdown
- Purpose: Shuts down the WOL custom score screen and notifies shell of completion
- Calls: `layout->hide`, `TheShell->shutdownComplete`

### WOLCustomScoreScreenUpdate
- Purpose: Updates the WOL custom score screen state (currently empty implementation)
- Calls: None

### WOLCustomScoreScreenInput
- Purpose: Handles keyboard input for the score screen (ESC key for disconnect)
- Calls: `TheWindowManager->winSendSystemMsg`

### WOLCustomScoreScreenSystem
- Purpose: Handles system messages for the score screen window (focus, selection events)
- Calls: None

## Globals
- **parentWOLCustomScoreID** (NameKeyType): ID for the parent score screen window
- **buttonDisconnectID** (NameKeyType): ID for the disconnect button
- **buttonLobbyID** (NameKeyType): ID for the lobby button
- **parentWOLCustomScore** (GameWindow*): Pointer to the parent score screen window
- **buttonDisconnect** (GameWindow*): Pointer to the disconnect button
- **buttonLobby** (GameWindow*): Pointer to the lobby button

## Dependencies
- Key includes: `PreRTS.h`, `BaseType.h`, `GameEngine.h`, `NameKeyGenerator.h`, `WindowLayout.h`, `Gadget.h`, `Shell.h`, `KeyDefs.h`, `GameWindowManager.h`, `GadgetListBox.h`, `GadgetTextEntry.h`, `GlobalData.h`
- External symbols: `TheNameKeyGenerator`, `TheWindowManager`, `TheShell`
