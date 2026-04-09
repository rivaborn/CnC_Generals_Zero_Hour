# GeneralsMD/Code/GameEngine/Source/GameLogic/Object/Update/StealthDetectorUpdate.cpp

## Purpose
Handles stealth detection logic for objects in the game, including visual/audio feedback and particle effects.

## Responsibilities
- Detects stealthed objects within range
- Manages detection status and UI feedback
- Handles particle effects and audio cues for detection
- Supports detection while garrisoned/transported (configurable)

## Key Types
- **StealthDetectorUpdateModuleData (Class)**: Module data for stealth detector configuration
- **PartitionFilterStealthedOrStealthGarrisoned (Class)**: Filter for stealthed objects or those garrisoning stealthed units

## Key Functions
### StealthDetectorUpdate::update
- Purpose: Main detection update loop
- Calls: `ThePartitionManager->iterateObjectsInRange`, `stealth->markAsDetected`, `TheRadar->tryEvent`, `TheAudio->addAudioEvent`, `TheInGameUI->message`

### PartitionFilterStealthedOrStealthGarrisoned::allow
- Purpose: Determines if an object should be considered for stealth detection
- Calls: `objOther->getStatusBits`, `objOther->getContain`

## Globals
- None

## Dependencies
- `PartitionManager.h`, `StealthUpdate.h`, `ContainModule.h`, `Radar.h`, `Audio.h`, `InGameUI.h`, `ParticleSys.h`, `Xfer.h`
