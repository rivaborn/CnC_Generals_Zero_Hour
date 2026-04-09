# GeneralsMD/Code/GameEngine/Include/GameLogic/RankInfo.h - Enhanced Analysis

## Architectural Role
This file defines the data model and interface for player progression (ranks) in the game. It bridges the game logic layer with the INI-based configuration system, enabling rank definitions to be loaded and queried at runtime.

## Cross-References
### Incoming
- Likely called by `Player` class for rank progression checks
- Used by UI systems for displaying rank information
- Referenced by `GameLogic` subsystem for skill point calculations

### Outgoing
- Depends on `INI` parsing infrastructure for configuration loading
- Uses `Science` system for granting research points
- Relies on `UnicodeString` for localized rank names

## Design Patterns
- **Singleton Pattern**: `TheRankInfoStore` provides global access to rank data
- **Data Transfer Object**: `RankInfo` encapsulates rank attributes for configuration
- **Friend Pattern**: `friend_parseRankDefinition` allows INI parser to populate rank data

*Not inferable*: Exact memory pool implementation details.
