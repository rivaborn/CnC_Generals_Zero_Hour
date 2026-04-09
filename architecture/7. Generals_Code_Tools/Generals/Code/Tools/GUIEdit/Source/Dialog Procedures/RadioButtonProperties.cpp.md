# Generals/Code/Tools/GUIEdit/Source/Dialog Procedures/RadioButtonProperties.cpp

## Purpose
Handles the radio button properties dialog in the GUI editor tool, allowing users to configure radio button appearance and behavior.

## Responsibilities
- Manages the radio button properties dialog callback
- Loads and saves radio button state properties (images, colors, borders)
- Handles group assignment for radio buttons
- Populates group combo box with existing groups

## Key Types
- **ImageAndColorInfo (struct)**: Stores image, color, and border color data for a radio button state
- **RadioButtonData (struct)**: Not inferable (used for radio button user data)
- **GameWindow (class)**: Represents a window/gadget in the GUI system

## Key Functions
### radioButtonPropertiesCallback
- Purpose: Handles dialog messages for the radio button properties dialog
- Calls: `HandleCommonDialogMessages`, `SaveCommonDialogProperties`, `GadgetRadioSet*`, `GetStateInfo`, `GetDlgItemInt`, `TheNameKeyGenerator->nameToKey`

### loadExistingGroupsCombo
- Purpose: Recursively populates a combo box with existing radio button groups
- Calls: `SendMessage` (CB_FINDSTRINGEXACT, CB_ADDSTRING), `winGetChild`, `winGetNext`, `BitTest`, `winGetStyle`

### InitRadioButtonPropertiesDialog
- Purpose: Initializes and displays the radio button properties dialog
- Calls: `CreateDialog`, `CommonDialogInitialize`, `GadgetRadioGet*`, `StoreImageAndColor`, `GetDlgItem`, `SetDlgItemInt`, `SwitchToState`

## Globals
- None

## Dependencies
- `Common/NameKeyGenerator.h`
- `GameClient/GameWindowManager.h`
- `GUIEdit.h`
- `Properties.h`
- `Resource.h`
- `GameClient/GadgetRadioButton.h`
- `GameClient/Gadget.h`
- Windows API (HWND, WPARAM, LPARAM, etc.)
- `TheEditor` (global editor instance)
- `TheWindowManager` (global window manager)
- `TheNameKeyGenerator` (global name key generator)
