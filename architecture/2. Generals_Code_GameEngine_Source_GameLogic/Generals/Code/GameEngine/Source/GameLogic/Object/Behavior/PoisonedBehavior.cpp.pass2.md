# Generals/Code/GameEngine/Source/GameLogic/Object/Behavior/PoisonedBehavior.cpp - Enhanced Analysis

## Architectural Role
This file is integral to the game logic, specifically handling the behavior of objects that have been poisoned. It interacts with the damage system, visual effects (tinting), and updates the state of poisoned objects over time.

## Cross-References
### Incoming
- `DamageInfo::onDamage` calls `startPoisonedEffects`
- `DamageInfo::onHealing` calls `stopPoisonedEffects`
- `UpdateModule::update` calls `update`

### Outgoing
- Calls `getObject()->attemptDamage` to apply continuous damage.
- Calls `Drawable::setTintStatus` and `Drawable::clearTintStatus` to manage visual effects.
- Calls `TheGameLogic->getFrame()` to get the current game frame.

## Design Patterns
- **State Pattern**: The class manages different states (poisoned, not poisoned) and transitions between them using methods like `startPoisonedEffects` and `stopPoisonedEffects`.
- **Observer Pattern**: The class reacts to external events such as damage and healing through callbacks (`onDamage`, `onHealing`).
- **Singleton Pattern**: Uses `TheGameLogic` singleton to access game state information.
