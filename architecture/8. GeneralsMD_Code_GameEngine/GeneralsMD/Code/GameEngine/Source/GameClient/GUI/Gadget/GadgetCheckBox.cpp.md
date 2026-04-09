# GeneralsMD/Code/GameEngine/Source/GameClient/GUI/Gadget/GadgetCheckBox.cpp

## Purpose
Implements a checkbox GUI control for the game's window system.

## Responsibilities
- Handles mouse and keyboard input for checkboxes
- Manages checkbox state (checked/unchecked)
- Processes system messages for checkboxes
- Provides public API for setting/checking toggle state

## Key Types
- None

## Key Functions
### GadgetCheckBoxInput
- Purpose: Handles input messages for checkboxes
- Calls: TheWindowManager->winSendSystemMsg, TheWindowManager->winNextTab, TheWindowManager->winPrevTab

### GadgetCheckBoxSystem
- Purpose: Processes system messages for checkboxes
- Calls: TheWindowManager->winSendSystemMsg, window->winSetText

### GadgetCheckBoxSetText
- Purpose: Sets the text label for a checkbox
- Calls: TheWindowManager->winSendSystemMsg

### GadgetCheckBoxSetChecked
- Purpose: Sets the checkbox state to checked or unchecked
- Calls: TheWindowManager->winSendSystemMsg

### GadgetCheckBoxToggle
- Purpose: Toggles the checkbox state
- Calls: TheWindowManager->winSendSystemMsg

### GadgetCheckBoxIsChecked
- Purpose: Returns whether the checkbox is checked
- Calls: None

## Globals
- None

## Dependencies
- GameClient/Gadget.h
- GameClient/GameWindowManager.h
- GameClient/Keyboard.h
- Common/Language.h
- PreRTS.h
