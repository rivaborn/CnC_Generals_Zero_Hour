# GeneralsMD/Code/GameEngine/Source/GameLogic/Object/Update/AutoFindHealingUpdate.cpp

## Purpose
Handles AI behavior for units seeking healing from heal pads.

## Responsibilities
- Manages periodic scanning for nearby heal pads
- Determines when a unit should seek healing based on health thresholds
- Initiates healing requests via AI interface
- Configures scan parameters via module data

## Key Types
- **AutoFindHealingUpdateModuleData (Class)**: Stores configuration for scan rate, range, and health thresholds
- **AutoFindHealingUpdate (Class)**: Update module implementing healing-seeking behavior

## Key Functions
### AutoFindHealingUpdate::update
- Purpose: Main update loop that checks health and triggers healing scans
- Calls: getObject, getControllingPlayer, getAutoFindHealingUpdateModuleData, getAI, getBodyModule, aiGetHealed, scanClosestTarget

### AutoFindHealingUpdate::scanClosestTarget
- Purpose: Finds the nearest heal pad within scan range
- Calls: ThePartitionManager->iterateObjectsInRange, ThePartitionManager->getDistanceSquared

### AutoFindHealingUpdate::xfer
- Purpose: Serialization for network sync
- Calls: UpdateModule::xfer

## Globals
- None

## Dependencies
- Common: RandomValue, ThingTemplate, Player, Xfer
- GameClient: Drawable
- GameLogic: GameLogic, PartitionManager, Object, ObjectIter, Weapon, WeaponSet, AIUpdate
- Module headers: AutoFindHealingUpdate, PhysicsUpdate
