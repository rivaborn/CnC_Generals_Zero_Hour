# Generals/Code/GameEngine/Source/GameClient/GUI/ControlBar/ControlBarOCLTimer.cpp

## Purpose
Handles the display and updating of the On-Construction-List (OCL) timer in the control bar UI.

## Responsibilities
- Updates the OCL timer text and progress bar
- Populates the OCL timer context UI elements
- Retrieves and displays the remaining construction time
- Manages the sell button for the OCL item

## Key Types
- None

## Key Functions
### updateOCLTimerTextDisplay
- Purpose: Formats and updates the timer display text and progress bar.
- Calls: `TheNameKeyGenerator->nameToKey`, `TheWindowManager->winGetWindowFromId`, `TheGameText->fetch`, `GadgetStaticTextSetText`, `GadgetProgressBarSetProgress`

### populateOCLTimer
- Purpose: Initializes the OCL timer UI with the sell button and portrait.
- Calls: `findCommandButton`, `TheNameKeyGenerator->nameToKey`, `TheWindowManager->winGetWindowFromId`, `setControlCommand`, `win->winSetStatus`, `updateContextOCLTimer`, `setPortraitByObject`

### updateContextOCLTimer
- Purpose: Updates the OCL timer display if the remaining time has changed.
- Calls: `getObject`, `findUpdateModule`, `getRemainingFrames`, `getCountdownPercent`, `updateOCLTimerTextDisplay`

## Globals
- `m_displayedOCLTimerSeconds` (UnsignedInt): Stores the last displayed timer value to avoid redundant updates.

## Dependencies
- `PreRTS.h`, `NameKeyGenerator.h`, `ThingTemplate.h`, `Object.h`, `OCLUpdate.h`, `Drawable.h`, `GameText.h`, `ControlBar.h`, `GameWindow.h`, `GameWindowManager
