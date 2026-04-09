# GeneralsMD/Code/GameEngine/Source/GameClient/GUI/Gadget/GadgetProgressBar.cpp

## Purpose
Handles system messages and progress updates for a progress bar GUI gadget.

## Responsibilities
- Processes `GPM_SET_PROGRESS` messages to update progress bar position.
- Validates progress values (0-100).
- Stores progress value in window user data.
- Provides public API to send progress updates to a progress bar window.

## Key Types
None

## Key Functions
### GadgetProgressBarSystem
- Purpose: Handles system messages for the progress bar gadget.
- Calls: `winSetUserData`

### GadgetProgressBarSetProgress
- Purpose: Sends a progress update message to a progress bar window.
- Calls: `TheWindowManager->winSendSystemMsg`

## Globals
None

## Dependencies
- `GameWindow`, `WindowMsgHandledType`, `WindowMsgData`, `UnsignedInt`, `Int`
- `GPM_SET_PROGRESS` (message constant)
- `TheWindowManager` (global window manager instance)
- `winSetUserData`, `winSendSystemMsg` (window management functions)
