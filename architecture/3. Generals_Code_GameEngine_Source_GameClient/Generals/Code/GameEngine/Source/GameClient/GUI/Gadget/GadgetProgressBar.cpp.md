# Generals/Code/GameEngine/Source/GameClient/GUI/Gadget/GadgetProgressBar.cpp

## Purpose
Handles system messages and progress updates for a progress bar GUI gadget.

## Responsibilities
- Processes `GPM_SET_PROGRESS` messages to update progress bar position.
- Validates progress values (0-100).
- Stores progress value in window user data.
- Provides public API to send progress updates to the gadget.

## Key Types
None

## Key Functions
### GadgetProgressBarSystem
- Purpose: Handles system messages for the progress bar gadget.
- Calls: `winSetUserData`

### GadgetProgressBarSetProgress
- Purpose: Sends a progress update message to the progress bar gadget.
- Calls: `TheWindowManager->winSendSystemMsg`

## Globals
None

## Dependencies
- `GameWindow`, `WindowMsgHandledType`, `WindowMsgData` (from GameClient)
- `TheWindowManager` (global window manager instance)
- `GPM_SET_PROGRESS` (message constant)
