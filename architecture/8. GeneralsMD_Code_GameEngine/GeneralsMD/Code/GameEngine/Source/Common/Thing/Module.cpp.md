# GeneralsMD/Code/GameEngine/Source/Common/Thing/Module.cpp

## Purpose
Implements base module classes for game objects, including upgrade handling and serialization.

## Responsibilities
- Defines base `Module`, `ObjectModule`, and `DrawableModule` classes
- Implements upgrade multiplexing logic (`UpgradeMuxData`)
- Handles serialization (Xfer) and CRC for modules
- Provides factory method for module data creation

## Key Types
- `Module` (Class): Base class for all modules
- `ObjectModule` (Class): Module tied to game objects
- `DrawableModule` (Class): Module tied to drawable objects
- `UpgradeMuxData` (Struct): Handles upgrade application/removal logic

## Key Functions
### `Module::friend_newModuleData`
- Purpose: Factory method to create module data from INI
- Calls: `INI::initFromINI`

### `UpgradeMuxData::performUpgradeFX`
- Purpose: Applies upgrade visual effects to an object
- Calls: `FXList::doFXObj`

### `UpgradeMuxData::muxDataProcessUpgradeRemoval`
- Purpose: Removes specified upgrades from an object
- Calls: `Object::removeUpgrade`

### `UpgradeMuxData::getUpgradeActivationMasks`
- Purpose: Computes upgrade activation/conflict masks
- Calls: `TheUpgradeCenter->findUpgrade`

## Globals
- None

## Dependencies
- Key includes: `Module.h`, `Thing.h`, `INI.h`, `Upgrade.h`, `Xfer.h`
- External symbols: `TheUpgradeCenter`, `FXList`, `INI_INVALID_DATA`
