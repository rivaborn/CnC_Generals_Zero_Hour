# GeneralsMD/Code/GameEngine/Source/Common/RTS/ScoreKeeper.cpp

## Purpose
Manages player statistics for scoring in the game, tracking units, buildings, and resources.

## Responsibilities
- Tracks units/structures built, destroyed, lost, and captured
- Calculates player scores based on game events
- Serializes/deserializes score data for save/load
- Filters scoring based on object kind masks

## Key Types
- **ScoreKeeper (Class)**: Maintains player score statistics
- **ObjectCountMap (Type)**: Maps ThingTemplate to count (std::map)
- **KindOfMaskType (Type)**: Bitmask for object kind filtering

## Key Functions
### `addObjectBuilt`
- Purpose: Increment counters when an object is built
- Calls: `TheGameLogic->isScoringEnabled()`, `getTemplate()`, `isKindOfMulti`, `isKindOf`

### `addObjectDestroyed`
- Purpose: Track destroyed objects per player
- Calls: `TheGameLogic->isScoringEnabled()`, `getControllingPlayer()`, `getPlayerIndex()`, `getTemplate()`, `isKindOfMulti`, `isKindOf`, `testStatus`

### `calculateScore`
- Purpose: Compute total score from tracked statistics
- Calls: None directly (uses member variables)

### `xferObjectCountMap`
- Purpose: Serialize/deserialize object count maps
- Calls: `TheThingFactory->findTemplate()`, `xfer->xferAsciiString`, `xfer->xferInt`

## Globals
- **scoringBuildingMask (KindOfMaskType)**: Filters structure kinds for scoring
- **scoringBuildingDestroyMask (KindOfMaskType)**: Filters destroyable structures
- **scoringBuildingCreateMask (KindOfMaskType)**: Filters creatable structures

## Dependencies
- `PreRTS.h`, `GameState.h`, `KindOf.h`, `Player.h`, `ScoreKeeper.h`, `ThingFactory.h`, `ThingTemplate.h`, `Xfer.h`
- `Object.h`, `GameLogic.h`
- `TheGameLogic`, `TheThingFactory` (globals)
