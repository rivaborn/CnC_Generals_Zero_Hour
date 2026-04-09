# Generals/Code/Tools/matchbot/generals.h

## Purpose
Header file defining classes and types for the Generals matchmaking system, including user management and ladder matching logic.

## Responsibilities
- Declares `GeneralsUser` class for player data and status
- Defines `GeneralsMatcher` class for handling matchmaking logic
- Provides `GeneralsClientMatcher` for client-side matching
- Contains utility types like `UserMap` and `LadderMap`
- Declares match status enums and ping calculation structures

## Key Types
- `MapBitSet` (typedef): Vector of booleans for map availability tracking
- `UserStatus` (enum): Player matchmaking states (invalid, in channel, working, matched)
- `GeneralsUser` (class): Represents a player with points, ping, maps, and match status
- `UserMap` (typedef): Maps usernames to `GeneralsUser` objects
- `LadderMap` (typedef): Maps ladder IDs to `UserMap` instances
- `GeneralsMatcher` (class): Core matchmaking logic handler
- `GeneralsClientMatcher` (class): Client-side matching implementation

## Key Functions
### `computeMatchFitness`
- Purpose: Calculate match quality between two players
- Calls: Not inferable

### `checkMatches`
- Purpose: Periodically evaluate and create matches
- Calls: `checkMatchesInUserMap`, `sendMatchInfo`

### `handlePlayerJoined`
- Purpose: Process new player connections
- Calls: `addUser`, `addUserInLadder`

### `handlePlayerLeft`
- Purpose: Handle player disconnections
- Calls: `removeUser`, `removeUserInLadder`

## Globals
- `weightLowPing` (int): Weight for ping in matchmaking
- `weightAvgPoints`
