# GeneralsMD/Code/GameEngine/Include/GameLogic/Module/StructureBody.h - Enhanced Analysis

## Architectural Role
This file defines the base class for structure-specific game logic in the SAGE engine, extending the `ActiveBody` system. It serves as a foundational component for all buildable structures, managing construction ownership and providing module data parsing infrastructure.

## Cross-References
### Incoming
- `HiveStructureBody` (specialized structure type) inherits and uses `StructureBody` methods
- Game logic systems that need to track structure ownership (e.g., resource allocation, construction queues)

### Outgoing
- Directly extends `ActiveBody` and its module data system
- Uses `MultiIniFieldParse` for configuration parsing
- Interfaces with `Object` system for construction tracking

## Design Patterns
- **Module Pattern**: Uses the engine's module system (evident in `MAKE_STANDARD_MODULE_MACRO` and `ModuleData` inheritance)
- **Memory Pool Pattern**: Custom memory allocation via `MEMORY_POOL_GLUE` macros for performance optimization
- **Composition over Inheritance**: While inheriting from `ActiveBody`, it maintains clean separation of concerns through module data

*Not inferable*: Exact usage of `ObjectID` tracking pattern or how construction ownership affects game logic.
