# Generals/Code/GameEngine/Source/GameLogic/Object/Die/CreateCrateDie.cpp

## Purpose
This file implements the `CreateCrateDie` module, which handles the creation of crates upon an object's death based on certain conditions.

## Responsibilities
- Handles the logic for creating crates when an object dies.
- Checks various conditions such as killer type, veterancy level, and science requirements.
- Randomly selects a crate to create based on weighted probabilities.

## Key Types
- `CreateCrateDie` (Class): Manages the creation of crates upon an object's death.
- `CreateCrateDieModuleData` (Struct): Stores configuration data for crate creation conditions.

## Key Functions
### CreateCrateDie::onDie
- Purpose: Determines if a crate should be created when an object dies.
- Calls:
  - `isDieApplicable`
  - `findObjectByID`
  - `getRelationship`
  - `testCreationChance`
  - `testVeterancyLevel`
  - `testKillerType`
  - `testKillerScience`
  - `createCrate`

### CreateCrateDie::testCreationChance
- Purpose: Checks if a crate should be created based on a random chance.
- Calls:
  - `GameLogicRandomValueReal`

### CreateCrateDie::testVeterancyLevel
- Purpose: Compares the object's veterancy level with the required level for crate creation.
- Calls:
  - `getVeterancyLevel`

### CreateCrateDie::testKillerType
- Purpose: Checks if the killer type matches the required type for crate creation.
- Calls:
  - `isKindOfMulti`

### CreateCrateDie::testKillerScience
- Purpose: Checks if the killer's player has the required science for crate creation.
- Calls:
  - `hasScience`

### CreateCrateDie::createCrate
- Purpose: Creates a crate at a random position around the object's death location.
- Calls:
  - `findTemplate`
  - `newObject`
  - `setPosition`
  - `setOrientation`
  - `setLayer`
  - `getDrawable`
  - `setTerrainDecal`
  - `setTerrainDecalSize`
  - `setTerrainDecalFadeTarget`

## Globals
- None

## Dependencies
- Includes:
  - "PreRTS.h"
  - "Common/PlayerList.h"
  - "Common/Player.h"
  - "Common/RandomValue.h"
  - "Common/ThingFactory.h"
  - "Common/ThingTemplate.h"
  - "Common/Xfer.h"
  - "GameLogic/CrateSystem.h"
  - "GameLogic/ExperienceTracker.h"
  - "GameLogic/GameLogic.h"
  - "GameLogic/Object.h"
  - "GameLogic/PartitionManager.h"
  - "Game
