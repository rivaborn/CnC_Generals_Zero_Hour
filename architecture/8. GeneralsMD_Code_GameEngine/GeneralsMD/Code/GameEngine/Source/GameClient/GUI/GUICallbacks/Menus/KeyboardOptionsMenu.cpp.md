# GeneralsMD/Code/GameEngine/Source/GameClient/GUI/GUICallbacks/Menus/KeyboardOptionsMenu.cpp

## Purpose
Handles the keyboard options menu UI, allowing players to remap hotkeys.

## Responsibilities
- Manages keyboard input for hotkey assignment
- Populates category and command lists
- Handles modifier key states (Shift, Ctrl, Alt)
- Processes key press/release events for hotkey editing
- Initializes and shuts down the keyboard options menu

## Key Types
- `EntryData` (Struct): Tracks text entry state during hotkey assignment
- `MappableKeyCategories` (Enum): Categories for mappable keys (not inferable)
- `CategoryListName` (Array): List of category names (not inferable)

## Key Functions
### `populateCategoryBox`
- Purpose: Populates the category combo box with available key categories.
- Calls: `GadgetComboBoxReset`, `GadgetComboBoxAddEntry`, `GadgetComboBoxSetSelectedPos`

### `setKeyDown`
- Purpose: Updates modifier key state (Shift/Ctrl/Alt) during hotkey assignment.
- Calls: None

### `doKeyUp`
- Purpose: Handles key release events for modifier keys during hotkey assignment.
- Calls: `setKeyDown`

### `doKeyDown`
- Purpose: Handles key press events for modifier keys during hotkey assignment.
- Calls: `setKeyDown`

### `KeyboardOptionsMenuInit`
- Purpose: Initializes the keyboard options menu UI elements.
- Calls: `TheNameKeyGenerator->nameToKey`, `TheWindowManager->winGetWindowFromId`

### `KeyboardTextEntryInput`
- Purpose: Processes keyboard input for hotkey text entry field.
- Calls: `doKeyDown`, `doKeyUp`, `TheWindowManager->winSendSystemMsg`

## Globals
- `buttonBack` (GameWindow*): Back button widget
- `comboBoxCategoryList` (GameWindow*): Category selection combo box
- `listBoxCommandList` (GameWindow*): Command list box
- `shiftDown` (Bool): Tracks Shift key state
- `altDown` (Bool): Tracks Alt key state
- `ctrlDown` (Bool): Tracks Ctrl key state
- `absolute` (Bool): Tracks if a non-modifier key was pressed

## Dependencies
- `GameWindow`, `WindowLayout`, `UnicodeString`, `MetaMapRec`
- `GadgetComboBox`, `GadgetListBox`, `GadgetStaticText`
- `TheNameKeyGenerator`, `TheWindowManager`, `TheGameText`, `TheMetaMap`
