# Generals/Code/GameEngine/Source/GameLogic/Object/Body/InactiveBody.cpp - Enhanced Analysis

## Architectural Role
The `InactiveBody` class is a crucial component in the game engine's object management system, specifically handling objects that do not have physical bodies. It ensures these objects are immune to health-related events and manages exceptions like unstoppable damage types. This class fits into the broader architecture by providing a specialized module for non-physical entities, ensuring they behave correctly within the game logic.

## Cross-References
### Incoming
- `GameLogic/Object.cpp`: Calls `InactiveBody::attemptDamage` and `InactiveBody::attemptHealing`.
- `GameLogic/Damage.cpp`: Calls `InactiveBody::estimateDamage`.

### Outgoing
- `GameLogic/Module/DieModule.h`: Called through `getObject()->onDie(damageInfo)`.
- `GameLogic/Object.h`: Interacts with the object's state via methods like `setEffectivelyDead` and `getTemplate()`.

## Design Patterns
- **Null Object Pattern**: The `InactiveBody` class acts as a null object for body-related operations, ensuring that objects without physical bodies do not interfere with game logic.
- **Strategy Pattern**: The class uses different strategies to handle damage and healing based on the type of damage received, such as ignoring all damage except unstoppable types.
