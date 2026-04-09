# Generals/Code/GameEngine/Source/GameLogic/Object/Update/OCLUpdate.cpp

## Purpose
This file contains the implementation of the `OCLUpdate` class, which handles the periodic creation of objects based on an Object Creation List (OCL) for game entities.

## Responsibilities
- Manages the timing and execution of object creation from an OCL.
- Determines when to create new objects based on delays and conditions.
- Updates internal timers and checks game logic states.

## Key Types
- `OCLUpdateModuleData` (struct): Stores configuration data for OCL updates, including delay times and creation parameters.
- `OCLUpdate` (class): Handles the periodic creation of objects from an OCL based on specified delays and conditions.

## Key Functions
### update
- Purpose: Updates the module's state and creates objects if the conditions are met.
- Calls:
  - `shouldCreate`
  - `setNextCreationFrame`
  - `ObjectCreationList::create`

### shouldCreate
- Purpose: Checks if an object should be created based on current game frame and object status.
- Calls:
  - `TheGameLogic->getFrame`
  - `BitTest`

### setNextCreationFrame
- Purpose: Sets the next frame at which an object should be created, using a random delay within specified bounds.
- Calls:
  - `GameLogicRandomValue`
  - `TheGameLogic->getFrame`

## Globals
- None

## Dependencies
- Key includes and external symbols used but not defined here:
  - `PreRTS.h`
  - `Common/RandomValue.h`
  - `Common/Xfer.h`
  - `GameLogic/GameLogic.h`
  - `GameLogic/Object.h`
  - `GameLogic/ObjectCreationList.h`
  - `GameLogic/PartitionManager.h`
  - `GameLogic/Module/OCLUpdate.h`
  - `GameLogic/TerrainLogic
