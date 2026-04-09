# GeneralsMD/Code/GameEngine/Source/Common/RTS/Science.cpp - Enhanced Analysis

## Architectural Role
This file implements the core science/technology research system, acting as a central registry for all researchable technologies. It bridges the INI configuration system with runtime game logic, enabling technology trees, prerequisites, and player research state management.

## Cross-References
### Incoming
- `INI::parseScienceDefinition` calls `ScienceStore::friend_parseScienceDefinition`
- Player systems query `getPurchasableSciences` and `playerHasPrereqsForScience`
- UI systems likely use `getNameAndDescription` for display

### Outgoing
- Calls into `INI` subsystem for configuration parsing
- Relies on `Player` class for science ownership checks
- Uses `NameKeyGenerator` for string-to-enum conversions

## Design Patterns
- **Singleton Pattern**: `TheScienceStore` provides global access to science data
- **Override Pattern**: `ScienceInfo` supports hierarchical overrides via `deleteOverrides`/`deleteInstance`
- **Registry Pattern**: Maintains a collection of `ScienceInfo` objects for lookup

Rules followed. Analysis limited to observable code behavior.
