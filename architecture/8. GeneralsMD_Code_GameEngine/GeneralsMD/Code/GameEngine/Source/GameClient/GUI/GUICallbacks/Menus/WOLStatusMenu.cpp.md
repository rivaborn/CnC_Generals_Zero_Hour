# GeneralsMD/Code/GameEngine/Source/GameClient/GUI/GUICallbacks/Menus/WOLStatusMenu.cpp

## Purpose
Handles the WOL (Westwood Online) status menu UI, including initialization, shutdown, updates, and input handling.

## Responsibilities
- Initialize and shutdown the WOL status menu
- Handle keyboard and window system messages
- Manage menu focus and visibility
- (Commented out) Disconnect functionality via WOL API

## Key Types
- None

## Key Functions
### WOLStatusMenuInit
- Purpose: Initializes the WOL status menu, sets up window IDs and pointers.
- Calls: `TheNameKeyGenerator->nameToKey`, `TheWindowManager->winGetWindowFromId`, `layout->hide`, `TheWindowManager->winSetFocus`

### WOLStatusMenuShutdown
- Purpose: Shuts down the WOL status menu, hides the layout.
- Calls: `layout->hide`, `TheShell->shutdownComplete`

### WOLStatusMenuUpdate
- Purpose: Updates the WOL status menu (currently empty implementation).
- Calls: None

### WOLStatusMenuInput
- Purpose: Handles keyboard input for the WOL status menu (e.g., ESC key).
- Calls: `TheWindowManager->winSendSystemMsg`

### WOLStatusMenuSystem
- Purpose: Handles window system messages (e.g., focus, selection).
- Calls: None (commented-out WOL API calls)

## Globals
- `parentWOLStatusID` (NameKeyType): ID for the parent WOL status window.
- `buttonDisconnectID` (NameKeyType): ID for the disconnect button.
- `parentWOLStatus` (GameWindow*): Pointer to the parent WOL status window.
- `buttonDisconnect` (GameWindow*): Pointer to the disconnect button.
- `progressTextWindow` (GameWindow*): Pointer to the progress text window.

## Dependencies
- `PreRTS.h`, `Common/GameEngine.h`, `GameClient/WindowLayout.h`, `GameClient/Gadget.h`, `GameClient/Shell.h`, `GameClient/KeyDefs.h`, `GameClient/GameWindowManager.h`, `GameClient/GadgetListBox.h`, `GameClient/GadgetTextEntry.h`
- `TheNameKeyGenerator`, `TheWindowManager`, `TheShell` (global instances)
