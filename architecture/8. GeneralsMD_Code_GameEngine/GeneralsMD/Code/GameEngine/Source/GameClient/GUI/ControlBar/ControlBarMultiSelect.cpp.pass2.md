# GeneralsMD/Code/GameEngine/Source/GameClient/GUI/ControlBar/ControlBarMultiSelect.cpp - Enhanced Analysis

## Architectural Role
This file implements the multi-select command UI logic for the control bar, bridging the gap between unit selection (InGameUI) and command execution (ControlBar). It dynamically filters and displays commands valid for all selected units, acting as a mediator between the selection system and the command UI.

## Cross-References
### Incoming
- **InGameUI**: Calls `populateMultiSelect` and `updateContextMultiSelect` when selection changes
- **ControlBar**: Internal calls from other ControlBar methods (e.g., `setControlCommand`)

### Outgoing
- **Command System**: Uses `findCommandSet` and `getCommandAvailability` to determine valid commands
- **UI System**: Interacts with `GameWindow` and `GadgetPushButton` for visual updates
- **Object System**: Queries `Object` properties to determine command eligibility

## Design Patterns
- **Mediator Pattern**: Coordinates between selected units and command UI without tight coupling
- **Strategy Pattern**: Command availability checks are delegated to `getCommandAvailability`
- **Observer Pattern**: Reacts to selection changes via InGameUI callbacks (implied by context)

*Not inferable*: Exact event-driven mechanism not visible in this file.
