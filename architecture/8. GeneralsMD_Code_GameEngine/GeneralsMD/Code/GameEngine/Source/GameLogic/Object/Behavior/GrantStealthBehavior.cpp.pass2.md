# GeneralsMD/Code/GameEngine/Source/GameLogic/Object/Behavior/GrantStealthBehavior.cpp - Enhanced Analysis

## Architectural Role
This file implements the stealth-granting behavior for objects in the game, acting as a temporary effect module that scans nearby allies and applies stealth. It bridges the game logic layer with rendering (particle systems) and spatial partitioning systems.

## Cross-References
### Incoming
- Called by `ThePartitionManager` during spatial queries (via `iterateObjectsInRange`)
- Used by `StealthUpdate` module when stealth is granted/received
- Referenced in `Object` hierarchy for behavior attachment

### Outgoing
- Calls `TheParticleSystemManager` for visual effects
- Uses `ThePartitionManager` for spatial queries
- Interacts with `TheGameLogic` for object destruction
- Accesses `ContainModule` for rider/container relationships

## Design Patterns
- **Strategy Pattern**: Stealth granting logic is encapsulated as a behavior module that can be attached/detached from objects
- **Observer Pattern**: Particle system updates are tied to object position changes
- **Visitor Pattern**: `checkForGrantStealth` acts as a visitor callback during spatial queries

*Not inferable*: Exact factory pattern usage for module creation, though likely present in broader architecture.
