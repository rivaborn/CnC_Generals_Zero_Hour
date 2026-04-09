# GeneralsMD/Code/GameEngine/Include/GameLogic/Module/GarrisonContain.h - Enhanced Analysis

## Architectural Role
This file defines the core garrison containment system, bridging the game logic layer with the object containment hierarchy. It extends `OpenContain` to handle unit positioning, damage responses, and healing within garrisonable structures, playing a critical role in both combat mechanics and base defense.

## Cross-References
### Incoming
- **GameLogic/Module/OpenContain.h**: Base class for containment logic
- **Common/ModelState.h**: For damage state management
- **INI parsing utilities**: For configuration loading
- **Memory pool and module macros**: For object lifecycle management

### Outgoing
- **Object containment system**: Manages unit entry/exit
- **Damage system**: Handles body damage state changes
- **Healing system**: For unit recovery logic
- **Rally point system**: For unit deployment
- **Effect system**: For visual feedback (e.g., muzzle flashes)

## Design Patterns
- **Strategy Pattern**: Different behaviors for pristine/damaged/really damaged states via `findConditionIndex()` and `GARRISON_POINT_CONDITIONS`
- **Composite Pattern**: Manages a collection of garrisoned units as a single logical entity
- **Observer Pattern**: Notifies contained units of state changes (e.g., `onContaining`, `onRemoving`)

*Not inferable*: Exact implementation of `matchObjectsToGarrisonPoints()` and `positionObjectsAtStationGarrisonPoints()` suggests a spatial partitioning approach, but details are abstracted.
