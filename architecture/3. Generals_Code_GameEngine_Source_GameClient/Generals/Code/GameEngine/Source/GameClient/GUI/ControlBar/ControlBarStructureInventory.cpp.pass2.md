# Generals/Code/GameEngine/Source/GameClient/GUI/ControlBar/ControlBarStructureInventory.cpp - Enhanced Analysis

## Architectural Role
This file implements the UI logic for displaying garrisoned units within structures in the control bar, bridging the game's containment system (ContainModuleInterface) with the UI framework (GameWindow). It handles dynamic updates to the inventory display when units enter/leave structures or selection changes.

## Cross-References
### Incoming
- **ControlBar class**: Calls `populateStructureInventory` and `updateContextStructureInventory` from other UI contexts
- **ContainModuleInterface**: Invokes `populateButtonProc` during `iterateContained` traversal
- **InGameUI**: Likely triggers `updateContextStructureInventory` during selection changes

### Outgoing
- **GadgetButton API**: Uses `GadgetButtonSetEnabledImage`/`DrawOverlayImage` for button visualization
- **HotkeyManager**: Resets hotkeys during inventory population
- **CommandButton system**: Retrieves commands via `findCommandButton` for button functionality

## Design Patterns
- **Callback Pattern**: `populateButtonProc` serves as a visitor for `iterateContained`, enabling decoupled object iteration
- **State Management**: Tracks `m_lastRecordedInventoryCount` to detect changes requiring UI updates
- **Hardcoded Command IDs**: Uses magic numbers (STOP_ID/EVACUATE_ID) for command binding (anti-pattern noted in TODOs)
