# GeneralsMD/Code/GameEngine/Source/GameLogic/Object/Collide/CrateCollide/SabotagePowerPlantCrateCollide.cpp - Enhanced Analysis

## Architectural Role
This file implements the sabotage behavior for power plant crates, bridging the collision system with game state modifications. It extends the base `CrateCollide` class to handle power plant-specific sabotage logic, including validation, effect triggering, and player notifications.

## Cross-References
### Incoming
- **AIUpdateInterface**: Validates goal object alignment during sabotage execution
- **Player/Energy**: Modifies power state via `setPowerSabotagedTillFrame` and `onPowerBrownOutChange`
- **Radar**: Triggers infiltration events via `tryInfiltrationEvent`
- **Eva**: Plays sabotage announcement via `setShouldPlay`

### Outgoing
- **CrateCollide**: Base class for collision validation and feedback effects
- **Object**: Checks target relationships and state via `getRelationship` and `isEffectivelyDead`
- **ThingTemplate**: Likely used for kind validation via `isKindOf(KINDOF_FS_POWER)`

## Design Patterns
- **Template Method**: Extends `CrateCollide` methods while preserving base behavior
- **Strategy**: Encapsulates sabotage logic as a module for power plant targets
- **Observer**: Notifies `Player` and `Radar` of sabotage events via callbacks

*Not inferable*: Exact serialization format or module data structure.
