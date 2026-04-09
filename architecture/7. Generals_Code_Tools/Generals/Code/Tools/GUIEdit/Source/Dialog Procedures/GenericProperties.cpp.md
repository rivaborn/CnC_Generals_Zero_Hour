# Generals/Code/Tools/GUIEdit/Source/Dialog Procedures/GenericProperties.cpp

## Purpose
Handles the properties dialog for generic windows in the GUI editor, managing visual states and callbacks.

## Responsibilities
- Manages dialog callbacks for property editing
- Handles color/image selection for window states (enabled/disabled/highlighted)
- Initializes combo boxes with available callbacks
- Saves edited properties back to the target window

## Key Types
- **RGBColorInt**: RGB color data structure
- **GameWindow**: Target window being edited
- **FunctionLexicon::TableEntry**: Callback function entry

## Key Functions
### genericPropertiesCallback
- Purpose: Handles dialog messages for property editing
- Calls: `HandleCommonDialogMessages`, `GetControlColor`, `SelectColor`, `SaveCommonDialogProperties`, `SaveCallbacks`

### InitCallbackCombos
- Purpose: Populates combo boxes with available callbacks
- Calls: `TheFunctionLexicon->getTable`, `SendMessage`

### InitUserWinPropertiesDialog
- Purpose: Initializes the properties dialog with current window values
- Calls: `CreateDialog`, `CommonDialogInitialize`, `LoadImageListComboBox`, `SetControlColor`, `InitCallbackCombos`

## Globals
- **TheEditor**: Editor instance (external)
- **TheFunctionLexicon**: Callback function registry (external)

## Dependencies
- Windows API (`windows.h`, `commctrl.h`)
- Common utilities (`Debug.h`, `FunctionLexicon.h`)
- Editor-specific headers (`GUIEdit.h`, `Properties.h`, `Resource.h`, `EditWindow.h`)
