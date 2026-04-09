# Generals/Code/GameEngine/Source/GameLogic/Object/Update/AutoFindHealingUpdate.cpp

## Purpose
This file implements the `AutoFindHealingUpdate` module, which handles automatic healing for game objects by scanning for nearby heal pads.

## Responsibilities
- Manages periodic scanning for heal pads.
- Determines if an object needs healing based on its health status.
- Directs AI-controlled objects to seek and use heal pads when necessary.

## Key Types
- `AutoFindHealingUpdateModuleData (struct)`: Stores configuration data for the healing update module, such as scan rate, range, and health thresholds.
- `AutoFindHealingUpdate (class)`: Implements the logic for automatic healing updates.

## Key Functions
### AutoFindHealingUpdate::update()
- Purpose: Updates the object's state, checking if it needs healing and directing it to heal pads if necessary.
- Calls:
  - `getObject()`
  - `getControllingPlayer()->getPlayerType()`
  - `getAutoFindHealingUpdateModuleData()`
  - `getBodyModule()->getHealth()`
  - `getBodyModule()->getMaxHealth()`
  - `scanClosestTarget()`
  - `aiGetHealed(healUnit, CMD_FROM_AI)`

### AutoFindHealingUpdate::scanClosestTarget()
- Purpose: Scans for the closest heal pad within a specified range.
- Calls:
  - `ThePartitionManager->iterateObjectsInRange()`
  - `isKindOf(KINDOF_HEAL_PAD)`
  - `ThePartitionManager->getDistanceSquared()`

## Globals
- None

## Dependencies
- Key includes and external symbols used but not defined here:
  - `PreRTS.h`
  - `Common\RandomValue.h`
  - `Common\ThingTemplate.h`
  - `Common\Player.h`
  - `Common\Xfer.h`
  - `GameClient\Drawable.h`
  - `GameLogic\GameLogic.h`
  - `GameLogic\PartitionManager.h`
  - `GameLogic\Object.h`
  - `GameLogic\ObjectIter.h`
  - `GameLogic\Module\AutoFindHealingUpdate.h`
  - `GameLogic\Module\PhysicsUpdate.h`
  - `GameLogic\Weapon.h`
  - `GameLogic\WeaponSet.h`
  - `GameLogic\Module\AIUpdate.h`
