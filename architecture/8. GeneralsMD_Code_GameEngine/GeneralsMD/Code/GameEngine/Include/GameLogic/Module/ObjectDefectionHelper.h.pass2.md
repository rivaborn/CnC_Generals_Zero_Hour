# GeneralsMD/Code/GameEngine/Include/GameLogic/Module/ObjectDefectionHelper.h - Enhanced Analysis

## Architectural Role
This file defines the defection logic helper for game objects, managing timers and visual effects during unit defection. It extends the `ObjectHelper` base class, integrating into the SAGE engine's modular component system for game entity behavior.

## Cross-References
### Incoming
- Likely called by unit/building logic modules when defection events occur (e.g., `AmericaInfPilot` defecting)
- Referenced in module initialization code for entity behavior setup

### Outgoing
- Uses `ObjectHelper` base class methods
- Interacts with SAGE's memory pool system via `MEMORY_POOL_GLUE` macros
- Depends on `ModuleData` infrastructure for module configuration

## Design Patterns
- **Module Pattern**: Inherits from `ObjectHelper` to provide modular behavior for game entities
- **Timer Pattern**: Uses frame-based timers (`m_defectionDetectionStart/End`) for state management
- **Memory Pool Pattern**: Uses SAGE's memory allocation system for performance optimization
