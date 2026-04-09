# Generals/Code/GameEngine/Source/GameClient/GUI/Gadget/GadgetRadioButton.cpp

## Purpose
Implements radio button GUI control behavior, including selection management and input handling.

## Responsibilities
- Handles mouse/keyboard input for radio buttons
- Manages radio button group selection (only one selected per group)
- Processes system messages for radio buttons
- Provides utility functions for setting text, group, and selection state

## Key Types
- **RadioButtonData (struct)**: Stores group and screen ID for radio button
- **WinInstanceData (struct)**: Window instance state data (external)
- **GameWindow (class)**: Base window class (external)

## Key Functions
### doRadioUnselect
- Purpose: Recursively unselects radio buttons in a group excluding a specified window
- Calls: `BitTest`, `window->winGetUserData()`, `window->winGetInstanceData()`, `BitClear`, `window->winGetChild()`, `window->winGetNext()`

### unselectOtherRadioOfGroup
- Purpose: Unselects all radio buttons in a group except one specified window
- Calls: `TheWindowManager->winGetWindowList()`, `window->winGetNext()`, `doRadioUnselect`

### GadgetRadioButtonInput
- Purpose: Handles input messages for radio buttons (mouse/keyboard)
- Calls: `window->winGetInstanceData()`, `BitTest`, `BitSet`, `BitClear`, `window->winGetUserData()`, `TheWindowManager->winSendSystemMsg()`, `window->winNextTab()`, `window->winPrevTab()`

### GadgetRadioButtonSystem
- Purpose: Processes system messages for radio buttons
- Calls: `window->winGetInstanceData()`, `BitTest`, `BitSet`, `BitClear`, `window->winGetUserData()`, `TheWindowManager->winSendSystemMsg()`, `window->winSetText()`, `delete`

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
- `GameWindow`, `WinInstanceData`, `UnicodeString` (external types)
- `BitTest`, `BitSet`, `BitClear` (bit manipulation macros)
- `GWM_MOUSE
