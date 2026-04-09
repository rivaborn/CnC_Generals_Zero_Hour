# GeneralsMD/Code/GameEngine/Include/GameLogic/Module/SabotageInternetCenterCrateCollide.h - Enhanced Analysis

## Architectural Role
This file implements a specialized crate collision behavior for sabotaging internet centers, extending the base `CrateCollide` module. It integrates with the game's crate system, which handles power-up drops, and specifically targets buildings with sabotage effects.

## Cross-References
### Incoming
- **GameLogic/Module/CrateCollide.h**: Base class inheritance and module data structure
- **Common/Module.h**: Core module infrastructure
- **MultiIniFieldParse**: For configuration parsing (indirect via `buildFieldParse`)

### Outgoing
- **Thing**: Forward reference to game object system (collision targets)
- **Object**: Base game entity class (for `isValidToExecute` and `executeCrateBehavior`)
- **INI namespace**: For field parsing utilities

## Design Patterns
- **Template Method**: `executeCrateBehavior` and `isValidToExecute` are virtual hooks for derived behavior
- **Module Pattern**: Uses SAGE's module system (`MAKE_STANDARD_MODULE_MACRO`) for runtime registration
- **Data-Driven Design**: Module data (`SabotageInternetCenterCrateCollideModuleData`) parsed from INI files for configurability

**Not inferable**: Specific sabotage mechanics (e.g., how internet centers are disabled).
