# GeneralsMD/Code/GameEngine/Include/GameLogic/Module/OpenContain.h - Enhanced Analysis

## Architectural Role
This file defines the core containment system for the SAGE engine, enabling objects (vehicles, buildings) to carry other objects (units, crates). It bridges multiple subsystems (collision, damage, AI) through its interface inheritance, acting as a central hub for transport/container logic.

## Cross-References
### Incoming
- **AI/Behavior System**: Calls `orderAllPassengersToExit` and `orderAllPassengersToIdle` for passenger management
- **Collision System**: Invokes `onCollide` for container collision handling
- **Damage System**: Uses `onDamage` and `processDamageToContained` for damage propagation
- **UI System**: Likely calls `isDisplayedOnControlBar` for control bar rendering

### Outgoing
- **Audio System**: Plays `m_enterSound`/`m_exitSound` via `doLoadSound`/`doUnloadSound`
- **Object System**: Manages object lifecycle via `addOrRemoveObjFromWorld`
- **Model System**: Uses `m_firePoints` for passenger positioning relative to container model

## Design Patterns
- **Strategy Pattern**: `ExitInterface` allows different exit behaviors (doors, budding) without modifying `OpenContain`
- **Composite Pattern**: `ContainedItemsList` treats contained objects as a unified group for operations
- **Observer Pattern**: `monitorConditionChanges` reacts to model state changes (e.g., door opening) to reposition passengers

*Not inferable*: Exact implementation of `reserveDoorForExit` or `exitObjectViaDoor` (likely Template Method).
