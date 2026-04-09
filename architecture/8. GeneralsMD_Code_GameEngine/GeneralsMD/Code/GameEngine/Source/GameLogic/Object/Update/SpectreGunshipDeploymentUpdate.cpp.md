# GeneralsMD/Code/GameEngine/Source/GameLogic/Object/Update/SpectreGunshipDeploymentUpdate.cpp

## Purpose
Handles deployment of the Spectre Gunship special power from the Command Center.

## Responsibilities
- Manages creation and positioning of Spectre Gunship objects
- Handles special power initiation and targeting
- Manages gunship lifecycle (creation, targeting, cleanup)
- Validates module data on object creation

## Key Types
- **SpectreGunshipDeploymentUpdateModuleData (Class)**: Stores configuration for gunship deployment (templates, science cost, etc.)
- **SpectreGunshipDeploymentUpdate (Class)**: Main update module handling gunship deployment logic
- **GunshipCreateLocType (Enum)**: Defines where gunship should be created relative to map edges

## Key Functions
### SpectreGunshipDeploymentUpdate::initiateIntentToDoSpecialPower
- Purpose: Creates and deploys the Spectre Gunship at calculated position
- Calls: TheThingFactory->newObject, TheTerrainLogic->findClosestEdgePoint, TheTerrainLogic->findFarthestEdgePoint, TheGameLogic->selectObject

### SpectreGunshipDeploymentUpdate::update
- Purpose: Handles periodic update checks for object validity
- Calls: getObject()->testStatus, getObject()->isEffectivelyDead

### SpectreGunshipDeploymentUpdate::onObjectCreated
- Purpose: Validates module data when object is created
- Calls: getObject()->getSpecialPowerModule

## Globals
- **TheGunshipCreateLocTypeNames (const char**)**: String array for gunship creation location types
- **zero (Real)**: Static zero value (0.0f)

## Dependencies
- Common: ThingTemplate, ThingFactory, Player, PlayerList, Xfer, ClientUpdateModule
- GameClient: ControlBar, GameClient, Drawable, ParticleSys, FXList
- GameLogic: Locomotor, GameLogic, PartitionManager, Object, ObjectIter, Weaponset, Weapon, TerrainLogic
- GameLogic/Module: SpecialPowerModule, SpectreGunshipDeploymentUpdate, PhysicsUpdate, LaserUpdate, ActiveBody, AIUpdate, ContainModule
