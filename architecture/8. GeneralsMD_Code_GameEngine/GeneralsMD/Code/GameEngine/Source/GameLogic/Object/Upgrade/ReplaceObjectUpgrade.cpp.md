# GeneralsMD/Code/GameEngine/Source/GameLogic/Object/Upgrade/ReplaceObjectUpgrade.cpp

## Purpose
Implements an upgrade module that replaces an object with another object at the same location.

## Responsibilities
- Parses configuration fields for the replacement object name
- Handles the replacement logic (destroying the original object and creating a new one)
- Ensures pathfinding and team/player relationships are maintained
- Triggers post-creation callbacks for the new object

## Key Types
- **ReplaceObjectUpgradeModuleData (Class)**: Holds configuration data for the replacement upgrade, including the name of the replacement object.
- **ReplaceObjectUpgrade (Class)**: Implements the upgrade module that performs the object replacement.

## Key Functions
### `buildFieldParse`
- Purpose: Registers the configuration fields for parsing.
- Calls: `UpgradeModuleData::buildFieldParse`

### `upgradeImplementation`
- Purpose: Executes the replacement logic by destroying the original object and creating a new one.
- Calls: `TheAI->pathfinder()->removeObjectFromPathfindMap`, `TheGameLogic->destroyObject`, `TheThingFactory->newObject`, `TheAI->pathfinder()->addObjectToPathfindMap`, `CreateModuleInterface::onBuildComplete`, `Player::onStructureConstructionComplete`

### `crc`
- Purpose: Handles CRC (checksum) serialization for the module.
- Calls: `UpgradeModule::crc`

### `xfer`
- Purpose: Handles serialization/deserialization of the module.
- Calls: `UpgradeModule::xfer`

### `loadPostProcess`
- Purpose: Performs post-loading initialization.
- Calls: `UpgradeModule::loadPostProcess`

## Globals
- **None**

## Dependencies
- Key includes: `PreRTS.h`, `GameLogic/Module/ReplaceObjectUpgrade.h`, `Common/Player.h`, `Common
