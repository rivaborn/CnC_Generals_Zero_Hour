# Generals/Code/GameEngine/Source/GameLogic/Object/Behavior/FireWeaponWhenDamagedBehavior.cpp

## Purpose
This file implements the `FireWeaponWhenDamagedBehavior` class, which manages weapon firing behavior for game objects based on their damage state.

## Responsibilities
- Allocates and manages different weapons for various damage states.
- Handles object damage events to trigger appropriate weapon responses.
- Updates continuous weapon firing based on the object's current damage state.

## Key Types
- `FireWeaponWhenDamagedBehavior` (Class): Manages weapon behavior when an object is damaged.
- None

## Key Functions
### FireWeaponWhenDamagedBehavior::FireWeaponWhenDamagedBehavior
- Purpose: Initializes weapons based on module data and sets initial activation status.
- Calls:
  - `TheWeaponStore->allocateNewWeapon`
  - `reloadAmmo`
  - `giveSelfUpgrade`
  - `setWakeFrame`

### FireWeaponWhenDamagedBehavior::~FireWeaponWhenDamagedBehavior
- Purpose: Cleans up allocated weapons.
- Calls:
  - `deleteInstance`

### FireWeaponWhenDamagedBehavior::onDamage
- Purpose: Handles damage events to trigger reaction weapons based on the object's damage state.
- Calls:
  - `getDamageTypeFlag`
  - `forceFireWeapon`

### FireWeaponWhenDamagedBehavior::update
- Purpose: Updates continuous weapon firing based on the object's current damage state.
- Calls:
  - `forceFireWeapon`

## Globals
- `MAX_IDX` (Int): Maximum index value, not used in this file.
- `BEGIN_MIDPOINT_RATIO` (Real): Ratio for beginning midpoint, not used in this file.
- `END_MIDPOINT_RATIO` (Real): Ratio for end midpoint, not used in this file.

## Dependencies
- Key includes:
  - "PreRTS.h"
  - "Common/Thing.h"
  - "GameLogic/Module/FireWeaponWhenDamagedBehavior.h"
  - "GameLogic/Object.h"
  - "GameLogic/Weapon.h"

- External symbols used but not defined here:
  - `TheWeaponStore`
  - `DEBUG_ASSERTCRASH`
