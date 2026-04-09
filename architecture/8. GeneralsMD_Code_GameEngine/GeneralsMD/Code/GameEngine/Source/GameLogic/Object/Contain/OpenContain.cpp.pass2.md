# GeneralsMD/Code/GameEngine/Source/GameLogic/Object/Contain/OpenContain.cpp - Enhanced Analysis

## Architectural Role
This file implements the core containment system for the SAGE engine, managing how objects (units, vehicles) can be loaded into/out of containers (transports, buildings). It bridges the game logic layer with the object system, handling serialization, damage propagation, and containment rules.

## Cross-References
### Incoming
- **GameLogic/Object.cpp**: Calls `addToContain`/`removeFromContain` for transport/building interactions
- **GameLogic/AIUpdate.cpp**: Uses containment state for pathfinding/behavior decisions
- **GameClient/InGameUI.cpp**: Queries container state for UI feedback (e.g., load/unload buttons)

### Outgoing
- **GameLogic/PartitionManager.cpp**: Uses `addOrRemoveObjFromWorld` to toggle object visibility
- **GameLogic/AIPathfind.cpp**: Relies on `testForAttackingProc` for pathfinding around containers
- **Common/GameAudio.cpp**: Triggers `doLoadSound`/`doUnloadSound` for audio feedback

## Design Patterns
- **Strategy Pattern**: `OpenContainModuleData` configures containment behavior (e.g., `m_passengersAllowedToFire`) via INI parsing, allowing runtime specialization.
- **Observer Pattern**: `onContaining`/`onContainedBy` callbacks notify objects of containment state changes.
- **Memento Pattern**: `xfer()` serializes container state for save/load, preserving game integrity.

*Not inferable*: Exact use of `DieMuxData` or `ConditionState` integration.
