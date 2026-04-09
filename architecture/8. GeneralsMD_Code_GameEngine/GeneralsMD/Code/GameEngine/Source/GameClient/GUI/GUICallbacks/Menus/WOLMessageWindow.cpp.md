# GeneralsMD/Code/GameEngine/Source/GameClient/GUI/GUICallbacks/Menus/WOLMessageWindow.cpp

## Purpose
Handles the WOL (Westwood Online) message window UI in the game client.

## Responsibilities
- Initializes and shuts down the WOL message window
- Manages window input and system callbacks
- Handles keyboard input (e.g., ESC key)
- Manages window focus and selection events

## Key Types
None

## Key Functions
### WOLMessageWindowInit
- Purpose: Initializes the WOL message window and its components.
- Calls: `TheNameKeyGenerator->nameToKey`, `TheWindowManager->winGetWindowFromId`, `layout->hide`, `TheWindowManager->winSetFocus`

### WOLMessageWindowShutdown
- Purpose: Shuts down the WOL message window.
- Calls: `layout->hide`, `TheShell->shutdownComplete`

### WOLMessageWindowUpdate
- Purpose: Updates the WOL message window (currently empty implementation).
- Calls: None

### WOLMessageWindowInput
- Purpose: Handles keyboard input for the WOL message window.
- Calls: `TheWindowManager->winSendSystemMsg`

### WOLMessageWindowSystem
- Purpose: Handles system messages for the WOL message window.
- Calls: None

## Globals
- `parentWOLMessageWindowID` (NameKeyType): ID for the parent WOL message window.
- `buttonCancelID` (NameKeyType): ID for the cancel button.
- `parentWOLMessageWindow` (GameWindow*): Pointer to the parent WOL message window.
- `buttonCancel` (GameWindow*): Pointer to the cancel button.

## Dependencies
- `PreRTS.h`, `Common/GameEngine.h`, `GameClient/WindowLayout.h`, `GameClient/Gadget
