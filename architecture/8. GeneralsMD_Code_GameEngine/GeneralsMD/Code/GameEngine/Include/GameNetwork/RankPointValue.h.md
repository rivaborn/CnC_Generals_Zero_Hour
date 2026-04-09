# GeneralsMD/Code/GameEngine/Include/GameNetwork/RankPointValue.h

## Purpose
Defines rank-related data structures and functions for player progression in the game.

## Responsibilities
- Declares rank enumeration and associated data structures
- Provides function declarations for rank calculation and image lookup
- Defines global rank point values structure

## Key Types
- RankPoints (Struct): Stores rank thresholds and multipliers for progression
- (anonymous enum): Military rank levels from Private to Commander-in-Chief

## Key Functions
### CalculateRank
- Purpose: Determines player rank based on stats
- Calls: Not inferable

### GetFavoriteSide
- Purpose: Identifies player's preferred side
- Calls: Not inferable

### LookupSmallRankImage
- Purpose: Retrieves rank image based on side and rank
- Calls: Not inferable

## Globals
- TheRankPointValues (RankPoints*): Global pointer to rank point configuration

## Dependencies
- Image class (forward reference)
- PSPlayerStats class (forward reference)
