# Generals/Code/GameEngine/Source/GameClient/GUI/Gadget/GadgetComboBox.cpp

## Purpose
Implements the ComboBox GUI gadget, handling input, rendering, and management of dropdown list functionality.

## Responsibilities
- Manages ComboBox input events (keyboard/mouse)
- Controls dropdown list visibility and positioning
- Handles text entry and selection within the ComboBox
- Manages sub-gadgets (edit box, list box, dropdown button)
- Provides API for ComboBox configuration (colors, fonts, text limits)

## Key Types
- ComboBoxData (struct): Stores ComboBox state (entries, selection, editability)
- None: No classes defined in this file

## Key Functions
### GadgetComboBoxInput
- Purpose: Handles input messages for ComboBox
- Calls: TheWindowManager->winNextTab, TheWindowManager->winPrevTab, TheWindowManager->winSendInputMsg, HideListBox, GadgetComboBoxGetEditBox, GadgetComboBoxGetListBox, TheWindowManager->winSetLoneWindow, TheWindowManager->winFontHeight, TheAudio->addAudioEvent

### GadgetComboBoxSystem
- Purpose: Processes system messages for ComboBox
- Calls: TheWindowManager->winSendSystemMsg, GadgetTextEntryGetText, GadgetTextEntrySetText, GadgetListBoxSetSelected, HideListBox, GadgetListBoxGetSelected, GadgetComboBoxGetListBox

### GadgetComboBoxSetColors
- Purpose: Sets color scheme for ComboBox and sub-gadgets
- Calls: GadgetComboBoxSetEnabledColor, GadgetComboBoxSetEnabledBorderColor, GadgetComboBoxSetEnabledSelectedItemColor, GadgetComboBoxSetEnabledSelectedItemBorderColor, GadgetComboBoxSetDisabledColor, GadgetComboBoxSetDisabledBorderColor, GadgetComboBoxSetDisabledSelectedItemColor, GadgetComboBoxSetDisabledSelectedItemBorderColor, GadgetComboBoxSetHiliteColor, GadgetComboBoxSetHiliteBorderColor, GadgetComboBoxSetHiliteSelectedItemColor, GadgetComboBoxSetHiliteSelectedItemBorderColor, GadgetButtonSetEnabledColor, GadgetButtonSetEnabledBorderColor, GadgetButtonSetEnabledSelectedColor, GadgetButtonSetEnabledSelectedBorderColor, GadgetButtonSetDisabledColor, GadgetButtonSetDisabledBorderColor, GadgetButtonSetDisabledSelectedColor, GadgetButtonSetDisabledSelectedBorderColor, GadgetButtonSetHiliteColor, GadgetButtonSetHiliteBorderColor, GadgetButtonSetHiliteSelectedColor, GadgetButtonSetHiliteSelectedBorderColor, GadgetComboBoxGetEditBox, GadgetComboBoxGetDropDownButton, GadgetComboBoxGetListBox, GadgetListBoxSetColors

### GadgetComboBoxSetIsEditable
- Purpose: Enables/disables text editing in ComboBox
- Calls: GadgetComboBoxGetEditBox

### GadgetComboBoxGetText
- Purpose: Retrieves current text from ComboBox
- Calls: GadgetComboBoxGetEditBox, GadgetTextEntryGetText

### GadgetComboBoxSetText
- Purpose: Sets text in ComboBox
- Calls: GadgetComboBoxGetEditBox, GadgetTextEntrySetText

### GadgetComboBoxAddEntry
- Purpose: Adds an entry to ComboBox dropdown list
- Calls: TheWindowManager->winSendSystemMsg

### GadgetComboBoxGetSelectedPos
- Purpose: Gets currently selected item index
- Calls: TheWindowManager->winSendSystemMsg

### GadgetComboBoxSetSelectedPos
- Purpose: Sets selected item index
- Calls: TheWindowManager->winSendSystem
