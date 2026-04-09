# Generals/Code/Tools/GUIEdit/Source/Dialog Procedures/PushButtonProperties.cpp

## Purpose
Handles the push button properties dialog in the GUI editor tool, allowing users to modify button states and behaviors.

## Responsibilities
- Manages the push button properties dialog callback
- Initializes dialog with current button properties
- Saves modified properties back to the button object
- Handles common dialog messages and button-specific controls

## Key Types
- `ImageAndColorInfo` (struct): Stores image and color data for button states
- `GameWindow` (class): Represents the game window/control being edited

## Key Functions
### `pushButtonPropertiesCallback`
- Purpose: Handles dialog messages for the push button properties dialog
- Calls: `HandleCommonDialogMessages`, `SaveCommonDialogProperties`, `GetStateInfo`, `GadgetButtonSet*`, `IsDlgButtonChecked`, `DestroyWindow`

### `InitPushButtonPropertiesDialog`
- Purpose: Creates and initializes the push button properties dialog
- Calls: `CreateDialog`, `CommonDialogInitialize`, `GadgetButtonGet*`, `StoreImageAndColor`, `SwitchToState`, `CheckDlgButton`

## Globals
- None

## Dependencies
- `GUIEdit.h`, `Properties.h`, `Resource.h`, `GameClient/GadgetPushButton.h`
- `TheEditor` (global editor instance)
- `HandleCommonDialogMessages`, `SaveCommonDialogProperties`, `GetStateInfo`, `StoreImageAndColor`, `SwitchToState` (external functions)
- `GadgetButtonSet*` and `GadgetButtonGet*` functions (button property manipulation)
