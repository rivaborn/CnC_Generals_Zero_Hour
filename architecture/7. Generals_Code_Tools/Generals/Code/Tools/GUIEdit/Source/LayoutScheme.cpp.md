# Generals/Code/Tools/GUIEdit/Source/LayoutScheme.cpp

## Purpose
Handles layout scheme management for the GUI editor, including loading, saving, and applying visual schemes to UI elements.

## Responsibilities
- Manages layout scheme data (images, colors, fonts)
- Provides dialogs for loading/saving schemes
- Applies schemes to UI elements in the editor
- Handles scheme version compatibility

## Key Types
- LayoutScheme (Class): Main class for managing layout schemes
- ImageAndColorInfo (Struct): Stores image and color data for UI states
- StateIdentifier (Enum): Identifies different UI states (e.g., button enabled/disabled)

## Key Functions
### loadSchemeDataToDialog
- Purpose: Loads current scheme data into the dialog UI
- Calls: SetDlgItemText, SendDlgItemMessage, LoadStateCombo, LoadImageListComboBox, StoreImageAndColor, SwitchToState, LoadTextStateCombo, LoadFontCombo

### saveData
- Purpose: Saves dialog data back to the scheme
- Calls: GetStateInfo, storeImageAndColor, GetPropsEnabledTextColor, GetPropsEnabledTextBorderColor, GetPropsDisabledTextColor, GetPropsDisabledTextBorderColor, GetPropsHiliteTextColor, GetPropsHiliteTextBorderColor, GetSelectedFontFromCombo

### saveAsDialog
- Purpose: Shows a save file dialog for layout schemes
- Calls: GetSaveFileName

### openDialog
- Purpose: Shows an open file dialog for layout schemes
- Calls: GetOpenFileName

### layoutSchemeCallback
- Purpose: Handles dialog messages for the layout scheme dialog
- Calls: HandleCommonDialogMessages, loadSchemeDataToDialog, MessageBox, theScheme->applyPropertyTablesToWindow, saveAsDialog, saveData, theScheme->saveScheme, openDialog, theScheme->loadScheme

## Globals
- theScheme (LayoutScheme*): Current scheme being edited
- TheDefaultScheme (LayoutScheme*): Default scheme instance

## Dependencies
- Common/Debug.h
- GameClient/Gadget.h and related gadget headers
- GUIEdit.h, EditWindow.h, GUIEditWindowManager.h
- Resource.h, Properties.h, LayoutScheme.h
- Windows API (OPENFILENAME, DialogBox, etc.)
- Game-specific types (Image, Color, Font)
