# Generals/Code/GameEngine/Source/GameLogic/Object/Update/FlammableUpdate.cpp

## Purpose
This file contains the implementation of the `FlammableUpdate` class, which manages the flammable and burned statuses of game objects, including their effects such as damage over time and sound playback.

## Responsibilities
- Manage the flammable status of an object.
- Handle the transition between different states (normal, aflame, burned).
- Apply flame damage to the object periodically.
- Play burning sounds when applicable.

## Key Types
- `FlammableUpdateModuleData` (struct): Stores configuration data for flammable behavior.
- `FlammableUpdate` (class): Manages the flammable status and its effects on an object.

## Key Functions
### FlammableUpdate::onDamage
- Purpose: Handles damage events, checking if they should cause the object to catch fire.
- Calls:
  - `getFlammableUpdateModuleData()`
  - `tryToIgnite()`

### FlammableUpdate::update
- Purpose: Updates the flammable status of the object, including transitioning states and applying damage.
- Calls:
  - `doAflameDamage()`
  - `startBurningSound()`
  - `stopBurningSound()`
  - `calcSleepTime()`

### FlammableUpdate::tryToIgnite
- Purpose: Attempts to ignite the object if it is not already aflame.
- Calls:
  - `getObject()->setStatus()`
  - `getObject()->getBodyModule()->setAflame()`
  - `getObject()->setModelConditionState()`
  - `startBurningSound()`

### FlammableUpdate::doAflameDamage
- Purpose: Applies flame damage to the object.
- Calls:
  - `getObject()->attemptDamage()`

### FlammableUpdate::startBurningSound
- Purpose: Starts playing the burning sound for the object.
- Calls:
  - `TheAudio->addAudioEvent()`

### FlammableUpdate::stopBurningSound
- Purpose: Stops the burning sound for the object.
- Calls:
  - `TheAudio->removeAudioEvent()`

## Globals
None

## Dependencies
- Key includes and external symbols used but not defined here:
  - `PreRTS.h`
  - `Common/AudioEventRTS.h`
  - `Common/GameAudio.h`
  - `Common/Xfer.h`
  - `GameLogic/GameLogic.h`
  - `GameLogic/Object.h`
  - `GameLogic/Module/BodyModule.h`
  - `GameLogic/Module/FlammableUpdate.h`
  - `GameLogic/Module/FireSpreadUpdate.h`
