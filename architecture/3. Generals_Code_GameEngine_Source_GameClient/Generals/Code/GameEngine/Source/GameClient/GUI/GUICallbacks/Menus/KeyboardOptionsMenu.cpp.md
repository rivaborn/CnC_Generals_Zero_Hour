# Generals/Code/GameEngine/Source/GameClient/GUI/GUICallbacks/Menus/KeyboardOptionsMenu.cpp

## Purpose
Handles the keyboard options menu UI, allowing players to remap hotkeys.

## Responsibilities
- Manages keyboard input for hotkey assignment
- Populates category and command lists
- Handles modifier key states (Shift, Ctrl, Alt)
- Processes key press/release events for hotkey editing
- Initializes and shuts down the keyboard options menu

## Key Types
- **EntryData (Struct)**: Tracks text entry state during hotkey assignment
- **None**: No custom classes/enums defined in this file

## Key Functions
### KeyboardTextEntryInput
- Purpose: Handles text input for hotkey assignment field
- Calls: `doKeyDown`, `doKeyUp`, `setKeyDown`, `GadgetTextEntryInput`

### populateCategoryBox
- Purpose: Fills the category dropdown with available command categories
- Calls: `GadgetComboBoxReset`, `GadgetComboBoxAddEntry`, `GadgetComboBoxSetSelectedPos`

### setKeyDown
- Purpose: Updates modifier key state flags
- Calls: None

### fillCommandListBox
- Purpose: Populates the command list based on selected category
- Calls: `GadgetListBoxReset`, `GadgetListBoxAddEntryText`

### doKeyUp/doKeyDown
- Purpose: Handles modifier key press/release logic for hotkey strings
- Calls: `setKeyDown`

### KeyboardOptionsMenuInit
- Purpose: Initializes the keyboard options menu UI elements
- Calls: `populateCategoryBox`, `fillCommandListBox`

### KeyboardOptionsMenuShutdown
- Purpose: Cleans up menu resources
- Calls: None

### KeyboardOptionsMenuInput
- Purpose: Processes menu navigation and button clicks
- Calls: `KeyboardOptionsMenuShutdown`

### KeyboardOptionsMenuSystem
- Purpose: Handles system messages for the menu
- Calls: `KeyboardTextEntryInput`

## Globals
- **buttonBackID/buttonBack (NameKeyType/GameWindow*)**: Back button reference
- **comboBoxCategoryListID/comboBoxCategoryList (NameKeyType/GameWindow*)**: Category dropdown
- **listBoxCommandListID/listBoxCommandList (NameKeyType/GameWindow*)**: Command list
- **staticTextDescriptionID/staticTextDescription (NameKeyType/GameWindow*)**: Description text
- **staticTextCurrentHotkeyID/staticTextCurrentHotkey (NameKeyType/GameWindow*)**: Current hotkey display
- **buttonResetAllID/buttonResetAll (NameKeyType/GameWindow*)**: Reset all button
- **textEntryAssignHotkeyID/textEntryAssignHotkey (NameKeyType/GameWindow*)**: Hotkey input field
- **buttonAssignID/buttonAssign (NameKeyType/GameWindow*)**: Assign button
- **shiftDown/altDown/ctrlDown (Bool)**: Modifier key state flags
- **absolute (Bool)**: Tracks if a non-modifier key was pressed
- **alt/ctrl/shift (UnicodeString)**: Modifier key display strings

## Dependencies
- **Includes**: `PreRTS.h`, `GameAudio.h`, `GameEngine.h`, `UserPreferences.h`, `WindowLayout.h`, `Gadget.h`, `GadgetComboBox.h`, `GadgetListBox.h`, `GadgetStaticText.h`, `IMEManager.h`, `Shell.h`, `KeyDefs.h`, `GameWindowManager.h`, `Mouse.h`, `GameText.h`, `MetaEvent.h`
- **External**: `TheNameKeyGenerator`, `TheWindowManager`, `TheGameText`, `TheMetaMap`, `GEM_UPDATE_TEXT`,
