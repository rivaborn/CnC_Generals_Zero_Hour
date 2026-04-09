# GeneralsMD/Code/GameEngine/Include/GameClient/GadgetRadioButton.h

## Purpose
Header file providing helper functions for configuring radio button gadgets in the game UI.

## Responsibilities
- Defines inline functions for setting/getting radio button visual states (enabled/disabled/highlighted)
- Manages radio button text and selection state
- Handles radio button grouping for mutual exclusivity

## Key Types
- None

## Key Functions
### GadgetRadioSetText
- Purpose: Sets the text for a radio button gadget.
- Calls: Not inferable

### GadgetRadioSetSelection
- Purpose: Sets the selection state of a radio button.
- Calls: Not inferable

### GadgetRadioSetGroup
- Purpose: Assigns a radio button to a group for mutual exclusivity.
- Calls: Not inferable

### GadgetRadioSetEnabledImage / GadgetRadioSetEnabledColor / GadgetRadioSetEnabledBorderColor
- Purpose: Configures visual appearance when radio button is enabled.
- Calls: `g->winSetEnabledImage/Color/BorderColor`

### GadgetRadioSetDisabledImage / GadgetRadioSetDisabledColor / GadgetRadioSetDisabledBorderColor
- Purpose: Configures visual appearance when radio button is disabled.
- Calls: `g->winSetDisabledImage/Color/BorderColor`

### GadgetRadioSetHiliteImage / GadgetRadioSetHiliteColor / GadgetRadioSetHiliteBorderColor
- Purpose: Configures visual appearance when radio button is highlighted.
- Calls: `g->winSetHiliteImage/Color/BorderColor`

### GadgetRadioGetSelectedImage / GadgetRadioGetSelectedUncheckedBoxImage / GadgetRadioGetSelectedCheckedBoxImage
- Purpose: Retrieves visual elements for the selected state.
- Calls: `g->winGetHilite
