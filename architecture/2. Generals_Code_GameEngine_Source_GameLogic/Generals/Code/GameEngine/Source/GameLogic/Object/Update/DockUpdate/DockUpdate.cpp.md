# Generals/Code/GameEngine/Source/GameLogic/Object/Update/DockUpdate/DockUpdate.cpp

## Purpose
This file contains the implementation of the `DockUpdate` class, which manages docking behavior for game objects in Command & Conquer Generals.

## Responsibilities
- Manages docking positions and states.
- Handles object approach, entry, and exit from docking points.
- Updates model conditions related to docking.
- Loads and saves docking position data.

## Key Types
- `DockUpdateModuleData (struct)`: Stores configuration data for docking modules.
- `DockUpdate (class)`: Manages the docking logic for game objects.

## Key Functions
### DockUpdate::DockUpdate
- Purpose: Initializes a new instance of the `DockUpdate` class.
- Calls:
  - `loadDockPositions`

### DockUpdate::isClearToApproach
- Purpose: Checks if an object can approach a docking point.
- Calls: None

### DockUpdate::reserveApproachPosition
- Purpose: Reserves an approach position for an object.
- Calls:
  - `loadDockPositions`
  - `computeApproachPosition`

### DockUpdate::advanceApproachPosition
- Purpose: Advances an object to the next approach position.
- Calls:
  - `loadDockPositions`
  - `computeApproachPosition`

### DockUpdate::isClearToEnter
- Purpose: Checks if an object can enter a docking point.
- Calls: None

### DockUpdate::getEnterPosition
- Purpose: Retrieves the entry position for an object.
- Calls:
  - `loadDockPositions`
  - `getObject()->convertBonePosToWorldPos`

### DockUpdate::onApproachReached
- Purpose: Marks an approach position as reached by an object.
- Calls: None

### DockUpdate::onEnterReached
- Purpose: Handles the event when an object enters a docking point.
- Calls:
  - `clearAndSetModelConditionFlags`
  - `getObject()->convertBonePosToWorldPos`

### DockUpdate::update
- Purpose: Updates the docking state of the object.
- Calls:
  - `TheGameLogic->findObjectByID`
  - `getObject()->isKindOf`
  - `getDrawable()->getModelConditionFlags`
  - `clearModelConditionFlags`

## Globals
- None

## Dependencies
- Key includes and external symbols used but not defined here:
  - `PreRTS.h`
  - `Common/Debug.h`
  - `Common/Xfer.h`
  - `GameClient/Drawable.h`
  - `GameLogic/GameLogic.h`
  - `GameLogic/Object.h`
  - `GameLogic/PartitionManager.h`
  - `GameLogic/Module/DockUpdate.h`
