# GeneralsMD/Code/GameEngine/Source/GameLogic/Object/Behavior/NeutronBlastBehavior.cpp

## Purpose
Implements the behavior for neutron blast effects in the game, triggered when an object dies.

## Responsibilities
- Handles neutron blast logic on object death
- Applies blast effects to nearby objects based on configuration
- Manages special cases for infantry, vehicles, and containers
- Provides serialization and CRC support

## Key Types
- **NeutronBlastBehavior (Class)**: Manages neutron blast behavior for objects
- **NeutronBlastBehaviorModuleData (Struct)**: Configuration data for blast parameters (external)

## Key Functions
### `onDie`
- Purpose: Triggers neutron blast effect when object dies
- Calls: `getNeutronBlastBehaviorModuleData`, `ThePartitionManager->iterateObjectsInRange`, `neutronBlastToObject`

### `neutronBlastToObject`
- Purpose: Applies neutron blast effects to a specific object
- Calls: `getNeutronBlastBehaviorModuleData`, `obj->kill`, `contain->killAllContained`, `obj->setDisabled`, `obj->getAI()->aiIdle`, `TheGameLogic->deselectObject`, `obj->getDrawable()->setTerrainDecal`, `obj->setTeam`

### `update`
- Purpose: Update callback that returns sleep forever
- Calls: None

## Globals
- None

## Dependencies
- `NeutronBlastBehavior.h` (header)
- `Common/Player.h`, `Common/PlayerList.h`
- `GameLogic/Module/ContainModule.h`
- `GameLogic/GameLogic.h`, `GameLogic/Object.h`
- `GameLogic/PartitionManager.h`
- `GameLogic/Module/AIUpdate.h`
- `GameClient/Drawable.h`
