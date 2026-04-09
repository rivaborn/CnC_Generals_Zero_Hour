# GeneralsMD/Code/GameEngine/Include/GameNetwork/LANGameInfo.h

## Purpose
Defines classes and functions for managing LAN game information, including game slots, player data, and game options.

## Responsibilities
- Define `LANGameSlot` and `LANGameInfo` classes for LAN game state management
- Provide functions for displaying LAN game lists, slots, and options
- Handle game options serialization (generate/parse strings)
- Manage player connections and timeouts

## Key Types
- **LANGameSlot (Class)**: Represents a slot in a LAN game, holding player info and connection state
- **LANGameInfo (Class)**: Manages overall LAN game state, including slots, map, seed, and game name
- **GameWindow (Class)**: Forward declaration for UI window handling (not defined here)

## Key Functions
### LANDisplayGameList
- Purpose: Displays a list of LAN games in a UI listbox
- Calls: None visible in header

### GenerateGameOptionsString
- Purpose: Serializes game options into a string
- Calls: None visible in header

### ParseGameOptionsString
- Purpose: Deserializes game options from a string into a LANGameInfo object
- Calls: None visible in header

## Globals
- None

## Dependencies
- `GameNetwork/GameInfo.h` (base class)
- `GameNetwork/LANPlayer.h` (player data)
- `UnicodeString`, `AsciiString`, `Bool`, `Int`, `UnsignedInt` (primitive types)
