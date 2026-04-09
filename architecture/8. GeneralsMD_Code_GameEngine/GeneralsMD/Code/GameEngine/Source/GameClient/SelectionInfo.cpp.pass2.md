# GeneralsMD/Code/GameEngine/Source/GameClient/SelectionInfo.cpp - Enhanced Analysis

## Architectural Role
This file implements the selection system's core logic, bridging UI input, game object relationships, and command execution. It acts as a mediator between player input (via `TheInGameUI`) and game object state, determining valid targets and context-sensitive actions.

## Cross-References
### Incoming
- **GameClient/CommandXlat.cpp**: Uses `contextCommandForNewSelection` to evaluate context commands
- **GameClient/GameClient.cpp**: Likely calls `addDrawableToList` during region-based selection
- **GameClient/ControlBar.cpp**: May use `getPickTypesForContext` for button state updates

### Outgoing
- **GameClient/GameClient.h**: Accesses `TheGameClient` for context command evaluation
- **GameClient/ControlBar.h**: Queries `TheInGameUI` for force attack/move modes
- **Common/PlayerList.h**: Checks object relationships via `ThePlayerList`

## Design Patterns
- **Strategy Pattern**: `getPickTypesForContext` dynamically selects pick logic based on UI state (force attack/move)
- **Visitor Pattern**: `addDrawableToList` acts as a callback for `iterateDrawablesInRegion`, filtering objects
- **State Pattern**: Selection behavior changes based on `forceAttackMode` and `forceMove` flags (implicit state)

*Not inferable*: No clear use of Observer or Factory patterns in this file.
