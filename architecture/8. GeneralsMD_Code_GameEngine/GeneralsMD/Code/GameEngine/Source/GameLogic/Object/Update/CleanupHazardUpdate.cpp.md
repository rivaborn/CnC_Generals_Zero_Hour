# GeneralsMD/Code/GameEngine/Source/GameLogic/Object/Update/CleanupHazardUpdate.cpp

## Purpose
Handles independent targeting and cleanup of hazard objects in the game world.

## Responsibilities
- Manages periodic scanning for hazard targets within a defined range
- Controls weapon firing at detected hazards
- Handles area cleanup commands with movement logic
- Tracks target validity and firing range
- Integrates with AI system for command handling

## Key Types
- **CleanupHazardUpdateModuleData (Class)**: Stores module configuration (weapon slot, scan rate, scan range)
- **CleanupHazardUpdate (Class)**: Main update module implementing hazard cleanup logic
- **WeaponBonus (Struct)**: Used for weapon range calculations (external)

## Key Functions
### CleanupHazardUpdate::update()
- Purpose: Main update loop that handles scanning and firing logic
- Calls: scanClosestTarget(), fireWhenReady(), AIUpdateInterface methods

### CleanupHazardUpdate::fireWhenReady()
- Purpose: Handles weapon firing at tracked targets with range checking
- Calls: ThePartitionManager distance calculations, AIUpdateInterface::aiAttackObject

### CleanupHazardUpdate::scanClosestTarget()
- Purpose: Finds nearest hazard target within scan range using partition system
- Calls: ThePartitionManager::getClosestObject

### CleanupHazardUpdate::setCleanupAreaParameters()
- Purpose: Configures the module for area cleanup operations
- Calls: AIUpdateInterface::aiMoveToPosition

## Globals
- None

## Dependencies
- Common: RandomValue, ThingTemplate, Xfer
- GameClient: Drawable
- GameLogic: GameLogic, PartitionManager, Object, ObjectIter, Weapon, WeaponSet
- GameLogic/Module: CleanupHazardUpdate.h, PhysicsUpdate.h, AIUpdate.h
- PreRTS.h (required first include)
