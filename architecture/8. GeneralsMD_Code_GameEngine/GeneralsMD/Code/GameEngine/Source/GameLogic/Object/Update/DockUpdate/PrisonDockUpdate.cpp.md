# GeneralsMD/Code/GameEngine/Source/GameLogic/Object/Update/DockUpdate/PrisonDockUpdate.cpp

## Purpose
Handles docking logic for prison structures in the game, specifically managing prisoner transfers from POW trucks.

## Responsibilities
- Manages docking actions between POW trucks and prison structures
- Unloads prisoners from trucks into the prison
- Handles serialization (CRC and Xfer) for network synchronization
- Provides load-time post-processing

## Key Types
- PrisonDockUpdate (Class): Manages prisoner docking logic for prison structures
- POWTruckAIUpdateInterface (Interface): Used to unload prisoners from trucks

## Key Functions
### PrisonDockUpdate::action
- Purpose: Handles the docking action to transfer prisoners from a POW truck to the prison
- Calls: getContain(), getAIUpdateInterface(), getPOWTruckAIUpdateInterface(), unloadPrisonersToPrison()

### PrisonDockUpdate::crc
- Purpose: Serializes the object for CRC calculation
- Calls: DockUpdate::crc()

### PrisonDockUpdate::xfer
- Purpose: Handles object serialization/deserialization
- Calls: DockUpdate::xfer()

### PrisonDockUpdate::loadPostProcess
- Purpose: Performs post-load initialization
- Calls: DockUpdate::loadPostProcess()

## Globals
None

## Dependencies
- PreRTS.h, ThingTemplate.h, Xfer.h, Object.h, ContainModule.h, POWTruckAIUpdate.h, PrisonDockUpdate.h
- DockUpdate (base class)
- ContainModuleInterface, AIUpdateInterface, POWTruckAIUpdateInterface (external interfaces)
