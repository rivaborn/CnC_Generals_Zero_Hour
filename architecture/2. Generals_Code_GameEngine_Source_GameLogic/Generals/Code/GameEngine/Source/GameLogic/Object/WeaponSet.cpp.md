# Generals/Code/GameEngine/Source/GameLogic/Object/WeaponSet.cpp

## Purpose
Handles the logic for weapon sets, including parsing from INI files, updating weapons, and choosing the best weapon for a target.

## Responsibilities
- Parsing weapon templates and settings from INI files.
- Managing weapon slots and their states.
- Updating weapons based on object conditions.
- Choosing the best weapon for a given target.
- Handling weapon locks and reloads.

## Key Types
- `WeaponTemplateSet` (Class): Manages a set of weapon templates.
- `WeaponSet` (Class): Represents a set of weapons for an object, including current state and selection logic.

## Key Functions
### getVictimAntiMask
- Purpose: Determines the anti-mask for a target based on its kind.
- Calls:
  - `isKindOf`
  - `isAirborneTarget`

### parseWeaponTemplateSet
- Purpose: Parses weapon template set data from an INI file.
- Calls:
  - `INI::parseFromINI`
  - `ThingTemplate::findWeaponTemplateSet`

### updateWeaponSet
- Purpose: Updates the weapon set for an object based on its current state and conditions.
- Calls:
  - `Object::getTemplate`
  - `WeaponTemplateSet::isWeaponLockSharedAcrossSets`
  - `Weapon::deleteInstance`
  - `TheWeaponStore::allocateNewWeapon`

### chooseBestWeaponForTarget
- Purpose: Chooses the best weapon for a target based on criteria like damage and range.
- Calls:
  - `Weapon::estimateWeaponDamage`
  - `Weapon::isWithinAttackRange`
  - `Weapon::getAntiMask`
  - `Weapon::isWithinTargetPitch`

## Globals
- None

## Dependencies
- Key includes:
  - "GameLogic/WeaponSet.h"
  - "Common/INI.h"
  - "Common/ThingFactory.h"
  - "Common/ThingTemplate.h"
  - "GameLogic/AI.h"
  - "GameLogic/Object.h"
  - "GameLogic/Weapon.h"

- External symbols used:
  - `TheWeaponSlotTypeNames`
  - `TheCommandSourceMaskNames`
  - `TheThingFactory`
  - `TheWeaponStore`
