# GeneralsMD/Code/GameEngine/Source/GameLogic/Object/Upgrade/UpgradeModule.cpp

## Purpose
Implements upgrade functionality for game objects, handling activation, conflicts, and state persistence.

## Responsibilities
- Manages upgrade execution state
- Validates upgrade conditions and conflicts
- Handles serialization (Xfer) and CRC for upgrades
- Processes upgrade effects and removals

## Key Types
- **UpgradeModule (Class)**: Base class for upgrade behavior, extends BehaviorModule and UpgradeMux
- **UpgradeMux (Class)**: Core upgrade logic handler
- **UpgradeMaskType**: Bitmask for upgrade conditions/conflicts

## Key Functions
### `UpgradeModule::crc`
- Purpose: Serializes upgrade module state for checksum
- Calls: `BehaviorModule::crc`, `UpgradeMux::upgradeMuxCRC`

### `UpgradeMux::attemptUpgrade`
- Purpose: Attempts to apply an upgrade if conditions are met
- Calls: `wouldUpgrade`, `giveSelfUpgrade`

### `UpgradeMux::giveSelfUpgrade`
- Purpose: Applies upgrade effects after validation
- Calls: `performUpgradeFX`, `processUpgradeRemoval`, `upgradeImplementation`

### `UpgradeMux::upgradeMuxXfer`
- Purpose: Serializes upgrade state for network/save
- Calls: None (direct Xfer calls)

## Globals
- **None**

## Dependencies
- `Xfer.h` (serialization)
- `UpgradeModule.h` (header)
- `BehaviorModule` (base class)
- `UpgradeMux` (mixin class)
