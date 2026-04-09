# GeneralsMD/Code/GameEngine/Source/GameClient/GUI/ControlBar/ControlBarBeacon.cpp

## Purpose
Handles the beacon display functionality in the control bar, including UI population and input handling.

## Responsibilities
- Populates the beacon UI with object-specific data
- Manages visibility of beacon-related UI elements based on object control
- Handles input for the beacon window (e.g., ESC key)

## Key Types
- None

## Key Functions
### populateBeacon
- Purpose: Updates the beacon UI with object data and controls visibility based on object ownership
- Calls: `setPortraitByObject`, `GadgetTextEntrySetText`, `TheWindowManager->winGetWindowFromId`, `TheWindowManager->winSetFocus`, `TheWindowManager->winHide`

### updateContextBeacon
- Purpose: Placeholder for context updates (currently empty)
- Calls: None

### BeaconWindowInput
- Purpose: Handles input messages for the beacon window (e.g., ESC to deselect)
- Calls: `TheInGameUI->deselectAllDrawables`

## Globals
- None

## Dependencies
- `ControlBar.h`, `GameWindow.h`, `GadgetTextEntry.h`, `InGameUI.h`, `Object.h`, `NameKeyGenerator.h`, `ThingTemplate.h`, `Drawable.h`
- `TheWindowManager`, `TheInGameUI`, `NAMEKEY` macro
