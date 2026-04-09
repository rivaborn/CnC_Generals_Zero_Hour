# GeneralsMD/Code/GameEngine/Include/Common/PlayerList.h

## Purpose
Manages the list of game players and teams, providing access and relationship queries.

## Responsibilities
- Maintains player and team state
- Provides player lookup by index, name, or mask
- Handles player relationships (allies/enemies/neutral)
- Supports game state serialization (snapshot system)

## Key Types
- **PlayerList (Class)**: Singleton managing all players and teams
- **AllowPlayerRelationship (Enum)**: Bitmask flags for player relationships (same, allies, enemies, neutral)

## Key Functions
### `getPlayersWithRelationship`
- Purpose: Returns players with specified relationship to source player
- Calls: Not inferable

### `validateTeam`
- Purpose: Validates or creates a team for a given owner
- Calls: Not inferable

### `updateTeamStates`
- Purpose: Clears entered/exited flags on all teams
- Calls: Not inferable

## Globals
- **ThePlayerList (PlayerList*)**: Singleton instance of PlayerList

## Dependencies
- `SubsystemInterface`, `Snapshot`, `Player`, `Team`, `TeamFactory`
- `DataChunkInput`, `DataChunkOutput`, `DataChunkInfo` (forward declarations)
- `NameKeyGenerator`, `GameCommon` headers
