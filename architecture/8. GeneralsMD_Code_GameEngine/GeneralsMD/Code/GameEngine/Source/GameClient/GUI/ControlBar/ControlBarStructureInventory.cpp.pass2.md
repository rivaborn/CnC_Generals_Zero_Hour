# GeneralsMD/Code/GameEngine/Source/GameClient/GUI/ControlBar/ControlBarStructureInventory.cpp - Enhanced Analysis

## Architectural Role
This file implements the UI logic for displaying garrisoned units within structures, bridging the game's object containment system (via `ContainModuleInterface`) with the control bar's visual representation. It handles dynamic updates to the inventory display when units enter/leave structures or selection changes.

## Cross-References
### Incoming
- Called by control bar context management (e.g., when structures are selected)
- Used by hotkey system (`TheHotKeyManager`) for dynamic hotkey assignment

### Outgoing
- Calls `ContainModuleInterface` methods (`iterateContained`, `getContainCount`, `getContainMax`)
- Uses `GadgetButton` UI primitives for button state management
- Interacts with `InGameUI` for selection handling

## Design Patterns
- **Callback Pattern**: `populateButtonProc` as a visitor for contained objects
- **Observer Pattern**: Implicit via `updateContextStructureInventory` reacting to containment changes
- **Strategy Pattern**: Command buttons (`Command_Evacuate`, `Command_Stop`) are dynamically assigned

*Not inferable*: No clear use of Factory, Decorator, or Composite patterns in this file.
