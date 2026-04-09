# GeneralsMD/Code/GameEngine/Source/GameLogic/Object/Update/DemoTrapUpdate.cpp

## Purpose
Handles demo trap proximity triggering logic in the game.

## Responsibilities
- Manages demo trap detonation based on proximity or manual triggers
- Handles weapon slot configuration for different detonation modes
- Implements scanning for nearby enemies within trigger range
- Processes special cases like friendly detonation and dozer disarming

## Key Types
- `DemoTrapUpdateModuleData` (Class): Stores configuration data for demo traps
- `DemoTrapUpdate` (Class): Main update module handling demo trap behavior

## Key Functions
### `DemoTrapUpdate::update()`
- Purpose: Main update loop that checks for detonation conditions
- Calls: `ThePartitionManager->iterateObjectsInRange`, `getObject()->getRelationship`, `detonate()`

### `DemoTrapUpdate::detonate()`
- Purpose: Triggers the demo trap explosion
- Calls: `TheWeaponStore->createAndFireTempWeapon`, `getObject()->kill()`

### `DemoTrapUpdate::onObjectCreated()`
- Purpose: Initializes demo trap state when object is created
- Calls: `getObject()->setWeaponSetFlag`, `getObject()->setWeaponLock`

## Globals
- None

## Dependencies
- `Common\BitFlagsIO.h`
- `Common\ThingTemplate.h`
- `Common\Xfer.h`
- `GameClient\Drawable.h`
- `GameLogic\GameLogic.h`
- `GameLogic\PartitionManager.h`
- `GameLogic\Object.h`
- `GameLogic\ObjectIter.h`
- `GameLogic\Module\DemoTrapUpdate.h`
- `GameLogic\Module\PhysicsUpdate.h`
- `GameLogic\Weaponset.h`
- `GameLogic\Weapon.h`
