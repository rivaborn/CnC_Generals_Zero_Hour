# Generals/Code/Tools/GUIEdit/Source/Dialog Procedures/ProgressBarProperties.cpp

## Purpose
Handles the progress bar properties dialog in the GUI editor, allowing users to modify visual states and properties of progress bars.

## Responsibilities
- Manages dialog creation and initialization for progress bar properties
- Handles user input for modifying progress bar states (enabled/disabled/highlighted)
- Applies changes to the target progress bar gadget
- Stores and retrieves image and color data for different progress bar states

## Key Types
- `ImageAndColorInfo` (struct): Stores image and color data for progress bar states
- `GameWindow` (class): Represents the target window being edited
- `GadgetProgressBar` (class): Progress bar gadget class with state management methods

## Key Functions
### `progressBarPropertiesCallback`
- Purpose: Handles dialog messages and user interactions for the progress bar properties dialog
- Calls: `HandleCommonDialogMessages`, `SaveCommonDialogProperties`, `GetStateInfo`, `GadgetProgressBarSet*`, `DestroyWindow`

### `InitProgressBarPropertiesDialog`
- Purpose: Initializes and displays the progress bar properties dialog for a given window
- Calls: `CreateDialog`, `CommonDialogInitialize`, `GadgetProgressBarGet*`, `StoreImageAndColor`, `SwitchToState`

## Globals
- None

## Dependencies
- `GUIEdit.h`, `Properties.h`, `Resource.h`, `GameClient/GadgetProgressBar.h`
- `TheEditor` (global editor instance)
- `HandleCommonDialogMessages`, `SaveCommonDialogProperties`, `GetStateInfo`, `StoreImageAndColor`, `SwitchToState` (external functions)
- `GadgetProgressBarSet*` and `GadgetProgressBarGet*` methods (external)
