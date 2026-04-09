# GeneralsMD/Code/GameEngine/Source/GameClient/GUI/GUICallbacks/Menus/LanMapSelectMenu.cpp

## Purpose
Handles the LAN map selection menu UI, including map browsing, preview, and start position management.

## Responsibilities
- Manages map selection UI elements (listbox, preview, radio buttons)
- Handles map list population and filtering (system/user maps)
- Processes map selection and start position adjustments
- Coordinates with underlying LAN game options menu

## Key Types
- **None**

## Key Functions
### `LanMapSelectMenuInit`
- Purpose: Initializes the map selection menu UI and populates the map list.
- Calls: `showLANGameOptionsUnderlyingGUIElements`, `populateMapListbox`, `positionStartSpots`

### `LanMapSelectMenuSystem`
- Purpose: Handles system messages for the map selection menu (e.g., button clicks, map selection).
- Calls: `GadgetListBoxSetSelected`, `GadgetListBoxGetSelected`, `GadgetListBoxGetText`, `GadgetListBoxGetItemData`, `positionStartSpots`, `PostToLanGameOptions`

### `LanMapSelectMenuInput`
- Purpose: Processes keyboard input for the map selection menu (e.g., ESC key).
- Calls: `TheWindowManager->winSendSystemMsg`

### `positionStartSpots`
- Purpose: Positions start spot buttons on the map preview.
- Calls: Not inferable (external function).

## Globals
- `buttonBack` (NameKeyType): ID for the back button.
- `buttonOK` (NameKeyType): ID for the OK button.
- `listboxMap` (NameKeyType): ID for the map listbox.
- `winMapPreviewID` (NameKeyType): ID for the map preview window.
- `parent` (GameWindow*): Parent window reference.
- `mapList` (GameWindow*): Map list window reference.
- `winMapPreview` (GameWindow*): Map preview window reference.
- `radioButtonSystemMapsID` (NameKeyType): ID for the system maps radio button.
- `radioButtonUserMapsID` (NameKeyType): ID for the user maps radio button.
- `buttonMapStartPosition` (GameWindow*[]): Array of start position buttons.
- `buttonMapStartPositionID` (NameKeyType[]): Array of start position button IDs.

## Dependencies
- `WindowLayout.h`, `Gadget.h`, `Shell.h`, `GameWindowManager.h`, `GadgetListBox.h`, `GadgetRadioButton.h`, `LANAPICallbacks.h`, `MapUtil.h`, `GUIUtil.h`
- `TheWindowManager`, `TheNameKeyGenerator`, `TheMapCache`, `TheLAN
