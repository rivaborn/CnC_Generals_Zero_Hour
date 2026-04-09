# GeneralsMD/Code/GameEngine/Include/Common/ScoreKeeper.h

## Purpose
Header file for the ScoreKeeper class, which tracks player statistics and calculates scores in the game.

## Responsibilities
- Track financial transactions (money earned/spent)
- Count objects built/destroyed/lost/captured
- Calculate player scores based on statistics
- Support serialization for network play

## Key Types
- **ScoreKeeper (Class)**: Tracks player statistics and calculates scores.
- **ObjectCountMap (Class)**: Maps ThingTemplate to count for tracking specific object types.
- **ObjectCountMapIt (Class)**: Iterator for ObjectCountMap.

## Key Functions
### ScoreKeeper::calculateScore
- Purpose: Performs the equation to calculate the score.
- Calls: Not inferable.

### ScoreKeeper::addObjectBuilt
- Purpose: Adds an object to the built count.
- Calls: Not inferable.

### ScoreKeeper::addObjectDestroyed
- Purpose: Adds an object to the destroyed count.
- Calls: Not inferable.

### ScoreKeeper::xferObjectCountMap
- Purpose: Serializes/deserializes ObjectCountMap data.
- Calls: Not inferable.

## Globals
- **m_totalMoneyEarned (Int)**: Total money harvested/refined/received.
- **m_totalMoneySpent (Int)**: Total money spent on units/buildings/repairs.
- **m_totalUnitsDestroyed (Int[MAX_PLAYER_COUNT])**: Total enemy units killed per player.
- **m_objectsBuilt (ObjectCountMap)**: Count of objects built by type.

## Dependencies
- **Snapshot.h**: Base class for serialization.
- **Object**: Forward reference for game objects.
- **ThingTemplate**: Forward reference for object templates.
