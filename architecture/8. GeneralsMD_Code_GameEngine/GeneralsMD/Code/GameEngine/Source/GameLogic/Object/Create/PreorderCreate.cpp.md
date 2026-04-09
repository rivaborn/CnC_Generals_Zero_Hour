# GeneralsMD/Code/GameEngine/Source/GameLogic/Object/Create/PreorderCreate.cpp

## Purpose
Handles setting preorder visual state when a building is created.

## Responsibilities
- Applies preorder model condition if player preordered
- Clears preorder state if not preordered
- Implements serialization (Xfer) and CRC for network sync

## Key Types
- PreorderCreate (Class): Module for managing preorder visual state on building creation

## Key Functions
### PreorderCreate::onBuildComplete
- Purpose: Sets preorder model condition based on player's preorder status
- Calls: getObject(), getControllingPlayer(), didPlayerPreorder(), setModelConditionState(), clearModelConditionState()

### PreorderCreate::crc
- Purpose: Serializes class data for CRC calculation
- Calls: CreateModule::crc()

### PreorderCreate::xfer
- Purpose: Handles network serialization of the module
- Calls: CreateModule::xfer(), Xfer::xferVersion()

## Globals
None

## Dependencies
- PreRTS.h (must be first)
- Common/Player.h
- Common/Xfer.h
- GameLogic/Object.h
- GameLogic/Module/PreorderCreate.h
