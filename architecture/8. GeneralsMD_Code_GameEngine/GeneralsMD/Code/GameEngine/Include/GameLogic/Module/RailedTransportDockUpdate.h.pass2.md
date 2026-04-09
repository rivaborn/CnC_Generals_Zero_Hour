# GeneralsMD/Code/GameEngine/Include/GameLogic/Module/RailedTransportDockUpdate.h - Enhanced Analysis

## Architectural Role
This file defines the docking behavior for railed transport units (e.g., trains), extending the base `DockUpdate` module. It bridges the game's entity system with the physics/animation pipeline, handling timed docking animations and load/unload logic.

## Cross-References
### Incoming
- **GameLogic/Module/DockUpdate.h**: Base class inheritance
- **GameLogic/Module/Thing.h**: `Thing` parameter in constructor
- **GameLogic/Object.h**: `Object`/`ObjectID` references
- **GameLogic/Module/ModuleData.h**: `ModuleData` inheritance
- **GameLogic/Module/MultiIniFieldParse.h**: Config parsing

### Outgoing
- **GameLogic/Module/DockUpdate.h**: Implements `DockUpdateInterface`
- **GameLogic/Module/UpdateModule.h**: Inherits `UpdateSleepTime` return type
- **GameLogic/Module/MemoryPool.h**: Uses `MEMORY_POOL_GLUE` macros
- **GameLogic/Module/ModuleMacros.h**: Uses `MAKE_STANDARD_MODULE_MACRO`

## Design Patterns
- **Template Method**: `update()` orchestrates docking phases via `doPullInDocking`/`doPushOutDocking`
- **Strategy**: `RailedTransportDockUpdateInterface` abstracts docking operations for mocking/testing
- **State Machine**: Implicit in `m_unloadCount` and `m_dockingObjectID`/`m_unloadingObjectID` tracking

*Not inferable*: Exact memory pool implementation or `MultiIniFieldParse` usage.
