# Generals/Code/Tools/GUIEdit/Source/Dialog Procedures/ComboBoxProperties.cpp

## Purpose
Handles the combo box properties dialog in the GUI editor tool, allowing users to modify visual and behavioral properties of combo box controls.

## Responsibilities
- Manages the combo box properties dialog callback
- Initializes dialog with current combo box properties
- Saves modified properties back to the combo box control
- Handles sub-control color synchronization
- Manages combo box-specific properties (max chars, editability, etc.)

## Key Types
- `ImageAndColorInfo` (struct): Stores image and color data for UI states
- `ComboBoxData` (struct): Contains combo box-specific properties

## Key Functions
### `comboBoxPropertiesCallback`
- Purpose: Handles dialog messages and control events for the combo box properties dialog
- Calls: `HandleCommonDialogMessages`, `GetStateInfo`, `StoreColor`, `SaveCommonDialogProperties`, `GadgetComboBoxSet*`, `GadgetButtonSet*`, `GadgetTextEntrySet*`, `GadgetListBoxSet*`, `GadgetSliderSet*`

### `InitComboBoxPropertiesDialog`
- Purpose: Creates and initializes the combo box properties dialog with current control values
- Calls: `CreateDialog`, `CommonDialogInitialize`, `StoreImageAndColor`, `GadgetComboBoxGet*`, `GadgetButtonGet*`, `GadgetTextEntryGet*`, `GadgetListBoxGet*`, `GadgetSliderGet*`, `SetDlgItemInt`, `CheckDlgButton`, `SwitchToState`

## Globals
- None

## Dependencies
- Key includes: `GUIEdit.h`, `Properties.h`, `LayoutScheme.h`, `Resource.h`, `GameClient/GadgetComboBox.h`, `GameClient/GadgetListBox.h`, `GameClient/GadgetSlider.h`, `GameClient/GadgetPushButton.h`, `GameClient/GadgetTextEntry.h`, `GameClient/GameWindowManager.h`
- External symbols: `TheEditor`, `HandleCommonDialogMessages`, `SaveCommonDialogProperties`, `GetStateInfo`, `StoreColor`, `StoreImageAndColor`, `SwitchToState`, various `Gadget*` functions
