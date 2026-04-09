# Generals/Code/GameEngine/Source/GameClient/GUI/GUICallbacks/Menus/PopupCommunicator.cpp

## Purpose
Handles the Electronic Arts instant messaging popup window in the game UI.

## Responsibilities
- Initializes and shuts down the popup communicator UI
- Manages keyboard input for the popup (e.g., ESC key handling)
- Processes window system messages (create, destroy, focus, selection)
- Destroys the popup when the OK button is clicked

## Key Types
- None

## Key Functions
### PopupCommunicatorInit
- Purpose: Initializes the popup communicator window and its controls
- Calls: TheNameKeyGenerator->nameToKey, TheWindowManager->winGetWindowFromId, TheWindowManager->winSetFocus, TheWindowManager->winSetModal

### PopupCommunicatorShutdown
- Purpose: Shuts down the popup communicator (currently empty implementation)
- Calls: None

### PopupcommunicatorUpdate
- Purpose: Updates the popup communicator state (currently empty implementation)
- Calls: None

### PopupCommunicatorInput
- Purpose: Handles keyboard input for the popup communicator
- Calls: TheWindowManager->winSendSystemMsg

### PopupCommunicatorSystem
- Purpose: Processes system messages for the popup communicator window
- Calls: WindowLayout->destroyWindows, WindowLayout->deleteInstance

## Globals
- buttonOkID (NameKeyType): Stores the ID of the OK button
- buttonOk (GameWindow*): Pointer to the OK button window
- parent (GameWindow*): Pointer to the parent popup window

## Dependencies
- GameClient/GUICallbacks.h
- GameClient/GameWindowManager.h
- PreRTS.h
- Uses TheNameKeyGenerator, TheWindowManager, WindowLayout, GameWindow classes
