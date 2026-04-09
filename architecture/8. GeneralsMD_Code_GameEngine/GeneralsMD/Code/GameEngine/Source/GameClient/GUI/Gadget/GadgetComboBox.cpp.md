# GeneralsMD/Code/GameEngine/Source/GameClient/GUI/Gadget/GadgetComboBox.cpp

## Purpose
Implements the ComboBox GUI gadget for the game client, handling user input, list management, and visual state.

## Responsibilities
- Manages ComboBox input events (keyboard/mouse)
- Controls attached ListBox and TextEntry gadgets
- Handles selection, text entry, and visual styling
- Provides API for modifying ComboBox properties

## Key Types
- ComboBoxData (struct): Stores ComboBox state (entries, selection, flags)
- None: No classes defined in this file

## Key Functions
### GadgetComboBoxInput
- Purpose: Handles user input for ComboBox
- Calls: TheWindowManager->winNextTab, winPrevTab, winSendInputMsg, GadgetComboBoxGetEditBox, AudioEventRTS, winSetLoneWindow, winIsHidden, winHide, winGetSize, winSetSize, winSetPosition, winGetInstanceData, winFontHeight, winSetFont, winSetEnabledTextColors, winSetDisabledTextColors, winSetHiliteTextColors, winSetIMECompositeTextColors

### GadgetComboBoxSystem
- Purpose: Processes system messages for ComboBox
- Calls: winGetUserData, winGetInstanceData, winSendSystemMsg, GadgetComboBoxGetEditBox, GadgetTextEntryGetText, GadgetTextEntrySetText, GadgetComboBoxGetListBox, GadgetListBoxSetSelected, HideListBox, GadgetListBoxGetSelected

### GadgetComboBoxSetColors
- Purpose: Sets color scheme for ComboBox and sub-gadgets
- Calls: GadgetComboBoxSetEnabledColor, GadgetComboBoxSetEnabledBorderColor, GadgetComboBoxSetEnabledSelectedItemColor, GadgetComboBoxSetEnabledSelectedItemBorderColor, GadgetComboBoxSetDisabledColor, GadgetComboBoxSetDisabledBorderColor, GadgetComboBoxSetDisabledSelectedItemColor, GadgetComboBoxSetDisabledSelectedItemBorderColor, GadgetComboBoxSetHiliteColor, GadgetComboBoxSetHiliteBorderColor, GadgetComboBoxSetHiliteSelectedItemColor, GadgetComboBoxSetHiliteSelectedItemBorderColor, GadgetComboBoxGetEditBox, GadgetButtonSetEnabledColor, GadgetButtonSetEnabledBorderColor, GadgetButtonSetEnabledSelectedColor, GadgetButtonSetEnabledSelectedBorderColor, GadgetButtonSetDisabledColor, GadgetButtonSetDisabledBorderColor, GadgetButtonSetDisabledSelectedColor, GadgetButtonSetDisabledSelectedBorderColor, GadgetButtonSetHiliteColor, GadgetButtonSetHiliteBorderColor, GadgetButtonSetHiliteSelectedColor, GadgetButtonSetHiliteSelectedBorderColor, GadgetComboBoxGetDropDownButton, GadgetComboBoxGetListBox, GadgetListBoxSetColors

### GadgetComboBoxSetIsEditable
- Purpose: Enables/disables text editing in ComboBox
- Calls: winGetUserData, GadgetComboBoxGetEditBox, winGetStatus, winSetStatus

### GadgetComboBoxGetText
- Purpose: Retrieves current text from ComboBox
- Calls: winGetStyle, GadgetComboBoxGetEditBox, GadgetTextEntryGetText

### GadgetComboBoxSetText
- Purpose: Sets text in ComboBox
- Calls: GadgetComboBoxGetEditBox, GadgetTextEntrySetText

### GadgetComboBoxAddEntry
- Purpose: Adds an entry to ComboBox
- Calls: winSendSystemMsg

### GadgetComboBoxReset
- Purpose: Clears all entries from ComboBox
- Calls: winSendSystemMsg
