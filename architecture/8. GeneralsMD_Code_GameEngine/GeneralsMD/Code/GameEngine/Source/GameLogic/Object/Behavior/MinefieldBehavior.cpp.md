# GeneralsMD/Code/GameEngine/Source/GameLogic/Object/Behavior/MinefieldBehavior.cpp

## Purpose
Implements minefield behavior for objects, handling detonation, collision, and health management.

## Responsibilities
- Manages minefield detonation logic
- Handles object collisions and immunity tracking
- Controls minefield health and regeneration
- Implements scooting behavior for mines
- Manages virtual mine counts and damage

## Key Types
- **MinefieldBehaviorModuleData (Class)**: Configuration data for minefield behavior
- **MinefieldBehavior (Class)**: Core minefield behavior implementation
- **DetonatorInfo (Struct)**: Tracks objects that detonated mines
- **ImmunityInfo (Struct)**: Tracks immunity timers for objects

## Key Functions
### `calcDistSquared`
- Purpose: Calculates squared distance between two 3D points
- Calls: None

### `detonateOnce`
- Purpose: Handles single mine detonation and health adjustment
- Calls: `TheWeaponStore->createAndFireTempWeapon`, `getObject()->attemptDamage`

### `onCollide`
- Purpose: Handles collision events and detonation logic
- Calls: `calcDistSquared`, `detonateOnce`, `setWakeFrame`

### `onDamage`
- Purpose: Processes damage and adjusts virtual mine count
- Calls: `detonateOnce`, `getObject()->attemptDamage`

### `setScootParms`
- Purpose: Configures mine scooting movement parameters
- Calls: `TheTerrainLogic->getGroundHeight`, `setWakeFrame`

## Globals
- **MIN_HEALTH (Real)**: Minimum health threshold for mines (0.1f)

## Dependencies
- Key includes: `GameLogic/Module/MinefieldBehavior.h`, `GameLogic/Weapon.h`, `Common/Xfer.h`
- External symbols: `TheGameLogic`, `TheWeaponStore`, `TheTerrainLogic`, `TheGlobalData`
