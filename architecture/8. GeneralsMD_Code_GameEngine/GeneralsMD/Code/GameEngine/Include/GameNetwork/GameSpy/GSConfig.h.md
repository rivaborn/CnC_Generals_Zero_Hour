# GeneralsMD/Code/GameEngine/Include/GameNetwork/GameSpy/GSConfig.h

## Purpose
Defines the GameSpy configuration interface for online game settings.

## Responsibilities
- Declares the `GameSpyConfigInterface` abstract class with pure virtual methods for GameSpy settings.
- Provides access to ping servers, QM (Quick Match) settings, player info, mangler locations, and leftover config parsing.
- Manages the global `TheGameSpyConfig` instance.

## Key Types
- **GameSpyConfigInterface (Class)**: Abstract interface for GameSpy configuration.

## Key Functions
### `getPingServers`
- Purpose: Retrieves the list of ping servers.
- Calls: None.

### `getQMMaps`
- Purpose: Retrieves the list of Quick Match maps.
- Calls: None.

### `getPointsForRank`
- Purpose: Gets the points required for a given rank.
- Calls: None.

### `getManglerLocation`
- Purpose: Retrieves the host and port for a mangler location by index.
- Calls: None.

### `create`
- Purpose: Factory method to create a `GameSpyConfigInterface` instance.
- Calls: None.

## Globals
- **TheGameSpyConfig (GameSpyConfigInterface*)**: Global pointer to the GameSpy configuration instance.

## Dependencies
- `Common/AsciiString.h`
- `Common/STLTypedefs.h`
- `std::list`, `Int`, `Bool`, `UnsignedShort` (from STLTypedefs)
