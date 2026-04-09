# GeneralsMD/Code/GameEngine/Source/Common/INI/INICommandButton.cpp - Enhanced Analysis

## Architectural Role
This file bridges the INI parsing subsystem with the UI control bar, handling the deserialization of command button definitions. It enforces consistency between button options and special power templates, critical for the game's context-sensitive UI.

## Cross-References
### Incoming
- `INI` subsystem calls `parseCommandButtonDefinition` during INI loading phases
- Likely invoked by `Game::LoadMission()` or similar initialization paths

### Outgoing
- Directly manipulates `TheControlBar` (global UI control bar)
- Calls into `SpecialPower` subsystem for template validation
- Uses `INI` methods for field parsing and error handling

## Design Patterns
- **Factory Method**: `newCommandButton`/`newCommandButtonOverride` create button instances
- **Singleton**: Relies on `TheControlBar` global instance
- **Guard Clause**: Early validation for duplicate buttons and special power consistency

*Not inferable*: No clear use of Observer or Strategy patterns in this snippet.
