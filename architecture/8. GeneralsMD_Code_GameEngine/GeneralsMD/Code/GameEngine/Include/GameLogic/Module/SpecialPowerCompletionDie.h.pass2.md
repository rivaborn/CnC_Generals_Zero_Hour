# GeneralsMD/Code/GameEngine/Include/GameLogic/Module/SpecialPowerCompletionDie.h - Enhanced Analysis

## Architectural Role
This file defines a die module that bridges unit death events with the script engine, enabling special power completion tracking. It integrates with the game's event-driven architecture by extending the `DieModule` base class and interacting with the scripting system.

## Cross-References
### Incoming
- Scripting system (likely `TheScriptEngine`) calls `notifyScriptEngine` when special powers complete
- INI parsing system calls `buildFieldParse` during module initialization
- Unit/thing destruction logic calls `onDie` when units are killed

### Outgoing
- Calls into `DieModuleData` base class for field parsing
- Likely calls `SpecialPowerTemplate` methods for power-specific logic
- Interfaces with object management system for creator ID resolution

## Design Patterns
- **Template Method**: `buildFieldParse` extends base class parsing with special power-specific fields
- **Observer**: Notifies script engine of state changes (unit death) without tight coupling
- **Dependency Injection**: Creator ID is injected via `setCreator`, decoupling from object lookup timing

Rules followed. Analysis limited to observable cross-cutting concerns.
