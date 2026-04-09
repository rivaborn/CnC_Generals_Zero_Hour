# GeneralsMD/Code/GameEngine/Include/Common/IgnorePreferences.h

## Purpose
Header file defining the `IgnorePreferences` class for managing user ignore lists in the game.

## Responsibilities
- Manages ignore preferences for multiplayer users
- Provides methods to set and retrieve ignore status
- Inherits from `UserPreferences` base class

## Key Types
- `IgnorePrefMap` (Class): Map type for storing ignore preferences (Int to AsciiString)
- `IgnorePreferences` (Class): Class for handling ignore preferences

## Key Functions
### `IgnorePreferences()`
- Purpose: Constructor for IgnorePreferences class
- Calls: None

### `~IgnorePreferences()`
- Purpose: Destructor for IgnorePreferences class
- Calls: None

### `setIgnore()`
- Purpose: Sets ignore status for a specific user
- Calls: None

### `getIgnores()`
- Purpose: Retrieves the current ignore preferences map
- Calls: None

## Globals
None

## Dependencies
- `Common/UserPreferences.h` (UserPreferences base class)
- `std::map` (STL container)
- `Int`, `AsciiString`, `Bool` (game-defined types)
