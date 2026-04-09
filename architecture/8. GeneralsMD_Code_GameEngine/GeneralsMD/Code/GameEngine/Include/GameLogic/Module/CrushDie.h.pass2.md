# GeneralsMD/Code/GameEngine/Include/GameLogic/Module/CrushDie.h - Enhanced Analysis

## Architectural Role
This file defines a specialized death module for handling crush-related destruction logic, integrating with the game's damage system and audio subsystem. It extends the base `DieModule` to provide crush-specific behavior and sound playback.

## Cross-References
### Incoming
- Damage system (calls `onDie` when crush damage occurs)
- INI parsing system (uses `buildFieldParse` for configuration)
- Thing/Object system (applied to game entities)

### Outgoing
- Audio subsystem (`AudioEventRTS` for sound playback)
- Base `DieModule` class (inheritance)
- INI parsing utilities (for configuration loading)

## Design Patterns
- **Strategy Pattern**: Extends `DieModule` to provide crush-specific death behavior
- **Configuration via Data**: Uses `CrushDieModuleData` for external INI-driven configuration
- **Memory Pool Pattern**: Uses SAGE engine's memory management macros for object allocation

Rules followed. Analysis limited to 400 tokens.
