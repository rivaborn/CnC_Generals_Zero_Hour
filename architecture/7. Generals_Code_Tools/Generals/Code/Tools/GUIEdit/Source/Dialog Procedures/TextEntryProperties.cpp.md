# Generals/Code/Tools/GUIEdit/Source/Dialog Procedures/TextEntryProperties.cpp

## Purpose
Handles the text entry properties dialog for the GUI editor, allowing configuration of text entry gadgets.

## Responsibilities
- Manages dialog creation and callback for text entry properties
- Saves/loads text entry state properties (enabled/disabled/highlighted)
- Configures text entry constraints (max length, character types, secrecy)

## Key Types
- **ImageAndColorInfo (struct)**: Stores image and color data for different states
- **EntryData (struct)**: Holds text entry constraints (max length, character types, secrecy)

## Key Functions
### textEntryPropertiesCallback
- Purpose: Handles dialog messages for text entry properties
- Calls: `HandleCommonDialogMessages`, `SaveCommonDialogProperties`, `GadgetTextEntrySet*`, `GetStateInfo`, `GetDlgItemInt`, `IsDlgButtonChecked`

### InitTextEntryPropertiesDialog
- Purpose: Initializes and displays the text entry properties dialog
- Calls: `CreateDialog`, `CommonDialogInitialize`, `GadgetTextEntryGet*`, `StoreImageAndColor`, `SetDlgItemInt`, `CheckDlgButton`, `SwitchToState`

## Globals
- None

## Dependencies
- `GUIEdit.h`, `Properties.h`, `Resource.h`, `GameClient/GadgetTextEntry.h`
- `TheEditor` (global editor instance)
- `HandleCommonDialogMessages`, `SaveCommonDialogProperties`, `GetStateInfo`, `StoreImageAndColor`, `SwitchToState` (external functions)
- `GadgetTextEntrySet*` and `GadgetTextEntryGet*` (text entry gadget functions)
