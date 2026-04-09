# Generals/Code/GameEngine/Source/GameLogic/Object/Behavior/InstantDeathBehavior.cpp

## Purpose
This file implements the `InstantDeathBehavior` class, which handles the immediate destruction of game objects upon taking damage.

## Responsibilities
- Parses configuration data for FX, OCLs, and weapons.
- Manages the death behavior of game objects.
- Triggers random effects, object creation lists, and weapon firing upon an object's death.

## Key Types
- `InstantDeathBehaviorModuleData (struct)`: Stores parsed data for FX, OCLs, and weapons.
- `InstantDeathBehavior (class)`: Handles the immediate destruction logic of game objects.

## Key Functions
### parseFX
- Purpose: Parses FX entries from an INI file.
- Calls: `TheFXListStore->findFXList`

### parseOCL
- Purpose: Parses OCL entries from an INI file.
- Calls: `TheObjectCreationListStore->findObjectCreationList`

### parseWeapon
- Purpose: Parses weapon template entries from an INI file.
- Calls: `TheWeaponStore->findWeaponTemplate`

## Globals
None

## Dependencies
- Key includes:
  - "PreRTS.h"
  - "Common/Thing.h"
  - "Common/ThingTemplate.h"
  - "Common/INI.h"
  - "GameLogic/Module/InstantDeathBehavior.h"
  - "GameLogic/Object.h"
  - "GameClient/FXList.h"
  - "GameLogic/Weapon.h"

- External symbols used:
  - `TheFXListStore`
  - `TheObjectCreationListStore`
  - `TheWeaponStore`
  - `GameLogicRandomValue`
  - `DEBUG_ASSERTCRASH`
  - `TheGameLogic`
