# GeneralsMD/Code/GameEngine/Include/GameClient/GameText.h

## Purpose
Defines the `GameTextInterface` abstract class for localized text management in the game.

## Responsibilities
- Declares the interface for fetching localized text strings.
- Provides methods for loading map-specific text files.
- Manages string labels and their Unicode representations.
- Supports querying strings by label prefix.

## Key Types
- `AsciiString` (Class): Represents ASCII string data.
- `UnicodeString` (Class): Represents Unicode string data.
- `AsciiStringVec` (Class): Vector of `AsciiString` objects.
- `GameTextInterface` (Class): Abstract interface for localized text operations.

## Key Functions
### `CreateGameTextInterface`
- Purpose: Factory function to create a `GameTextInterface` instance.
- Calls: Not inferable.

## Globals
- `TheGameText` (GameTextInterface*): Global pointer to the game text interface instance.

## Dependencies
- `<vector>` (C++ STL)
- `SubsystemInterface` (base class)
- `AsciiString`, `UnicodeString` (forward-declared classes)
