# GeneralsMD/Code/GameEngine/Source/GameClient/GUI/ControlBar/ControlBarStructureInventory.cpp

## Purpose
Manages the UI display of objects garrisoned inside structures in the control bar.

## Responsibilities
- Populates inventory buttons with garrisoned objects
- Updates the inventory display when object counts change
- Handles hotkey management for garrisoned units
- Manages visibility and state of control bar buttons

## Key Types
- **PopulateButtonInfo (struct)**: Holds data for populating inventory buttons (source object, button index, control bar reference, button array)

## Key Functions
### `populateButtonProc`
- Purpose: Callback to populate a single inventory button with an object
- Calls: `GadgetButtonSetEnabledImage`, `GadgetButtonDrawOverlayImage`, `calculateVeterancyOverlayForObject`

### `populateStructureInventory`
- Purpose: Populates all inventory buttons for a given building
- Calls: `resetContainData`, `findCommandButton`, `setControlCommand`, `contain->iterateContained`

### `updateContextStructureInventory`
- Purpose: Updates the inventory display when needed (e.g., object count changes)
- Calls: `TheInGameUI->deselectDrawable`, `populateStructureInventory`

## Globals
- **STOP_ID (const int)**: Button ID for stop command (10)
- **EVACUATE_ID (const int)**: Button ID for evacuate command (11)

## Dependencies
- Common: `NameKeyGenerator`, `ThingTemplate`, `Player`, `PlayerList`
- GameLogic: `Object`, `ContainModuleInterface`
- GameClient: `InGameUI`, `Drawable`, `ControlBar`, `GameWindow`, `GameWindowManager`, `GadgetPushButton`, `Hotkey`
- External: `TheHotKeyManager`, `ThePlayerList`, `TheInGameUI`
