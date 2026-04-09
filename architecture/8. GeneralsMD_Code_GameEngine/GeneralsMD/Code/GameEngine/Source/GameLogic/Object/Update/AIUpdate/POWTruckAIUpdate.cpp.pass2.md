# GeneralsMD/Code/GameEngine/Source/GameLogic/Object/Update/AIUpdate/POWTruckAIUpdate.cpp - Enhanced Analysis

## Architectural Role
This file implements the specialized AI behavior for the POW Truck unit, extending the base AIUpdateInterface. It handles prisoner transport logic, prison interaction, and AI state management within the larger game logic system.

## Cross-References
### Incoming
- `ActionManager` (for command processing)
- `Player` (for money/bounty handling)
- `ContainModuleInterface` (for prisoner transport)
- Other AIUpdate modules (for prisoner surrender state)

### Outgoing
- `TheGameLogic` (for object lookup)
- `ThePartitionManager` (for spatial queries)
- `TheAI->pathfinder()` (for pathfinding)
- `TheInGameUI` (for floating text display)
- `TheGlobalData`/`TheGameText` (for localization)

## Design Patterns
- **State Pattern**: Uses `m_currentTask` enum to manage different AI states (WAITING, FIND_TARGET, etc.)
- **Strategy Pattern**: Different behaviors for AUTOMATIC vs MANUAL AI modes
- **Visitor Pattern**: Uses `iterateContained` with callback for prisoner transfer logic

*Not inferable*: Exact command pattern implementation details for AI commands.
