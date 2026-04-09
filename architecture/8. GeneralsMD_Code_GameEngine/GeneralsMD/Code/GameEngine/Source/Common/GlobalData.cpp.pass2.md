# GeneralsMD/Code/GameEngine/Source/Common/GlobalData.cpp - Enhanced Analysis

## Architectural Role
This file implements the central configuration management system for the SAGE engine, acting as a global registry for runtime settings that affect rendering, gameplay, and system behavior. It provides a stack-based override mechanism that allows temporary modifications to game parameters without permanently altering the base configuration.

## Cross-References
### Incoming
- Game initialization systems (likely in `Main.cpp` or similar)
- Rendering subsystems (terrain, water, lighting)
- Audio systems (for time-of-day effects)
- UI systems (for resolution and display settings)
- Networking components (firewall settings)

### Outgoing
- `INI` parsing system for configuration loading
- `UserPreferences` for player-specific settings
- `OptionPreferences` for UI/control preferences
- `FirewallHelper` for network configuration
- `TerrainVisual` and related rendering components

## Design Patterns
- **Singleton with Override Stack**: Uses a global singleton (`TheWritableGlobalData`) with a linked-list of overrides, allowing temporary configuration changes that can be reset.
- **Data-Driven Design**: Heavy use of INI parsing tables (`FieldParse`) to map configuration values to class members, enabling external configuration without code changes.
- **Immutable Base with Mutable Overrides**: The original configuration is preserved, with all modifications creating new instances in the override stack.

Not inferable: No clear use of other patterns like Factory, Observer, or Strategy in this file.
