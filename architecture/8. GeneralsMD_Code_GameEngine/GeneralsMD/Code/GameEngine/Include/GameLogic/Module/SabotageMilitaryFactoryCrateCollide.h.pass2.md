# GeneralsMD/Code/GameEngine/Include/GameLogic/Module/SabotageMilitaryFactoryCrateCollide.h - Enhanced Analysis

## Architectural Role
This file implements a specialized crate collision behavior that temporarily disables military factories, fitting into the game's modular crate system. It extends the base `CrateCollide` class to handle sabotage mechanics, integrating with the factory production system and collision detection framework.

## Cross-References
### Incoming
- **GameLogic/Module/CrateCollide.h**: Base class inheritance and module data structure
- **Thing.h**: Forward reference for collision target validation
- **MultiIniFieldParse.h**: Used in `buildFieldParse` for INI configuration

### Outgoing
- **CrateCollideModuleData**: Inherited class for module data
- **Object**: Base class for collision targets in `executeCrateBehavior`
- **INI parsing system**: For configuration via `buildFieldParse`

## Design Patterns
- **Template Method**: `executeCrateBehavior` and `isValidToExecute` are virtual hooks for specialized behavior
- **Module Pattern**: Uses `ModuleData` for configuration, enabling runtime customization
- **Factory Method**: `buildFieldParse` registers INI parsing for module data initialization

*Not inferable*: Exact sabotage mechanics or factory interaction details.
