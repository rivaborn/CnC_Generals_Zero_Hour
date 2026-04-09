# GeneralsMD/Code/GameEngine/Include/Common/IgnorePreferences.h - Enhanced Analysis

## Architectural Role
This header defines the `IgnorePreferences` class, which extends the `UserPreferences` base class to manage multiplayer ignore lists. It integrates with the game's preference system and networking infrastructure to handle player ignore functionality.

## Cross-References
### Incoming
- Likely called by multiplayer UI components (e.g., player list screens)
- Used by networking code handling chat/voice communication filtering

### Outgoing
- Inherits from `UserPreferences` (preference management system)
- Uses STL `std::map` for internal storage

## Design Patterns
- **Inheritance**: Extends `UserPreferences` to specialize preference handling for ignore lists
- **Encapsulation**: Hides internal `IgnorePrefMap` implementation behind public methods
- **Not inferable**: No clear factory, observer, or other patterns evident from header alone
