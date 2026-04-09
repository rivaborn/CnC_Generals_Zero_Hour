# GeneralsMD/Code/GameEngine/Source/GameClient/GUI/GUICallbacks/Menus/PopupCommunicator.cpp

## Purpose
Handles the Electronic Arts instant messaging system popup communicator UI in the game client.

## Responsibilities
- Initializes and shuts down the popup communicator window
- Manages keyboard input for the popup (e.g., ESC key handling)
- Processes window system messages (CREATE, DESTROY, INPUT_FOCUS, SELECTED)
- Destroys the popup when the OK button is selected

## Key Types
None

## Key Functions
### PopupCommunicatorInit
- Purpose: Initializes the popup communicator window and sets keyboard focus
- Calls: TheNameKeyGenerator->nameToKey, TheWindowManager->winGetWindowFromId, TheWindowManager->winSetFocus, TheWindowManager->winSetModal

### PopupCommunicatorShutdown
- Purpose: Shuts down the popup communicator (currently empty implementation)
- Calls: None

### PopupcommunicatorUpdate
- Purpose: Updates the popup communicator (currently empty implementation)
- Calls: None

### PopupCommunicatorInput
- Purpose: Handles keyboard input for the popup communicator
- Calls: TheWindowManager->winSendSystemMsg

### PopupCommunicatorSystem
- Purpose: Processes window system messages for the popup communicator
- Calls: window->winGetLayout, popupCommunicatorLayout->destroyWindows, popupCommunicatorLayout->deleteInstance

## Globals
- buttonOkID (NameKeyType): Stores the ID of the OK button
- buttonOk (GameWindow*): Pointer to the OK button window
- parent (GameWindow*): Pointer to the parent popup window

## Dependencies
- GameClient/GUICallbacks.h
- GameClient/GameWindowManager.h
- PreRTS.h
- TheNameKeyGenerator, TheWindowManager (external symbols)
