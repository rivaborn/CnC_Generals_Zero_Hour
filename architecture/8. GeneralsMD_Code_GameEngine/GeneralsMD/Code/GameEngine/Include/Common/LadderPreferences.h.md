# GeneralsMD/Code/GameEngine/Include/Common/LadderPreferences.h

## Purpose
Defines classes for managing ladder game preferences, including saving/loading ladder server connections.

## Responsibilities
- Stores ladder server connection details (name, address, port, last play date)
- Manages a map of recent ladder servers
- Provides methods to load/save ladder preferences
- Tracks recently played ladder servers

## Key Types
- **LadderPref (Class)**: Represents a ladder server connection with name, address, port, and last play date.
- **LadderPrefMap (Class)**: Typedef for `std::map<time_t, LadderPref>` to store ladder servers by last play date.
- **LadderPreferences (Class)**: Manages ladder preferences, inheriting from `UserPreferences`.

## Key Functions
### `LadderPref::operator==`
- Purpose: Compares two `LadderPref` objects for equality based on address and port.
- Calls: None.

### `LadderPreferences::loadProfile`
- Purpose: Loads ladder preferences for a specific profile.
- Calls: Not inferable (implementation in .cpp).

### `LadderPreferences::write`
- Purpose: Writes ladder preferences to storage.
- Calls: Not inferable (implementation in .cpp).

### `LadderPreferences::getRecentLadders`
- Purpose: Returns the map of recent ladder servers.
- Calls: None.

### `LadderPreferences::addRecentLadder`
- Purpose: Adds a ladder server to the recent ladders list.
- Calls: None.

## Globals
- None.

## Dependencies
- `Common/UserPreferences.h` (base class)
- `std::map` (STL)
- `UnicodeString`, `AsciiString` (string types)
- `time_t` (C standard library)
