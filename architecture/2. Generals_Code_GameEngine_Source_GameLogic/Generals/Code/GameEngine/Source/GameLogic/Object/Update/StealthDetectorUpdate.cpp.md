# Generals/Code/GameEngine/Source/GameLogic/Object/Update/StealthDetectorUpdate.cpp

## Purpose
This file contains the implementation for the `StealthDetectorUpdate` class, which handles the detection of stealthed units in the game. It includes logic for checking stealth status, updating detection rates, and providing UI feedback when a unit is detected.

## Responsibilities
- Detects stealthed units within a specified range.
- Manages detection rates and update intervals.
- Provides audio and UI feedback upon detecting stealthed units.
- Handles particle effects and radar events for detected units.

## Key Types
- **StealthDetectorUpdateModuleData (Class):** Stores configuration data for the stealth detector, such as detection rate, range, and sound effects.
- **PartitionFilterStealthedOrStealthGarrisoned (Class):** Filters objects to detect those that are either stealthed or garrisoning stealth units.

## Key Functions
### buildFieldParse
- Purpose: Initializes field parsing for the module data.
- Calls: `UpdateModuleData::buildFieldParse`

### StealthDetectorUpdate
- Purpose: Constructor for the `StealthDetectorUpdate` class, initializes detection settings and wake frames.
- Calls: `getStealthDetectorUpdateModuleData`, `setWakeFrame`

### setSDEnabled
- Purpose: Enables or disables the stealth detector update module.
- Calls: `setWakeFrame`

### allow (PartitionFilterStealthedOrStealthGarrisoned)
- Purpose: Determines if an object is allowed to be detected based on its stealth status or garrisoning status.
- Calls: None

### update
- Purpose: Main update function that checks for stealthed units, provides feedback, and manages particle effects.
- Calls: `getStealthDetectorUpdateModuleData`, `iterateObjectsInRange`, `tryEvent`, `createEvent`, `addAudioEvent`, `message`, `markAsDetected`, `setHeatVisionOpacity`, `createParticleSystem`, `attachToDrawable`, `attachToObject`

### crc
- Purpose: Handles CRC operations for the module.
- Calls: `UpdateModule::crc`

### xfer
- Purpose: Handles data transfer (serialization/deserialization) for the module.
- Calls: `xferVersion`, `UpdateModule::xfer`, `xferBool`

### loadPostProcess
- Purpose: Performs post-load processing after deserialization.
- Calls: `UpdateModule::loadPostProcess`

## Globals
- None

## Dependencies
- Key includes:
  - "Common/MiscAudio.h"
  - "Common/Radar.h"
  - "Common/ThingTemplate.h"
  - "Common/Xfer.h"
  - "GameClient/Drawable.h"
  - "GameClient/GameText.h"
  - "GameClient/InGameUI.h"
  - "GameClient/ParticleSys.h"
  - "GameLogic/Damage.h"
