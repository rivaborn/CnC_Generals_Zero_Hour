# GeneralsMD/Code/GameEngine/Source/GameLogic/Object/Die/EjectPilotDie.cpp

## Purpose
Handles the ejection of a pilot object when a vehicle dies, with different behaviors for in-air and on-ground scenarios.

## Responsibilities
- Manages pilot ejection logic upon vehicle destruction
- Plays ejection sounds and voice lines
- Determines ejection based on vehicle's altitude
- Handles serialization and network synchronization

## Key Types
- **EjectPilotDieModuleData (Class)**: Stores configuration for ejection (creation lists, invulnerability time)
- **EjectPilotDie (Class)**: Implements the die module behavior for pilot ejection

## Key Functions
### `ejectPilot`
- Purpose: Creates pilot object and plays ejection sounds
- Calls: `ObjectCreationList::create`, `TheAudio->addAudioEvent`

### `onDie`
- Purpose: Handles the die callback to trigger pilot ejection
- Calls: `isDieApplicable`, `TheGameLogic->findObjectByID`, `ejectPilot`

### `crc`
- Purpose: Serialization checksum for network sync
- Calls: `DieModule::crc`

### `xfer`
- Purpose: Serialization for network sync
- Calls: `DieModule::xfer`

### `loadPostProcess`
- Purpose: Post-load initialization
- Calls: `DieModule::loadPostProcess`

## Globals
- None

## Dependencies
- `Common/GameAudio.h`, `Common/Player.h`, `Common/ThingFactory.h`, `Common/ThingTemplate.h`, `Common/Xfer.h`
- `GameLogic/GameLogic.h`, `GameLogic/Module/EjectPilotDie.h`, `GameLogic/ExperienceTracker.h`, `GameLogic/Object.h`, `GameLogic/ObjectCreationList.h`
- `TheAudio`, `TheGameLogic`
