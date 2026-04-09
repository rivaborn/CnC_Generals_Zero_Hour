# GeneralsMD/Code/GameEngine/Include/GameLogic/Module/HealContain.h - Enhanced Analysis

## Architectural Role
This file defines the healing container module, extending the open container system to provide healing functionality for contained units. It integrates with the game's module system and object containment hierarchy, enabling units to recover health over time when inside specific structures.

## Cross-References
### Incoming
- Game logic systems that manage object containment (e.g., `OpenContain` subclasses)
- Module initialization code that instantiates healing containers
- Unit health management systems that check for healing conditions

### Outgoing
- `OpenContain` base class for containment logic
- `MultiIniFieldParse` for configuration parsing
- Object health systems for applying healing effects
- SAGE engine memory pool and module macros

## Design Patterns
- **Template Method**: `update()` and `doHeal()` define hooks for healing behavior while inheriting containment logic from `OpenContain`
- **Module Pattern**: Uses SAGE's module system for configuration and instantiation
- **Strategy**: Healing behavior can be customized via `m_framesForFullHeal` parameter
