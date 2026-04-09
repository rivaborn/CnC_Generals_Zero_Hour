# Generals/Code/GameEngine/Source/GameLogic/Object/Object.cpp

## Purpose
This file contains the implementation of the `Object` class, which represents a basic game object in Command & Conquer Generals. It handles various aspects such as initialization, behavior modules, and interactions with other objects.

## Responsibilities
- Manage object creation and destruction.
- Handle behavior modules and their interactions.
- Provide methods for object status checks and updates.
- Implement defecting logic for team changes.
- Manage radar visibility and priority.

## Key Types
- `Object` (Class): Represents a game object with various attributes and behaviors.
- `BehaviorModule` (Class): Base class for different behavior modules attached to objects.
- `SpecialPowerUpdateInterface` (Interface): Interface for special power updates.
- `SpawnBehaviorInterface` (Interface): Interface for spawn behavior.

## Key Functions
### Object::Object
- Purpose: Constructor for the `Object` class, initializes various attributes and modules.
- Calls:
  - `newInstance(SightingInfo)`
  - `TheGameLogic->allocateObjectID()`
  - `TheModuleFactory->newModule`

### addIcon
- Purpose: Adds an icon at a specified position in the game world.
- Calls: None

### localIsHero
- Purpose: Checks if an object is considered a hero.
- Calls: None

### isPosDifferent
- Purpose: Compares two positions to determine if they are different.
- Calls: None

### isAngleDifferent
- Purpose: Compares two angles to determine if they are different.
- Calls: None

## Globals
- `s_allWeaponFireFlags` (ModelConditionFlags[]): Array of weapon fire flags.

## Dependencies
- Key includes:
  - "Common/BitFlagsIO.h"
  - "Common/BuildAssistant.h"
  - "GameLogic/Object.h"
  - "GameLogic/Module/AIUpdate.h"
  - "GameLogic/Module/BehaviorModule.h"
  - "GameLogic/PartitionManager.h"
  - "GameLogic/ScriptEngine.h"
- External symbols:
  - `addIcon`
  - `TheGameLogic`
  - `ThePlayerList`
  - `TheAI`
  - `TheModuleFactory`
  - `TheRadar`
  - `TheAudio`
  - `TheControlBar`
