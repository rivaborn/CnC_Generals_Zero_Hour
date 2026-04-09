# Generals/Code/GameEngine/Source/GameLogic/Object/Update/StructureCollapseUpdate.cpp

## Purpose
This file contains the implementation for the `StructureCollapseUpdate` class, which handles the collapse logic of structures in the game.

## Responsibilities
- Manages the collapse state and timing of structures.
- Parses configuration data from INI files.
- Handles visual effects and object creation lists during different phases of the collapse.
- Updates the structure's position and orientation during the collapse process.

## Key Types
- `StructureCollapseUpdate` (Class): Manages the collapse logic for a structure.
- `StructureCollapseUpdateModuleData` (Struct): Holds configuration data for the collapse update module.
- `StructureCollapsePhaseType` (Enum): Defines different phases of the collapse process.

## Key Functions
### parseFX
- Purpose: Parses FX lists from an INI file and associates them with collapse phases.
- Calls: `INI::scanIndexList`, `TheFXListStore->findFXList`

### parseOCL
- Purpose: Parses Object Creation Lists (OCLs) from an INI file and associates them with collapse phases.
- Calls: `INI::scanIndexList`, `TheObjectCreationListStore->findObjectCreationList`

### beginStructureCollapse
- Purpose: Initiates the structure collapse process.
- Calls: `GameLogicRandomValue`, `doPhaseStuff`

### onDie
- Purpose: Handles the death of a structure and begins its collapse if applicable.
- Calls: `getAIUpdateInterface`, `TheGameLogic->deselectObject`, `beginStructureCollapse`

### update
- Purpose: Updates the structure's state during the collapse process.
- Calls: `GameLogicRandomValue`, `doPhaseStuff`, `doCollapseDoneStuff`

### doPhaseStuff
- Purpose: Executes visual effects and object creation lists for a given collapse phase.
- Calls: `buildNonDupRandomIndexList`, `FXList::doFXPos`, `ObjectCreationList::create`

## Globals
- `MAX_IDX` (Int): Maximum index value used in certain functions.
- `TheStructureCollapsePhaseNames` (const char*[]): Array of strings representing collapse phases.

## Dependencies
- Key includes: "PreRTS.h", "Common/Thing.h", "Common/ThingTemplate.h", "Common/INI.h", "GameClient/FXList.h", "GameLogic/GameLogic.h", "GameLogic/ObjectCreationList.h"
- External symbols used: `TheFXListStore`, `TheObjectCreationListStore`, `TheGameLogic`, `TheGlobalData`
