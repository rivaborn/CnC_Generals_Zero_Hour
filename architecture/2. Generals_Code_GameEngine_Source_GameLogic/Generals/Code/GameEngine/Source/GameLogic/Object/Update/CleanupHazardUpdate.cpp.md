# Generals/Code/GameEngine/Source/GameLogic/Object/Update/CleanupHazardUpdate.cpp

## Purpose
This file contains the implementation of the `CleanupHazardUpdate` class, which handles the cleanup of hazards by targeting and destroying them.

## Responsibilities
- Manages the targeting and destruction of hazards.
- Ensures the object remains "busy" for scripting purposes during cleanup operations.
- Handles periodic scanning to find the closest target within a specified range.
- Controls firing based on weapon availability and target proximity.

## Key Types
- `CleanupHazardUpdateModuleData (struct)`: Stores configuration data for hazard cleanup, including weapon slot, scan frames, and scan range.
- `CleanupHazardUpdate (class)`: Manages the cleanup process, handling updates, targeting, and firing logic.

## Key Functions
### CleanupHazardUpdate::onObjectCreated
- Purpose: Initializes the module by setting up the weapon template and ensuring the scan range is larger than the firing range.
- Calls: `setWeaponSetFlag`, `getWeaponInWeaponSlot`, `getTemplate`, `getAttackRange`.

### CleanupHazardUpdate::update
- Purpose: The main update function that handles scanning for targets, managing target acquisition, and controlling firing.
- Calls: `isIdle`, `aiBusy`, `scanClosestTarget`, `fireWhenReady`, `findObjectByID`, `getDistanceSquared`, `setWeaponLock`, `aiAttackObject`.

### CleanupHazardUpdate::fireWhenReady
- Purpose: Handles the logic for firing at a target, including checking range and weapon availability.
- Calls: `findObjectByID`, `getAttackRange`, `isIdle`, `isBusy`, `setWeaponLock`, `aiAttackObject`.

### CleanupHazardUpdate::scanClosestTarget
- Purpose: Scans for the closest target within the specified scan range.
- Calls: `getClosestObject`, `getID`.

## Globals
- None

## Dependencies
- Key includes:
  - "PreRTS.h"
  - "Common\RandomValue.h"
  - "Common\ThingTemplate.h"
  - "Common\Xfer.h"
  - "GameClient\Drawable.h"
  - "GameLogic\GameLogic.h"
  - "GameLogic\PartitionManager.h"
  - "GameLogic\Object.h"
  - "GameLogic\ObjectIter.h"
  - "GameLogic\Module\CleanupHazardUpdate.h"
  - "GameLogic\Module\PhysicsUpdate.h"
  - "GameLogic\Weapon.h"
  - "GameLogic\WeaponSet.h"
  - "GameLogic\Module\AIUpdate.h"
