# GeneralsMD/Code/GameEngine/Source/GameLogic/Object/Behavior/FireWeaponWhenDamagedBehavior.cpp - Enhanced Analysis

## Architectural Role
This file implements a damage-reactive behavior system for game objects, bridging the damage state management (BodyModule) with weapon firing logic (Weapon). It's part of the modular behavior system that allows objects to dynamically change behavior based on damage states.

## Cross-References
### Incoming
- **BodyModule**: Calls `getDamageState()` to determine current damage level
- **Weapon**: Uses `forceFireWeapon()` to trigger weapon firing
- **UpdateModule**: Inherits and extends update logic
- **UpgradeMux**: Inherits upgrade management functionality

### Outgoing
- **TheWeaponStore**: Allocates weapon instances via `allocateNewWeapon()`
- **Object**: Accesses object properties and position
- **Xfer**: Handles serialization/deserialization for networking

## Design Patterns
- **Strategy Pattern**: Different weapon behaviors for different damage states (pristine, damaged, etc.)
- **State Pattern**: Behavior changes based on object's damage state
- **Observer Pattern**: Reacts to damage events via `onDamage()` callback

Rules followed. Output under 400 tokens.
