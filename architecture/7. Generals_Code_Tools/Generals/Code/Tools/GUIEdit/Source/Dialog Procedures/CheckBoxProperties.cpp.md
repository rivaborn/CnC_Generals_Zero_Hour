# Generals/Code/Tools/GUIEdit/Source/Dialog Procedures/CheckBoxProperties.cpp

## Purpose
Handles the properties dialog for checkbox gadgets in the GUI editor.

## Responsibilities
- Manages checkbox property dialog creation and callbacks
- Loads/saves checkbox state images and colors
- Handles user input for checkbox properties

## Key Types
- **ImageAndColorInfo (struct)**: Stores image and color data for checkbox states
- **GameWindow (class)**: Target window being edited
- **GadgetCheckBox (class)**: Checkbox gadget type

## Key Functions
### checkBoxPropertiesCallback
- Purpose: Handles dialog messages for checkbox properties
- Calls: `HandleCommonDialogMessages`, `SaveCommonDialogProperties`, `GetStateInfo`, `GadgetCheckBoxSet*`, `DestroyWindow`

### InitCheckBoxPropertiesDialog
- Purpose: Initializes and displays the checkbox properties dialog
- Calls: `CreateDialog`, `CommonDialogInitialize`, `GadgetCheckBoxGet*`, `StoreImageAndColor`, `SwitchToState`

## Globals
- None

## Dependencies
- `GUIEdit.h`, `Properties.h`, `Resource.h`, `GameClient/GadgetCheckBox.h`
- `TheEditor` (global editor instance)
- `HandleCommonDialogMessages`, `SaveCommonDialogProperties`, `GetStateInfo`, `StoreImageAndColor`, `SwitchToState` (external functions)
