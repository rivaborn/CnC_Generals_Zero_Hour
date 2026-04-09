# GeneralsMD/Code/GameEngine/Source/GameLogic/Object/Collide/CrateCollide/ConvertToHijackedVehicleCrateCollide.cpp

## Purpose
Handles the logic for hijacking vehicles when a terrorist (mobile crate) collides with an enemy vehicle.

## Responsibilities
- Validates target vehicles for hijacking (enemy, not dead, not immune, etc.)
- Transfers vehicle ownership to the hijacker's team
- Manages hijacker's entry into the vehicle (hiding, status flags)
- Handles experience/veterancy transfer between hijacker and vehicle

## Key Types
- **ConvertToHijackedVehicleCrateCollide (Class)**: Main class implementing vehicle hijacking behavior
- **HijackerUpdate (Class)**: Module for managing hijacker's state while in vehicle

## Key Functions
### ConvertToHijackedVehicleCrateCollide()
- Purpose: Constructor initializing the crate collision behavior
- Calls: CrateCollide constructor

### isValidToExecute()
- Purpose: Checks if a target vehicle can be hijacked
- Calls: CrateCollide::isValidToExecute(), getStatusBits(), getRelationship(), getContain(), getContainCount()

### executeCrateBehavior()
- Purpose: Performs the actual vehicle hijacking
- Calls: TheRadar->tryInfiltrationEvent(), TheEva->setShouldPlay(), setTeam(), setStatus(), aiMoveToPosition(), aiIdle(), cancelTask(), TheAudio->addAudioEvent(), transferObjectName(), setVeterancyLevel(), findUpdateModule(), setTargetObject(), setIsInVehicle(), setUpdate(), leaveGroup(), setVisionRange(), setShroudClearingRange(), unRegisterObject(), setDrawableHidden()

### crc()
- Purpose: Serialization CRC calculation
- Calls: CrateCollide::crc()

### xfer()
- Purpose: Serialization/deserialization
- Calls: CrateCollide::xfer()

### loadPostProcess()
- Purpose: Post-load initialization
- Calls: CrateCollide::loadPostProcess()

## Globals
- **key_HijackerUpdate (NameKeyType)**: Name key for HijackerUpdate module lookup

## Dependencies
- Common: Player, PlayerList, Radar, ThingTemplate, Xfer
- GameClient: Drawable, Eva, InGameUI
- GameLogic: ExperienceTracker, AIUpdate, HijackerUpdate, ContainModule, Object, PartitionManager, ScriptEngine, DozerAIUpdate
- PreRTS.h (must be first include)
