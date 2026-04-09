# Generals/Code/GameEngine/Source/GameLogic/Object/Update/FlammableUpdate.cpp - Enhanced Analysis

## Architectural Role
The `FlammableUpdate` class is a critical component of the game logic, responsible for managing the flammable and burned statuses of game objects. It integrates with various subsystems such as audio, damage handling, and object status management to provide realistic fire effects.

## Cross-References
### Incoming
- **GameLogic**: Calls `FlammableUpdate::onDamage` when an object takes flame or particle beam damage.
- **AudioEventRTS**: Used by `startBurningSound` and `stopBurningSound` for managing burning sounds.
- **FireSpreadUpdate**: Accessed in `tryToIgnite` to start fire spreading.

### Outgoing
- **GameLogic**: Interacts with game logic through methods like `getObject()->setStatus`, `attemptDamage`, and `setModelConditionState`.
- **AudioEventRTS**: Manages audio events for burning sounds.
- **FireSpreadUpdate**: Starts fire spreading when an object catches fire.

## Design Patterns
- **Observer Pattern**: The class observes damage events (`onDamage`) to determine if the object should catch fire.
- **State Pattern**: Manages different states (normal, aflame, burned) with transitions handled by methods like `tryToIgnite` and `update`.
- **Strategy Pattern**: Uses configuration data (`FlammableUpdateModuleData`) to define behavior such as damage amounts and sound names.
