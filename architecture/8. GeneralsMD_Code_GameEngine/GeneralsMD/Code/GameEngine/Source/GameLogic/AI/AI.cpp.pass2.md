# GeneralsMD/Code/GameEngine/Source/GameLogic/AI/AI.cpp - Enhanced Analysis

## Architectural Role
This file is the core of the AI subsystem, bridging game logic and pathfinding. It manages AI behavior trees, target selection, and spatial queries through the PartitionManager, while also handling serialization for network play.

## Cross-References
### Incoming
- **AIUpdate.h**: Calls `AI::update()` for per-frame processing
- **BehaviorTree.cpp**: Uses `AI::findClosestEnemy/Ally` for node evaluation
- **Unit.cpp**: Queries `AI::getAdjustedVisionRangeForObject` for stealth detection

### Outgoing
- **PartitionManager.h**: Spatial queries (`getClosestObject`, `iterateContained`)
- **Pathfinder.cpp**: Delegates pathfinding via `m_pathfinder`
- **ScriptEngine.h**: Evaluates scripted attack conditions

## Design Patterns
- **Strategy Pattern**: Target selection via `priorityFunc` callbacks
- **Composite Pattern**: `TAiData` aggregates faction-specific configs (`AISideInfo`, `AISideBuildList`)
- **Observer Pattern**: AI updates triggered by `GameLogic::update()` (not shown in snippet)
