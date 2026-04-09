# GeneralsMD/Code/GameEngine/Source/GameLogic/Object/Contain/TransportContain.cpp - Enhanced Analysis

## Architectural Role
This file implements the core transport containment system, bridging the game logic layer with the object hierarchy. It manages unit loading/unloading mechanics, slot capacity, and special behaviors like health regeneration and weapon upgrades, serving as a critical component in the game's tactical gameplay.

## Cross-References
### Incoming
- **RailedTransportContain.cpp**: Calls `isSpecificRiderFreeToExit` and `onRemoving` for specialized transport behavior.
- **Other containment modules**: Likely invoke `isValidContainerFor` and `onContaining` during unit loading.

### Outgoing
- **OpenContain base class**: Extends functionality via `OpenContain::isValidContainerFor`, `OpenContain::onContaining`, etc.
- **AI/Pathfinding**: Uses `TheAI->pathfinder()->validMovementTerrain` for exit validation.
- **Physics/Animation**: Calls `setPosition`, `setOrientation`, `applyMotiveForce` for unloading mechanics.

## Design Patterns
- **Template Method**: Extends `OpenContain` with transport-specific overrides (e.g., `isSpecificRiderFreeToExit`).
- **Strategy**: Configurable behaviors (exit scattering, health regen) via `TransportContainModuleData`.
- **Observer**: Notifies contained units of state changes (e.g., `onRemoving` triggers `setAttitude`).

*(Note: Truncated content confirms these patterns but omits full implementation details.)*
