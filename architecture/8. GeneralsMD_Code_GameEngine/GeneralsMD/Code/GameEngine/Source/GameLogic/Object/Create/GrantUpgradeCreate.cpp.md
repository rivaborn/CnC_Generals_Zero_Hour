# GeneralsMD/Code/GameEngine/Source/GameLogic/Object/Create/GrantUpgradeCreate.cpp

## Purpose
Handles granting upgrades to objects or players when a module is created or built.

## Responsibilities
- Parses configuration for upgrade granting
- Applies upgrades to objects or players under specific conditions
- Manages upgrade application during creation and build completion
- Handles serialization (Xfer) and CRC for network sync

## Key Types
- **GrantUpgradeCreateModuleData (Class)**: Holds upgrade name and exempt status flags
- **GrantUpgradeCreate (Class)**: Module that grants upgrades on creation/build

## Key Functions
### `onCreate`
- Purpose: Grants upgrade if object status matches exempt criteria
- Calls: `TheUpgradeCenter->findUpgrade`, `Player::addUpgrade`, `Object::giveUpgrade`, `Player::getAcademyStats()->recordUpgrade`

### `onBuildComplete`
- Purpose: Grants upgrade when object build completes (if not exempt)
- Calls: `TheUpgradeCenter->findUpgrade`, `Player::addUpgrade`, `Object::giveUpgrade`

### `xfer`
- Purpose: Serializes module state for network sync
- Calls: `CreateModule::xfer`

## Globals
- None

## Dependencies
- `PreRTS.h`, `Common/Player.h`, `Common/Upgrade.h`, `Common/Xfer.h`, `GameLogic/Module/GrantUpgradeCreate.h`, `GameLogic/Object.h`
- `TheUpgradeCenter` (external), `INI` namespace, `ObjectStatusMaskType`
