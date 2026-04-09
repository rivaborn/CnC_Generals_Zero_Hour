# GeneralsMD/Code/GameEngine/Source/GameLogic/Object/Die/RebuildHoleExposeDie.cpp

## Purpose
Handles the creation of a rebuild hole when a structure is destroyed, allowing it to be rebuilt later.

## Responsibilities
- Creates a rebuild hole object when the parent structure dies
- Transfers attackers to the new hole if enabled
- Configures hole properties (health, geometry, rebuild target)
- Handles serialization and network synchronization

## Key Types
- **RebuildHoleExposeDieModuleData (Class)**: Stores configuration for hole creation (hole template name, max health, attacker transfer flag)
- **RebuildHoleExposeDie (Class)**: Die module that implements the rebuild hole logic

## Key Functions
### RebuildHoleExposeDieModuleData::buildFieldParse
- Purpose: Registers INI field parsers for module data
- Calls: `DieModuleData::buildFieldParse`

### RebuildHoleExposeDie::onDie
- Purpose: Creates rebuild hole when parent object dies
- Calls: `isDieApplicable`, `getRebuildHoleExposeDieModuleData`, `TheThingFactory->newObject`, `TheAI->pathfinder()->addObjectToPathfindMap`, `RebuildHoleBehavior::getRebuildHoleBehaviorInterfaceFromObject`, `TheScriptEngine->transferObjectName`, `AIUpdateInterface::transferAttack`

### RebuildHoleExposeDie::crc
- Purpose: Generates CRC checksum for network synchronization
- Calls: `DieModule::crc`

### RebuildHoleExposeDie::xfer
- Purpose: Serializes/deserializes module state
- Calls: `DieModule::xfer`

### RebuildHoleExposeDie::loadPostProcess
- Purpose: Post-processing after loading
- Calls: `DieModule::loadPostProcess`

## Globals
- None

## Dependencies
- `PreRTS.h`, `Common/Player.h`, `Common/PlayerList.h`, `Common/ThingFactory.h`, `Common/Xfer.h`, `GameLogic/AI.h`, `GameLogic/AIPathfind.h`, `GameLogic/GameLogic.h`, `GameLogic/Module/AIUpdate.h`, `GameLogic/Module/BodyModule.h`, `GameLogic/Module/RebuildHoleBehavior.h`, `GameLogic/Module/RebuildHoleExposeDie.h`, `GameLogic/Object.h`, `GameLogic/ScriptEngine.h`, `GameClient/SelectionXlat.h`
