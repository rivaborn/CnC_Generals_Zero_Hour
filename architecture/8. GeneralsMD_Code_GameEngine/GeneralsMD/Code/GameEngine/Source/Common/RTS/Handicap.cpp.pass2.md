# GeneralsMD/Code/GameEngine/Source/Common/RTS/Handicap.cpp - Enhanced Analysis

## Architectural Role
Handicap.cpp implements the game's difficulty scaling system, allowing dynamic adjustment of build costs, build times, and other attributes based on player settings or AI behavior. It bridges the configuration system (Dict) with runtime entity behavior.

## Cross-References
### Incoming
- **Game Logic**: Likely called by player/building creation systems to apply handicap modifiers
- **AI**: Used by AI logic to adjust behavior based on handicap settings
- **UI**: Possibly referenced during difficulty selection screens

### Outgoing
- **Configuration**: Reads from `Dict` objects for handicap values
- **Entity System**: Uses `ThingTemplate` to determine entity types
- **Name Key System**: Relies on `TheNameKeyGenerator` for dictionary key lookup

## Design Patterns
- **Strategy Pattern**: `getBestThingType()` acts as a strategy for determining handicap applicability
- **Table-Driven Design**: Uses a 2D array (`m_handicaps`) for efficient lookup of handicap values
- **Dependency Injection**: Handicap values are injected via `readFromDict()` rather than hardcoded

*Not inferable*: No clear use of Factory, Observer, or other patterns in this file.
