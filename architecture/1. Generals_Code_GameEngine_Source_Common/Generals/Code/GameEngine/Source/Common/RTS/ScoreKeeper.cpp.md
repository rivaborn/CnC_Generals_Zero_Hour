# Generals/Code/GameEngine/Source/Common/RTS/ScoreKeeper.cpp

## Purpose
The `ScoreKeeper` class maintains accurate counts for various game statistics, such as units and buildings built, captured, and destroyed, for each player. This information is used to display scores on the score screen and observer screen.

## Responsibilities
- Track and update scores based on game events.
- Maintain counts of units and buildings built, captured, and destroyed.
- Calculate the current score for a player.
- Handle serialization and deserialization of score data.

## Key Types
- `ScoreKeeper` (Class): Manages scoring for a player.
- `KindOfMaskType` (Struct/Enum): Used to filter object types based on their kind.

## Key Functions
### reset
- Purpose: Initializes the score keeper with default values.
- Calls: None

### addObjectBuilt
- Purpose: Increments counts for built objects.
- Calls: `isScoringEnabled`, `isKindOfMulti`

### getTotalUnitsBuilt
- Purpose: Returns the total number of units built that match a given mask.
- Calls: `isKindOfMulti`

### removeObjectBuilt
- Purpose: Decrements counts for built objects.
- Calls: `isScoringEnabled`, `isKindOfMulti`

### addObjectCaptured
- Purpose: Increments counts for captured objects.
- Calls: `isScoringEnabled`, `isKindOf`

### addObjectDestroyed
- Purpose: Increments counts for destroyed objects and updates the score.
- Calls: `isScoringEnabled`, `isKindOfMulti`, `testStatus`

### addObjectLost
- Purpose: Increments counts for lost objects.
- Calls: `isScoringEnabled`, `isKindOfMulti`, `testStatus`

### calculateScore
- Purpose: Calculates and returns the current score based on various statistics.
- Calls: None

## Globals
- `scoringBuildingMask` (KindOfMaskType): Mask for scoring buildings.
- `scoringBuildingDestroyMask` (KindOfMaskType): Mask for scoring building destruction.
- `scoringBuildingCreateMask` (KindOfMaskType): Mask for scoring building creation.

## Dependencies
- Key includes: "PreRTS.h", "Common/GameState.h", "Common/KindOf.h", "Common/Player.h", "Common/ScoreKeeper.h", "Common/ThingFactory.h", "Common/ThingTemplate.h", "Common/Xfer.h", "GameLogic/Object.h", "GameLogic/GameLogic.h"
- External symbols: `TheGameLogic`, `TheThingFactory`
