# GeneralsMD/Code/GameEngine/Include/GameNetwork/GameSpy/PersistentStorageDefs.h

## Purpose
Defines interfaces and types for GameSpy persistent storage functionality in Generals Zero Hour.

## Responsibilities
- Declares locale type enum for player regions
- Exposes functions for handling persistent storage responses
- Provides APIs for updating player stats and UI elements
- Defines interfaces for player info management

## Key Types
- LocaleType (Enum): Represents player locale/region identifiers (0-37)

## Key Functions
### HandlePersistentStorageResponses
- Purpose: Processes incoming persistent storage responses from GameSpy.
- Calls: Not inferable

### UpdateLocalPlayerStats
- Purpose: Updates the local player's statistics in persistent storage.
- Calls: Not inferable

### SetLookAtPlayer
- Purpose: Sets the player to "look at" (focus on) another player by ID and nickname.
- Calls: Not inferable

### PopulatePlayerInfoWindows
- Purpose: Fills player info windows with data from persistent storage.
- Calls: Not inferable

## Globals
None

## Dependencies
- AsciiString (external type)
- Int (external type)
- GameSpy persistent storage system (external)
