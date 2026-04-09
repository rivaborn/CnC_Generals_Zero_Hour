# Generals/Code/GameEngine/Source/GameLogic/Object/Update/ProductionExitUpdate/QueueProductionExitUpdate.cpp

## Purpose
This file contains the implementation of `QueueProductionExitUpdate`, a class responsible for managing the exit process of produced units from production buildings in Command & Conquer Generals. It handles the positioning, orientation, and movement of newly created objects.

## Responsibilities
- Manage the exit delay between unit productions.
- Position and orient newly created units based on building orientation and configuration.
- Handle the reservation and unreservation of exit doors.
- Update the state to determine when a new unit can be exited.
- Provide methods for exiting units via budding or standard door exits.

## Key Types
- `QueueProductionExitUpdate` (Class): Manages the exit process of produced units from production buildings.

## Key Functions
### QueueProductionExitUpdate::exitObjectViaDoor
- Purpose: Exits a newly created object through a specified door, setting its position, orientation, and initial physics.
- Calls:
  - `getObject()`
  - `getTransformMatrix()`
  - `getOrientation()`
  - `setOrientation()`
  - `setPosition()`
  - `applyMotiveForce()`
  - `setPitchRate()`
  - `addObjectToPathfindMap()`
  - `snapPosition()`
  - `aiFollowExitProductionPath()`

### QueueProductionExitUpdate::getExitPosition
- Purpose: Retrieves the exit position for a newly created object.
- Calls:
  - `getObject()`
  - `getTransformMatrix()`

### QueueProductionExitUpdate::reserveDoorForExit
- Purpose: Reserves an exit door for a unit if available.
- Calls:
  - `isFreeToExit()`

### QueueProductionExitUpdate::unreserveDoorForExit
- Purpose: Unreserves an exit door after a unit has exited.

### QueueProductionExitUpdate::isFreeToExit
- Purpose: Determines if the production building is free to exit another unit.
- Calls:
  - `getObject()`

### QueueProductionExitUpdate::update
- Purpose: Updates the state of the exit process, reducing delay and checking if the building is free to exit a new unit.

### QueueProductionExitUpdate::exitObjectByBudding
- Purpose: Exits a newly created object by budding from an existing host object.
- Calls:
  - `getPosition()`
  - `getOrientation()`
  - `setLayer()`
  - `aiMoveToPosition()`

### QueueProductionExitUpdate::getNaturalRallyPoint
- Purpose: Retrieves the natural rally point for units, optionally offsetting it.
- Calls:
  - `getObject()`
  - `getTransformMatrix()`

## Globals
- None

## Dependencies
- Key includes and external symbols used but not defined here:
  - `PreRTS.h`
  - `Common
