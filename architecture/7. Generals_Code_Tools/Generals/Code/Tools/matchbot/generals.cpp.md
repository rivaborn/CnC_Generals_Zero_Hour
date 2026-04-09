# Generals/Code/Tools/matchbot/generals.cpp

## Purpose
Implements the matchmaking system for Command & Conquer Generals, handling player matching, ladder management, and match notifications.

## Responsibilities
- Manages player user data and matchmaking state
- Implements matching algorithms based on player attributes
- Handles GameSpy peer messages for matchmaking
- Manages ladder and non-ladder player pools
- Sends match notifications to players

## Key Types
- GeneralsUser (Class): Represents a player with matchmaking attributes
- GeneralsMatcher (Class): Core matchmaking logic and player management
- GeneralsClientMatcher (Class): Client-side matchmaking interface
- MapBitSet (Type): Bit set for map selection tracking

## Key Functions
### intToString
- Purpose: Converts integer to string representation
- Calls: None

### uintToString
- Purpose: Converts unsigned integer to string representation
- Calls: None

### MapSetUnion
- Purpose: Performs bitwise union of two map bit sets
- Calls: None

### MapSetCount
- Purpose: Counts set bits in a map bit set
- Calls: None

### calcPingDelta
- Purpose: Calculates ping difference between two players
- Calls: None

### sendMatchInfo
- Purpose: Sends match notification to players
- Calls: MapSetUnion, MapSetCount, intToString, uintToString

### handleUserInfo
- Purpose: Processes player connection info
- Calls: findUser, addUserInLadder, addNonLadderUser

## Globals
- MaxPingValue (const int): Maximum ping value constant

## Dependencies
- Key includes: tcp.h, wdebug.h, mydebug.h, ghttp/ghttp.h, generals.h, global.h
- External symbols: Global.config, Global.rnd, time(), sqrt()
