# Generals/Code/GameEngine/Source/GameClient/GUI/ControlBar/ControlBarBeacon.cpp

## Purpose
Handles the beacon display functionality in the control bar, including UI population and input handling.

## Responsibilities
- Populates the beacon UI with object-specific data
- Manages visibility of beacon-related UI elements based on object control
- Handles input events for the beacon window

## Key Types
None

## Key Functions
### populateBeacon
- Purpose: Updates the beacon UI with object data and controls visibility based on object control
- Calls: `setPortraitByObject`, `GadgetTextEntrySetText`, `TheWindowManager->winGetWindowFromId`, `TheWindowManager->winSetFocus`, `TheWindowManager->winHide`

### updateContextBeacon
- Purpose: Placeholder for context-sensitive beacon updates (currently empty)
- Calls: None

### BeaconWindowInput
- Purpose: Handles input events for the beacon window (currently only ESC key)
- Calls: `TheInGameUI->deselectAllDrawables`

## Globals
None

## Dependencies
- `PreRTS.h`
- `Common/NameKeyGenerator.h`
- `Common/ThingTemplate.h`
- `GameClient/ControlBar.h`
- `GameClient/Drawable.h`
- `GameClient/GameWindow.h`
- `GameClient/GadgetTextEntry.h`
- `GameClient/InGameUI.h`
- `GameLogic/Object.h`
- `TheWindowManager`
- `TheInGameUI`
