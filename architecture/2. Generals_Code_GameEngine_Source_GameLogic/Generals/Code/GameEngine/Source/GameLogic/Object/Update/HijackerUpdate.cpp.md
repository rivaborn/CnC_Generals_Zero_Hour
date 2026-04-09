# Generals/Code/GameEngine/Source/GameLogic/Object/Update/HijackerUpdate.cpp

## Purpose
This file implements the `HijackerUpdate` class, which manages the behavior of a hijacker object in the game. It ensures that the hijacker stays with their hijacked vehicle until it dies and then reverts to being a pedestrian hijacker.

## Responsibilities
- Manage the position synchronization between the hijacker and the hijacked vehicle.
- Handle the transition of the hijacker from being inside a vehicle to becoming a pedestrian again after the vehicle is destroyed.
- Update experience levels when the hijacker is in a vehicle.
- Manage the hijacker's visibility and collision status.

## Key Types
- `HijackerUpdate` (Class): Manages the hijacker's update logic.
- None

## Key Functions
### HijackerUpdate::update
- Purpose: Updates the hijacker's state, including position synchronization with the vehicle and handling post-vehicle destruction behavior.
- Calls:
  - `getObject()`
  - `getTargetObject()`
  - `setPosition()`
  - `isSignificantlyAboveTerrain()`
  - `getPosition()`
  - `getExperienceTracker()`
  - `setVeterancyLevel()`
  - `registerObject()`
  - `getDrawable()`
  - `setDrawableHidden()`
  - `clearStatus()`
  - `aiIdle()`
  - `findTemplate()`
  - `newObject()`
  - `addToContain()`

### HijackerUpdate::setTargetObject
- Purpose: Sets the target object (hijacked vehicle) and updates related state.
- Calls:
  - `getID()`
  - `getBehaviorModules()`
  - `getEjectPilotDieInterface()`

### HijackerUpdate::getTargetObject
- Purpose: Retrieves the current target object (hijacked vehicle).
- Calls:
  - `findObjectByID()`

## Globals
- None

## Dependencies
- Key includes and external symbols used but not defined here:
  - `PreRTS.h`
  - `Player.h`
  - `ThingFactory.h`
  - `ThingTemplate.h`
  - `Xfer.h`
  - `Drawable.h`
  - `Object.h`
  - `HijackerUpdate.h`
  - `AIUpdate.h`
  - `GameLogic.h`
  - `PartitionManager.h`
  - `EjectPilotDie.h`
  - `ContainModule.h`
  - `ExperienceTracker.h`
