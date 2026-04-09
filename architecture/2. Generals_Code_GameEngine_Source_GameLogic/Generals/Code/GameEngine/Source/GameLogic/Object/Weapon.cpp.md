# Generals/Code/GameEngine/Source/GameLogic/Object/Weapon.cpp

## Purpose
This file contains the implementation for weapon-related logic in Command & Conquer Generals, including parsing weapon templates from INI files and managing weapon states.

## Responsibilities
- Parse weapon data from INI files.
- Manage weapon states and properties.
- Handle weapon firing mechanics and line-of-sight checks.
- Implement CRC (Cyclic Redundancy Check) for weapon objects.

## Key Types
- **AssistanceRequestData (Class)**: Manages assistance request data.
- **WeaponTemplate**: Defines the template for weapons, including parsing functions.
- **WeaponBonusSet**: Represents a set of bonuses that can be applied to weapons.
- **WeaponBonus**: Represents individual bonuses that can be applied to weapon fields.

## Key Functions
### parsePerVetLevelAsciiString
- Purpose: Parses ASCII strings per veteran level from INI files.
- Calls: `INI::scanIndexList`, `ini->getNextToken`, `ini->getNextAsciiString`.

### parseAllVetLevelsAsciiString
- Purpose: Parses a single ASCII string for all veteran levels from INI files.
- Calls: `ini->getNextAsciiString`.

### parsePerVetLevelFXList
- Purpose: Parses FX lists per veteran level from INI files.
- Calls: `INI::scanIndexList`, `INI::parseFXList`.

### parseAllVetLevelsFXList
- Purpose: Parses a single FX list for all veteran levels from INI files.
- Calls: `INI::parseFXList`.

### isClearGoalFiringLineOfSightTerrain (overloaded)
- Purpose: Determines if the firing line of sight is clear between the source and goal positions, considering terrain.

## Globals
- **ATTACK_RANGE_CALC_TYPE**: Defines the type of attack range calculation.
- **DAMAGE_RANGE_CALC_TYPE**: Defines the type of damage range calculation.
- **TheWeaponStore**: Pointer to the weapon store definition.

## Dependencies
- Key includes: `Common/CRC.h`, `Common/GameState.h`, `GameLogic/Damage.h`, `GameLogic/Object.h`, `GameLogic/PartitionManager.h`.
- External symbols used: `TheVeterancyNames`, `TheDamageNames`, `TheWeaponAffectsMaskNames`, `TheWeaponCollideMaskNames`, `TheWeaponReloadNames`, `TheWeaponPrefireNames`.
