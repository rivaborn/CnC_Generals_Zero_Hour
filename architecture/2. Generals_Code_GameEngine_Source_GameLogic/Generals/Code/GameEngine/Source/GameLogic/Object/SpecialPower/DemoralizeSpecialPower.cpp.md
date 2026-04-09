# Generals/Code/GameEngine/Source/GameLogic/Object/SpecialPower/DemoralizeSpecialPower.cpp

## Purpose
This file implements the `DemoralizeSpecialPower` class, which handles the demoralization special power in Command & Conquer Generals. It affects enemy units within a range by reducing their morale for a duration.

## Responsibilities
- Manages the initialization and execution of the demoralize special power.
- Calculates the effect's range and duration based on captured units.
- Applies the demoralizing effect to nearby enemy units.
- Handles serialization and deserialization of the module data.

## Key Types
- `DemoralizeSpecialPowerModuleData (struct)`: Stores configuration for the demoralize special power, including base and bonus values for range and duration.
- `DemoralizeSpecialPower (class)`: Implements the logic for executing the demoralize special power.

## Key Functions
### DemoralizeSpecialPower::doSpecialPowerAtLocation
- Purpose: Applies the demoralize effect at a specified location.
- Calls:
  - `SpecialPowerModule::doSpecialPowerAtLocation`
  - `ContainModuleInterface::getContainCount`
  - `ThePartitionManager->iterateObjectsInRange`
  - `AIUpdateInterface::setDemoralized`
  - `FXList::doFXPos`

### DemoralizeSpecialPower::doSpecialPowerAtObject
- Purpose: Applies the demoralize effect at a specified object's location.
- Calls:
  - `doSpecialPowerAtLocation`

## Globals
None

## Dependencies
- Key includes and external symbols used but not defined here:
  - `Common/Xfer.h`
  - `GameClient/FXList.h`
  - `GameLogic/Object.h`
  - `GameLogic/PartitionManager.h`
  - `GameLogic/Module/AIUpdate.h`
  - `GameLogic/Module/ContainModule.h`
  - `GameLogic/Module/DemoralizeSpecialPower.h`
