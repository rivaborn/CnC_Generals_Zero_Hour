# Generals/Code/GameEngine/Source/Common/RTS/ProductionPrerequisite.cpp

## Purpose
This file contains the implementation for managing production prerequisites in the Command & Conquer Generals game engine. It handles checking if a player meets the necessary conditions to produce or upgrade units, including required units and technologies.

## Responsibilities
- Manage prerequisite units and sciences.
- Resolve names of prerequisite units to their corresponding templates.
- Calculate the number of owned prerequisite units.
- Determine possible build facility templates based on prerequisites.
- Check if production prerequisites are satisfied by a player.
- Add unit prerequisites with optional "or" conditions.
- Generate a list of unsatisfied prerequisites for display.

## Key Types
- `ProductionPrerequisite` (Class): Manages production prerequisites, including units and sciences.
- `PrereqUnitRec` (Struct): Represents a prerequisite unit record with flags and associated template.

## Key Functions
### ProductionPrerequisite::resolveNames
- Purpose: Resolves the names of prerequisite units to their corresponding templates.
- Calls: 
  - `TheThingFactory->findTemplate`
  - `DEBUG_ASSERTCRASH`

### ProductionPrerequisite::calcNumPrereqUnitsOwned
- Purpose: Calculates the number of owned prerequisite units for a player.
- Calls: 
  - `player->countObjectsByThingTemplate`

### ProductionPrerequisite::getAllPossibleBuildFacilityTemplates
- Purpose: Retrieves all possible build facility templates based on prerequisites.
- Calls: None

### ProductionPrerequisite::getExistingBuildFacilityTemplate
- Purpose: Gets an existing build facility template that meets the prerequisites for a player.
- Calls: 
  - `player->countObjectsByThingTemplate`

### ProductionPrerequisite::isSatisfied
- Purpose: Checks if all production prerequisites are satisfied by a player.
- Calls: 
  - `player->hasScience`
  - `calcNumPrereqUnitsOwned`

### ProductionPrerequisite::addUnitPrereq (overloaded)
- Purpose: Adds a unit prerequisite with optional "or" conditions.
- Calls: None

### ProductionPrerequisite::getRequiresList
- Purpose: Generates a list of unsatisfied prerequisites for display.
- Calls: 
  - `player->countObjectsByThingTemplate`
  - `TheGameText->fetch`

## Globals
- None

## Dependencies
- Key includes:
  - "PreRTS.h"
  - "Common/ProductionPrerequisite.h"
  - "Common/Player.h"
  - "Common/ThingFactory.h"
  - "Common/ThingTemplate.h"
  - "GameLogic/Object.h"
  - "GameClient/Drawable.h"
  - "GameClient/GameText.h"

- External symbols used:
  - `TheThingFactory`
  - `TheGameText`
