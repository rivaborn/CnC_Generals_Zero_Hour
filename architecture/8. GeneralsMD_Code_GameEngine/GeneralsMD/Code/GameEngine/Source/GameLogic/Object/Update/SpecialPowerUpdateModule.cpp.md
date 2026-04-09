# GeneralsMD/Code/GameEngine/Source/GameLogic/Object/Update/SpecialPowerUpdateModule.cpp

## Purpose
Implements the SpecialPowerUpdateModule class, handling special power updates for game objects.

## Responsibilities
- Manages special power update logic for game objects
- Performs science checks for special power availability
- Handles serialization (CRC and Xfer) for the module
- Provides post-load processing

## Key Types
- SpecialPowerUpdateModule (Class): Base class for special power update modules

## Key Functions
### SpecialPowerUpdateModule::doesSpecialPowerUpdatePassScienceTest
- Purpose: Checks if the player has the required science for the special power
- Calls: getExtraRequiredScience, getObject, getControllingPlayer, hasScience

### SpecialPowerUpdateModule::crc
- Purpose: Serializes the module for CRC calculation
- Calls: UpdateModule::crc

### SpecialPowerUpdateModule::xfer
- Purpose: Serializes the module for save/load operations
- Calls: UpdateModule::xfer

### SpecialPowerUpdateModule::loadPostProcess
- Purpose: Performs post-load processing
- Calls: UpdateModule::loadPostProcess

## Globals
- None

## Dependencies
- PreRTS.h
- Common/Player.h, Common/PlayerList.h, Common/Science.h, Common/SpecialPower.h, Common/Xfer.h
- GameLogic/GameLogic.h, GameLogic/Object.h
- GameLogic/Module/SpecialPowerUpdateModule.h, GameLogic/Module/SpecialPowerModule.h
