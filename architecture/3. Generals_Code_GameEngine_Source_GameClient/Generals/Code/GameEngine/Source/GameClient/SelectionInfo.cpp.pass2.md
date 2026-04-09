# Generals/Code/GameEngine/Source/GameClient/SelectionInfo.cpp - Enhanced Analysis

## Architectural Role
This file implements the selection system's decision logic, bridging UI input (selection/drag operations) with game object relationships and command evaluation. It acts as a mediator between the input system and the command execution pipeline, determining context-sensitive behavior (e.g., force attack mode, garrisoning).

## Cross-References
### Incoming
- **GameClient/InGameUI.cpp**: Likely calls `contextCommandForNewSelection` during selection/drag operations
- **GameClient/CommandXlat.cpp**: Uses `getPickTypesForContext` for command translation
- **GameClient/Drawable.cpp**: Calls `addDrawableToList` during region-based selection

### Outgoing
- **GameClient/GameClient.cpp**: Calls `evaluateContextCommand` for command validation
- **GameLogic/ActionManager.cpp**: Uses `canPlayerGarrison` for garrison logic
- **Common/PlayerList.cpp**: Accesses `ThePlayerList` for relationship checks

## Design Patterns
- **Strategy Pattern**: `getPickTypesForContext` dynamically selects pick logic based on UI state (force attack mode, GUI commands)
- **Visitor Pattern**: `addDrawableToList` acts as a visitor for drawable filtering during region queries
- **State Pattern**: Selection behavior implicitly changes based on `SelectionInfo` counts (e.g., enemy/friend/civilian thresholds)

*Not inferable*: No clear use of Observer or Factory patterns in this file.
