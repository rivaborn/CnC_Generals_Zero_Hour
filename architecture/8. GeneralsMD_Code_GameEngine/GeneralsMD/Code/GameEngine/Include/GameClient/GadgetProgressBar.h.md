# GeneralsMD/Code/GameEngine/Include/GameClient/GadgetProgressBar.h

## Purpose
Header file providing helper functions for manipulating progress bar gadgets in the game UI.

## Responsibilities
- Defines inline functions for setting/getting progress bar properties
- Handles enabled/disabled/highlight states
- Manages color, border, and image attributes

## Key Types
None

## Key Functions
### GadgetProgressBarSetProgress
- Purpose: Sets the progress value of a progress bar
- Calls: None (direct GameWindow method call)

### GadgetProgressBarSetEnabledColor
- Purpose: Sets the enabled state color
- Calls: g->winSetEnabledColor

### GadgetProgressBarSetDisabledColor
- Purpose: Sets the disabled state color
- Calls: g->winSetDisabledColor

### GadgetProgressBarSetHiliteColor
- Purpose: Sets the highlight state color
- Calls: g->winSetHiliteColor

## Globals
None

## Dependencies
- GameClient/GameWindow.h
- Uses GameWindow class methods (winSetEnabledColor, winGetEnabledColor, etc.)
- Uses Color and Image types (not defined here)
