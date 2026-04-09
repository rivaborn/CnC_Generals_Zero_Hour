# GeneralsMD/Code/GameEngine/Include/GameClient/Eva.h - Enhanced Analysis

## Architectural Role
This file defines the EVA (Electronic Versatile Assistant) subsystem, which handles in-game voice announcements triggered by game events. It acts as an intermediary between game events and the audio system, managing message priorities, timing, and side-specific voice lines.

## Cross-References
### Incoming
- Game event handlers (e.g., building loss, superweapon detection)
- Player state queries (e.g., funds, unit counts)
- INI parsing system for configuration

### Outgoing
- AudioEventRTS for voice playback
- Player subsystem for state checks
- Memory allocation system via MemoryPoolObject

## Design Patterns
- **Strategy Pattern**: Uses `ShouldPlayFunc` callbacks to determine message play conditions, allowing dynamic behavior without modifying core logic.
- **Observer Pattern**: Monitors game state changes to trigger appropriate EVA messages.
- **Singleton Pattern**: Global `TheEva` instance provides centralized access to the EVA subsystem.

*Not inferable*: Exact implementation of `AudioEventRTS` integration or how `EvaCheck` objects are populated.
