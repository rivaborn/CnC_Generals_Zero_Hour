# GeneralsMD/Code/GameEngine/Source/GameLogic/Object/Behavior/MinefieldBehavior.cpp - Enhanced Analysis

## Architectural Role
This file implements the core behavior for minefield objects in the game, handling detonation logic, collision detection, and health management. It integrates with the game's physics, damage, and weapon systems to create functional minefields that interact with other objects.

## Cross-References
### Incoming
- **GenerateMinefieldBehavior.cpp**: Uses `calcDistSquared`, `detonateOnce`, `onCollide`, `onDamage`, `setScootParms` for mine placement and management.
- **Other behavior modules**: Likely call `onCollide` and `onDamage` for collision and damage handling.

### Outgoing
- **Weapon System**: Calls `TheWeaponStore->createAndFireTempWeapon` for detonation effects.
- **Terrain System**: Uses `TheTerrainLogic->getGroundHeight` for scooting calculations.
- **Object System**: Calls `getObject()->attemptDamage` and `setWakeFrame` for health and update management.
- **Global Data**: Accesses `TheGlobalData->m_gravity` for physics calculations.

## Design Patterns
- **State Pattern**: Uses `UpdateSleepTime` to manage update frequency based on minefield state (e.g., draining, scooting).
- **Observer Pattern**: Listens for collision and damage events via `onCollide` and `onDamage`.
- **Strategy Pattern**: Configurable detonation logic via `MinefieldBehaviorModuleData` (e.g., `m_detonatedBy`, `m_workersDetonate`).
