# GeneralsMD/Code/GameEngine/Source/Common/RTS/ResourceGatheringManager.cpp - Enhanced Analysis

## Architectural Role
This file implements the resource gathering logic for supply trucks, acting as a bridge between the AI system and the game's economic simulation. It manages the lifecycle of supply structures and provides pathfinding decisions for resource transport.

## Cross-References
### Incoming
- **SupplyTruckAIUpdate**: Uses `findBestSupplyWarehouse` and `findBestSupplyCenter` for docking target selection
- **SupplyCenterDockUpdate/SupplyWarehouseDockUpdate**: Called via `getDockUpdateInterface` for docking validation
- **ActionManager**: Validates supply transfer eligibility via `canTransferSuppliesAt`

### Outgoing
- **GameLogic**: Queries object state via `findObjectByID`
- **PartitionManager**: Computes distances via `getDistanceSquared`
- **Object**: Accesses AI interfaces and docking modules

## Design Patterns
- **Strategy Pattern**: `computeRelativeCost` encapsulates docking target evaluation logic, allowing for future extensions (e.g., threat assessment)
- **Observer Pattern**: Implicitly observed by supply trucks via `SupplyTruckAIInterface`, though not explicitly implemented here
- **Null Object Pattern**: Returns `NULL` for invalid queries, delegating error handling to callers

*Not inferable*: No clear use of Factory, Decorator, or Visitor patterns.
