# Generals/Code/GameEngine/Source/GameLogic/Object/Die/EjectPilotDie.cpp

## Purpose
This file implements the logic for ejecting a pilot when an object dies, creating new objects based on whether the dying object is in air or on ground.

## Responsibilities
- Handle the death of an object and create new objects accordingly.
- Play audio events for ejection sounds and voices.
- Manage invulnerability time after ejection.

## Key Types
- `EjectPilotDieModuleData (struct)`: Stores data for creating objects when a pilot is ejected, including creation lists for air and ground scenarios and invulnerability time.
- `EjectPilotDie (class)`: Inherits from `DieModule` and implements the logic for ejecting a pilot.

## Key Functions
### EjectPilotDie::ejectPilot
- Purpose: Creates new objects based on the creation list and plays ejection sounds and voices.
- Calls:
  - `ObjectCreationList::create`
  - `AudioEventRTS::setPosition`
  - `AudioEventRTS::setPlayerIndex`
  - `TheAudio->addAudioEvent`

### EjectPilotDie::onDie
- Purpose: Checks if the death is applicable and calls `ejectPilot` with appropriate parameters.
- Calls:
  - `isDieApplicable`
  - `TheGameLogic->findObjectByID`
  - `getObject()->isSignificantlyAboveTerrain`
  - `ejectPilot`

## Globals
None

## Dependencies
- Includes: `PreRTS.h`, `Common/GameAudio.h`, `Common/Player.h`, `Common/ThingFactory.h`, `Common/ThingTemplate.h`, `Common/Xfer.h`, `GameLogic/GameLogic.h`, `GameLogic/Module/EjectPilotDie.h`, `GameLogic/ExperienceTracker.h`, `GameLogic/Object.h`, `GameLogic/ObjectCreationList
