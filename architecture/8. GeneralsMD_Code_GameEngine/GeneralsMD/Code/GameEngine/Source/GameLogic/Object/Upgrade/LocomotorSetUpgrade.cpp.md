# GeneralsMD/Code/GameEngine/Source/GameLogic/Object/Upgrade/LocomotorSetUpgrade.cpp

## Purpose
Implements an upgrade module that sets a locomotor set bit for weapon set selection in the game's AI system.

## Responsibilities
- Constructs and destructs the LocomotorSetUpgrade module
- Applies locomotor upgrades to the associated object via AI interface
- Handles serialization (Xfer) and CRC for save/load functionality
- Performs post-load processing

## Key Types
- LocomotorSetUpgrade (Class): Upgrade module that modifies locomotor behavior for AI pathfinding/weapon selection

## Key Functions
### LocomotorSetUpgrade::LocomotorSetUpgrade
- Purpose: Constructor that initializes the upgrade module
- Calls: UpgradeModule constructor

### LocomotorSetUpgrade::upgradeImplementation
- Purpose: Applies the locomotor upgrade by notifying the AI system
- Calls: getObject(), getAIUpdateInterface(), AIUpdateInterface::setLocomotorUpgrade

### LocomotorSetUpgrade::crc
- Purpose: Generates/verifies CRC checksum for save game integrity
- Calls: UpgradeModule::crc

### LocomotorSetUpgrade::xfer
- Purpose: Serializes/deserializes the module state
- Calls: UpgradeModule::xfer, Xfer::xferVersion

### LocomotorSetUpgrade::loadPostProcess
- Purpose: Performs post-load initialization
- Calls: UpgradeModule::loadPostProcess

## Globals
None

## Dependencies
- PreRTS.h (GameEngine header)
- Common/Xfer.h (Serialization)
- GameLogic/Object.h (Game object base)
- GameLogic/Module/LocomotorSetUpgrade.h (Module header)
- GameLogic/Module/AIUpdate.h (AI interface)
