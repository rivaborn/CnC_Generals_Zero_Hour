# GeneralsMD/Code/GameEngine/Source/GameClient/GUI/Gadget/GadgetRadioButton.cpp

## Purpose
Implements radio button GUI control functionality, handling selection, grouping, and input events.

## Responsibilities
- Manages radio button selection logic (mutually exclusive within groups)
- Handles mouse and keyboard input for radio buttons
- Processes system messages for radio button state changes
- Provides API for setting text, group, and selection state

## Key Types
- **RadioButtonData (struct)**: Stores group and screen ID for radio button
- **WinInstanceData (struct)**: Window instance state (not defined here)

## Key Functions
### doRadioUnselect
- Purpose: Recursively unselects radio buttons in a group excluding a specified window
- Calls: `BitTest`, `window->winGetUserData()`, `BitClear`, `window->winGetChild()`

### unselectOtherRadioOfGroup
- Purpose: Unselects all radio buttons in a group except one
- Calls: `TheWindowManager->winGetWindowList()`, `doRadioUnselect`

### GadgetRadioButtonInput
- Purpose: Handles input messages for radio buttons (mouse/keyboard)
- Calls: `BitTest`, `TheWindowManager->winSendSystemMsg()`, `unselectOtherRadioOfGroup`, `BitSet`, `window->winNextTab()`, `window->winPrevTab()`

### GadgetRadioButtonSystem
- Purpose: Processes system messages for radio buttons
- Calls: `BitTest`, `TheWindowManager->winSendSystemMsg()`, `window->winSetText()`, `delete`, `BitClear`

### GadgetRadioSetText
- Purpose: Sets the text label for a radio button
- Calls: `TheWindowManager->winSendSystemMsg()`

### GadgetRadioSetGroup
- Purpose: Sets the group and screen ID for a radio button
- Calls: `window->winGetUserData()`

### GadgetRadioSetSelection
- Purpose: Sets the selection state of a radio button
- Calls: `TheWindowManager->winSendSystemMsg()`

## Globals
- **TheWindowManager (GameWindowManager**)**: Global window manager instance

## Dependencies
- `PreRTS.h`, `Language.h`, `GameWindowManager.h`, `Gadget.h`
- `GameWindow`, `WinInstanceData`, `UnicodeString` types
- `BitTest`, `BitSet`, `BitClear` macros
- `MSG_HANDLED`, `MSG_IGNORED` constants
