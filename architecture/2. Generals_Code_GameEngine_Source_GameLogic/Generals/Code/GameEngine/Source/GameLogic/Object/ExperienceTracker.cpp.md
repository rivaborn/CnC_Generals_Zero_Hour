# Generals/Code/GameEngine/Source/GameLogic/Object/ExperienceTracker.cpp

## Purpose
This file implements the `ExperienceTracker` class, which manages experience points for game objects to track their veterancy levels.

## Responsibilities
- Track and manage experience points for game objects.
- Determine if an object can gain experience or reach a certain level.
- Handle experience point distribution to other objects if configured.
- Update veterancy levels based on accumulated experience.
- Serialize and deserialize experience data for network synchronization.

## Key Types
- `ExperienceTracker` (Class): Manages experience points and veterancy levels for game objects.
- `VeterancyLevel` (Enum): Represents different veterancy levels an object can achieve.

## Key Functions
### getExperienceValue
- Purpose: Returns the experience value of killing a specific object.
- Calls: 
  - `Object::getRelationship`
  - `ThingTemplate::getExperienceValue`

### isTrainable
- Purpose: Checks if the object can gain experience points.
- Calls: 
  - `ThingTemplate::isTrainable`

### addExperiencePoints
- Purpose: Adds experience points to the object and updates its veterancy level if necessary.
- Calls: 
  - `Object::getExperienceTracker`
  - `GameLogic::findObjectByID`
  - `Object::onVeterancyLevelChanged`

### setMinVeterancyLevel
- Purpose: Sets the minimum veterancy level for the object.
- Calls: 
  - `ThingTemplate::getExperienceRequired`
  - `Object::onVeterancyLevelChanged`

### xfer
- Purpose: Serializes and deserializes experience data for network synchronization.
- Calls: 
  - `Xfer::xferInt`
  - `Xfer::xferUser`
  - `Xfer::xferObjectID`
  - `Xfer::xferReal`

## Globals
- None

## Dependencies
- Key includes:
  - "Common/Xfer.h"
  - "Common/ThingTemplate.h"
  - "GameLogic/ExperienceTracker.h"
  - "GameLogic/GameLogic.h"
  - "GameLogic/Object.h"

- External symbols used but not defined here:
  - `Object`
  - `VeterancyLevel`
  - `LEVEL_REGULAR`, `LEVEL_LAST`, `LEVEL_COUNT`
  - `INVALID_ID`
  - `ALLIES`
  - `TheGameLogic`
