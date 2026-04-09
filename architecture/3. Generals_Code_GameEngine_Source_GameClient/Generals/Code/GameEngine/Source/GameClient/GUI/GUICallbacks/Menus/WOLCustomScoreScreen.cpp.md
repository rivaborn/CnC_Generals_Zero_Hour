# Generals/Code/GameEngine/Source/GameClient/GUI/GUICallbacks/Menus/WOLCustomScoreScreen.cpp

## Purpose
Handles the custom match score screen UI in the Westwood Online (WOL) lobby system.

## Responsibilities
- Initializes and shuts down the score screen UI
- Manages user input (keyboard/mouse) for the screen
- Handles window system messages for the UI
- Manages focus and visibility of UI elements

## Key Types
- None (procedural code with global functions)

## Key Functions
### WOLCustomScoreScreenInit
- Purpose: Initializes UI elements and window IDs for the score screen
- Calls: TheNameKeyGenerator->nameToKey, TheWindowManager->winGetWindowFromId, layout->hide, TheWindowManager->winSetFocus

### WOLCustomScoreScreenShutdown
- Purpose: Cleans up and hides the score screen UI
- Calls: layout->hide, TheShell->shutdownComplete

### WOLCustomScoreScreenUpdate
- Purpose: Updates the score screen state (currently empty implementation)
- Calls: None

### WOLCustomScoreScreenInput
- Purpose: Handles keyboard input for the score screen
- Calls: TheWindowManager->winSendSystemMsg

### WOLCustomScoreScreenSystem
- Purpose: Handles system messages for the score screen windows
- Calls: None

## Globals
- parentWOLCustomScoreID (NameKeyType): ID for the parent window
- buttonDisconnectID (NameKeyType): ID for the disconnect button
- buttonLobbyID (NameKeyType): ID for the lobby button
- parentWOLCustomScore (GameWindow*): Pointer to the parent window
- buttonDisconnect (GameWindow*): Pointer to the disconnect button
- buttonLobby (GameWindow*): Pointer to the lobby button

## Dependencies
- PreRTS.h, BaseType.h, GameEngine.h, NameKeyGenerator.h, WindowLayout.h, Gadget.h, Shell.h, KeyDefs.h, GameWindowManager.h, GadgetListBox.h, GadgetTextEntry.h, GlobalData.h
- TheNameKeyGenerator, TheWindowManager, TheShell (external symbols)
