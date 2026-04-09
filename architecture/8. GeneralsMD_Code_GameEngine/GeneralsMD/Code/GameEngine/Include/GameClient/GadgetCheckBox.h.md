# GeneralsMD/Code/GameEngine/Include/GameClient/GadgetCheckBox.h

## Purpose
Header file defining helper functions for checkbox gadgets in the game UI.

## Responsibilities
- Provides wrapper functions for checkbox state manipulation
- Manages visual states (enabled/disabled/highlighted)
- Handles checkbox text and checked state
- Exposes getter/setter functions for checkbox appearance

## Key Types
None

## Key Functions
### GadgetCheckBoxSetText
- Purpose: Sets the text of a checkbox gadget
- Calls: Not inferable

### GadgetCheckBoxIsChecked
- Purpose: Checks if a checkbox is currently checked
- Calls: Not inferable

### GadgetCheckBoxSetChecked
- Purpose: Sets the checked state of a checkbox
- Calls: Not inferable

### GadgetCheckBoxToggle
- Purpose: Toggles the checked state of a checkbox
- Calls: Not inferable

### GadgetCheckBoxSetEnabledImage / SetEnabledColor / SetEnabledBorderColor
- Purpose: Sets visual properties for enabled state
- Calls: GameWindow::winSetEnabledImage/Color/BorderColor

### GadgetCheckBoxSetDisabledImage / SetDisabledColor / SetDisabledBorderColor
- Purpose: Sets visual properties for disabled state
- Calls: GameWindow::winSetDisabledImage/Color/BorderColor

### GadgetCheckBoxSetHiliteImage / SetHiliteColor / SetHiliteBorderColor
- Purpose: Sets visual properties for highlighted state
- Calls: GameWindow::winSetHiliteImage/Color/BorderColor

## Globals
None

## Dependencies
- GameClient/GameWindow.h
- Uses GameWindow class methods (winSetEnabledImage/Color/BorderColor, etc.)
- Uses Image and Color types (not defined here)
