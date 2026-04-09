# GeneralsMD/Code/GameEngine/Include/GameLogic/Module/UndeadBody.h - Enhanced Analysis

## Architectural Role
This file defines the `UndeadBody` module, which extends the `ActiveBody` system to implement a "resurrection" mechanic where objects survive their first death with reduced health. It integrates with the game's damage and health systems, demonstrating how modular behavior can be added to game entities via composition.

## Cross-References
### Incoming
- Likely called by damage processing systems (e.g., `DamageInfo` handlers) when objects take lethal damage.
- May be referenced in entity definition files (INI) where undead behavior is configured.

### Outgoing
- Calls into `ActiveBody` base class methods for core functionality.
- Uses `MultiIniFieldParse` for configuration parsing, tying into the engine's data-driven design.

## Design Patterns
- **Module Pattern**: Extends `ActiveBody` via composition, allowing behavior to be added/removed dynamically.
- **State Pattern**: Implicitly manages two states (first life/second life) via `m_isSecondLife` flag.
- **Template Method**: `buildFieldParse` suggests a parsing framework where subclasses define their own field mappings.
