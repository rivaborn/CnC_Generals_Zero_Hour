# Generals/Code/GameEngine/Source/GameLogic/Object/Behavior/MinefieldBehavior.cpp

## Purpose
This file implements the behavior for minefields in Command & Conquer Generals, including detonation logic, health management, and collision handling.

## Responsibilities
- Handle minefield detonation when triggered by enemy units.
- Manage minefield health and regeneration.
- Control minefield movement and positioning.
- Respond to collisions with other game objects.
- Serialize minefield state for save/load operations.

## Key Types
- `MinefieldBehaviorModuleData` (struct): Stores configuration data for minefields.
- `MinefieldBehavior` (class): Implements the behavior logic for minefields.

## Key Functions
### detonateOnce
- Purpose: Detonates a single virtual mine at a given position.
- Calls:
  - `TheWeaponStore->createAndFireTempWeapon`
  - `getObject()->attemptDamage`

### calcSleepTime
- Purpose: Determines how long the minefield can sleep before needing to update again.
- Calls:
  - `TheGameLogic->getFrame`

### update
- Purpose: Updates the minefield's state, including scooting and health draining.
- Calls:
  - `getObject()->setPosition`
  - `TheGameLogic->findObjectByID`
  - `attemptDamage`

### onCollide
- Purpose: Handles collisions with other objects, potentially triggering detonation.
- Calls:
  - `calcDistSquared`
  - `detonateOnce`

### onDamage
- Purpose: Manages damage to the minefield and triggers detonation as needed.
- Calls:
  - `attemptDamage`

## Globals
- `MIN_HEALTH` (Real): Minimum health threshold for minefields.

## Dependencies
- Key includes:
  - "Common/GameState.h"
  - "GameLogic/Object.h"
  - "GameLogic/Module/AIUpdate.h"
  - "GameLogic/Weapon.h"
- External symbols used:
  - `TheGameLogic`
  - `TheTerrainLogic`
  - `TheGlobalData`
  - `TheWeaponStore`
