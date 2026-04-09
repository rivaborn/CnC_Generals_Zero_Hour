# Generals/Code/GameEngine/Source/Common/System/BuildAssistant.cpp

## Purpose
This file contains the implementation of the `BuildAssistant` class, which manages building and selling objects in the game. It handles various tasks such as checking build feasibility, managing construction positions, and updating sell processes.

## Responsibilities
- Manage object construction and destruction.
- Check prerequisites for building units or structures.
- Handle the selling process of objects, including refunding money and animations.
- Clear obstacles during construction.
- Update the state of objects being sold.

## Key Types
- **SampleBuildData (Class)**: Stores data related to sample build locations.
- **ProductionCountData (Class)**: Used for counting units in production queues.
- **ObjectSellInfo (Class)**: Manages information about objects being sold.

## Key Functions
### isDozer
- Purpose: Determines if an object is a dozer.
- Calls: `obj->isKindOf(KINDOF_DOZER)`

### checkSampleBuildLocation
- Purpose: Not inferable from provided code snippet.
- Calls: Not visible in this file.

### countInProduction
- Purpose: Counts units of a given type in production queues for a player.
- Calls: `pui->countUnitTypeInQueue(productionCountData->type)`

## Globals
- **TheBuildAssistant (BuildAssistant \*)**: Singleton instance of the build assistant.
- **FRAMES_TO_ALLOW_SCAFFOLD (Real)**: Frames allowed for scaffold animation.
- **TOTAL_FRAMES_TO_SELL_OBJECT (Real)**: Total frames to sell an object.

## Dependencies
- Key includes:
  - "Common/BuildAssistant.h"
  - "Common/GlobalData.h"
  - "Common/Player.h"
  - "Common/ThingTemplate.h"
  - "GameLogic/AI.h"
  - "GameLogic/TerrainLogic.h"
  - "GameLogic/PartitionManager.h"
  - "GameClient/ControlBar.h"
  - "GameClient/Drawable.h"
  - "GameClient/InGameUI.h"
