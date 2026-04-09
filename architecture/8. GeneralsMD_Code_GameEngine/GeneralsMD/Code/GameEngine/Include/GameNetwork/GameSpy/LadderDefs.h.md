# GeneralsMD/Code/GameEngine/Include/GameNetwork/GameSpy/LadderDefs.h

## Purpose
Defines data structures and interfaces for managing online ladder systems in Generals Zero Hour.

## Responsibilities
- Declares `LadderInfo` to store ladder configuration data.
- Provides `LadderList` for managing collections of ladders.
- Exposes global `TheLadderList` for ladder access.
- Defines ladder categorization (local, special, standard).

## Key Types
- **LadderInfo (Class)**: Stores ladder metadata (name, rules, maps, factions, etc.).
- **LadderInfoList (Typedef)**: `std::list<LadderInfo *>` for ladder collections.
- **LadderList (Class)**: Manages ladder lists and lookup functionality.
- **GameWindow (Class)**: Forward declaration (external UI dependency).

## Key Functions
### `LadderList::findLadder`
- Purpose: Locates a ladder by address and port.
- Calls: Not inferable.

### `LadderList::findLadderByIndex`
- Purpose: Retrieves a ladder by its index (excluding local ladders).
- Calls: Not inferable.

### `LadderList::loadLocalLadders`
- Purpose: Loads local ladder configurations.
- Calls: Not inferable.

### `LadderList::checkLadder`
- Purpose: Validates a ladder configuration file.
- Calls: Not inferable.

## Globals
- **TheLadderList (LadderList *)**: Global instance for ladder management.

## Dependencies
- `Common/UnicodeString.h`, `Common/AsciiString.h`, `Common/STLTypedefs.h`
- `std::list` from STL
- `GameWindow` (forward-declared)
