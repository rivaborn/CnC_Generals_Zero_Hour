# GeneralsMD/Code/GameEngine/Source/GameClient/GUI/ControlBar/ControlBarOCLTimer.cpp

## Purpose
Handles the display and updating of the On-Construction-List (OCL) timer in the control bar UI.

## Responsibilities
- Updates timer text and progress bar for OCL objects
- Populates the OCL timer context UI with appropriate buttons
- Manages sell/rally point button visibility based on object type
- Displays object portraits and rally points
- Syncs timer display with OCL update module data

## Key Types
- `ControlBar` (Class): Manages control bar UI elements and contexts
- `OCLUpdate` (Class): Module providing OCL timer data (external)

## Key Functions
### `updateOCLTimerTextDisplay`
- Purpose: Formats and updates the timer text and progress bar.
- Calls: `GadgetStaticTextSetText`, `GadgetProgressBarSetProgress`, `TheGameText->fetch`

### `populateOCLTimer`
- Purpose: Configures the OCL timer UI context for a given object.
- Calls: `findCommandButton`, `setControlCommand`, `showRallyPoint`, `setPortraitByObject`, `updateContextOCLTimer`

### `updateContextOCLTimer`
- Purpose: Updates the OCL timer display based on current object state.
- Calls: `findUpdateModule`, `updateOCLTimerTextDisplay`

## Globals
- `m_displayedOCLTimerSeconds` (UnsignedInt): Tracks last displayed timer value

## Dependencies
- `PreRTS.h`, `NameKeyGenerator.h`, `ThingTemplate.h`, `Object.h`, `OCLUpdate.h`, `Drawable.h`, `GameText.h`, `ControlBar.h`, `GameWindow.h`, `GameWindowManager.h`, `GadgetStaticText.h`, `Gad
