# GeneralsMD/Code/GameEngine/Include/GameLogic/Module/ContainModule.h - Enhanced Analysis

## Architectural Role
This file defines the core containment system interface for the SAGE engine, bridging game logic (e.g., garrisoning, transport) with rendering (hidden/displayed units) and AI (evacuation behaviors). It serves as a critical abstraction layer for all container-like objects (buildings, vehicles) in the game.

## Cross-References
### Incoming
- **AI System**: Calls `orderAllPassengersToExit`/`orderAllPassengersToIdle` for evacuation logic
- **Damage System**: Uses `processDamageToContained` to propagate damage to contained units
- **Selection System**: Invokes `clientVisibleContainedFlashAsSelected` for UI feedback
- **Networking**: Likely serializes containment state via `getContainedItemsList`

### Outgoing
- **Object System**: Relies on `Object` methods (e.g., `getControllingPlayer`) for player occupancy
- **Weapon System**: Uses `Weapon` for `attemptBestFirePointPosition` calculations
- **Audio System**: Controls `enableLoadSounds` for container-specific audio cues

## Design Patterns
- **Interface Segregation**: `ContainModuleInterface` splits container behaviors into fine-grained methods (e.g., `isGarrisonable`, `isBustable`) to avoid forcing unrelated implementations.
- **Strategy Pattern**: `EvacDisposition` enum and `setEvacDisposition` enable runtime behavior switching for evacuation logic.
- **Visitor Pattern**: `ContainIterateFunc` callback allows external iteration over contained objects without exposing internal list structure.
