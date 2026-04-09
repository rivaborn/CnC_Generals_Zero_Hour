# GeneralsMD/Code/GameEngine/Source/GameLogic/Object/SpecialPower/DemoralizeSpecialPower.cpp

## Purpose
Implements the Demoralize special power, which affects enemy infantry within a range, reducing their effectiveness based on captured units.

## Responsibilities
- Applies demoralization effect to enemy infantry in a configurable range
- Calculates range and duration based on captured units
- Plays visual effects at the target location
- Handles serialization and CRC for network sync

## Key Types
- **DemoralizeSpecialPowerModuleData (Class)**: Stores configuration data for the demoralize power (range, duration, FX)
- **DemoralizeSpecialPower (Class)**: Implements the demoralize special power logic
- **None**: No enums/structs defined

## Key Functions
### `doSpecialPowerAtLocation`
- Purpose: Applies demoralization effect to objects in the specified location's range
- Calls: `SpecialPowerModule::doSpecialPowerAtLocation`, `ThePartitionManager->iterateObjectsInRange`, `FXList::doFXPos`, `ai->setDemoralized`

### `doSpecialPowerAtObject`
- Purpose: Applies demoralization effect to a specific target object
- Calls: `doSpecialPowerAtLocation`

### `crc`
- Purpose: Generates CRC checksum for network synchronization
- Calls: `SpecialPowerModule::crc`

### `xfer`
- Purpose: Serializes/deserializes the module state
- Calls: `SpecialPowerModule::xfer`

### `loadPostProcess`
- Purpose: Post-processing after loading module data
- Calls: `SpecialPowerModule::loadPostProcess`

## Globals
- **None**: No global/static variables

## Dependencies
- `PreRTS.h`, `Common/Xfer.h`, `GameClient/FXList.h`, `GameClient/InGameUI.h`, `GameLogic/Object.h`, `GameLogic/PartitionManager.h`, `GameLogic/Module/AIUpdate.h`, `GameLogic/Module/ContainModule.h`, `GameLogic/Module/DemoralizeSpecialPower.h`
- `SpecialPowerModule`, `MultiIniFieldParse`, `Thing`, `ModuleData`, `Object`, `ContainModuleInterface`, `AIUpdateInterface`, `PartitionFilterRelationship`, `PartitionFilterAcceptByKindOf`, `PartitionFilterSameMapStatus`, `PartitionFilter`, `ObjectIterator`, `MemoryPoolObjectHolder`, `Xfer`, `FXList`
