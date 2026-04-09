# GeneralsMD/Code/GameEngine/Source/GameLogic/Object/Update/PointDefenseLaserUpdate.cpp

## Purpose
Handles independent targeting logic for point defense lasers in the game.

## Responsibilities
- Manages laser targeting behavior (scanning, tracking, firing)
- Implements scan range and fire range logic
- Handles primary/secondary target types
- Manages cooldown between shots
- Tracks target movement for prediction

## Key Types
- **PointDefenseLaserUpdateModuleData (Class)**: Stores configuration data for the laser update module
- **PointDefenseLaserUpdate (Class)**: Main update module handling laser targeting logic

## Key Functions
### PointDefenseLaserUpdate::update()
- Purpose: Main update loop for laser targeting
- Calls: fireWhenReady(), scanClosestTarget()

### PointDefenseLaserUpdate::fireWhenReady()
- Purpose: Handles weapon firing logic when target is ready
- Calls: TheWeaponStore->allocateNewWeapon(), w->loadAmmoNow(), w->fireWeapon(), scanClosestTarget()

### PointDefenseLaserUpdate::scanClosestTarget()
- Purpose: Scans for closest valid target within scan range
- Calls: ThePartitionManager->iterateObjectsInRange(), getObject()->getRelationship()

### PointDefenseLaserUpdate::xfer()
- Purpose: Serialization method for network sync
- Calls: UpdateModule::xfer()

## Globals
- **TheGameLogic (GameLogic**)**: Global game logic instance
- **ThePartitionManager (PartitionManager**)**: Global partition manager
- **TheWeaponStore (WeaponStore**)**: Global weapon store

## Dependencies
- Common headers: BitFlagsIO, RandomValue, ThingTemplate, Xfer
- GameClient: Drawable
- GameLogic: GameLogic, PartitionManager, Object, ObjectIter, Module headers
- Weapon system: Weapon, WeaponTemplate
