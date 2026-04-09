# GeneralsMD/Code/GameEngine/Include/GameNetwork/GameInfo.h

## Purpose
Defines game session metadata, player slots, and game state management for Command & Conquer Generals.

## Responsibilities
- Manages game slots (players/AI/open slots)
- Tracks game settings (map, seed, superweapons)
- Handles game state transitions (in-game, in-progress)
- Provides serialization for game info

## Key Types
- **SlotState (Enum)**: Player slot states (open, closed, AI difficulty, human)
- **GameSlot (Class)**: Represents a player slot with state, color, position, and network info
- **GameInfo (Class)**: Core game session data including slots, map, and game options
- **SkirmishGameInfo (Class)**: Extends GameInfo for skirmish mode with snapshot support

## Key Functions
### `GameInfo::adjustSlotsForMap`
- Purpose: Adjusts slots based on map capacity and current players
- Calls: Not inferable

### `GameInfo::isSkirmish`
- Purpose: Determines if the game is a skirmish (1 human + 1+ AI)
- Calls: Not inferable

### `GameInfoToAsciiString`
- Purpose: Serializes GameInfo to a string
- Calls: Not inferable

### `ParseAsciiStringToGameInfo`
- Purpose: Deserializes string to GameInfo
- Calls: Not inferable

## Globals
- **TheGameInfo (GameInfo*)**: Global game info instance
- **TheSkirmishGameInfo (SkirmishGameInfo*)**: Global skirmish game info
- **TheChallengeGameInfo (SkirmishGameInfo*)**: Global challenge game info

## Dependencies
- `Common/Snapshot.h`, `Common/Money.h`
- `GameNetwork/NetworkDefs.h`, `GameNetwork/FirewallHelper.h`
- `UnicodeString`, `AsciiString`, `Xfer`, `Bool`, `Int`, `UnsignedInt`
