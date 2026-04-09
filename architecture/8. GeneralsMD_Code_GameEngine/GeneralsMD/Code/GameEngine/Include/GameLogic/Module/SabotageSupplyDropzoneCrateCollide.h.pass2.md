# GeneralsMD/Code/GameEngine/Include/GameLogic/Module/SabotageSupplyDropzoneCrateCollide.h - Enhanced Analysis

## Architectural Role
This file implements a specialized crate collision behavior for sabotage mechanics, extending the base `CrateCollide` system. It bridges the supply dropzone crate mechanics with power plant sabotage logic, handling cash theft and collision validation.

## Cross-References
### Incoming
- **GameLogic/Module/CrateCollide.h**: Base class inheritance
- **Common/Module.h**: Framework for module system
- **INI parsing utilities**: For configuration loading
- **Thing class**: Collision target reference

### Outgoing
- **CrateCollideModuleData**: Parent class for module data
- **Object system**: For collision target validation
- **Power plant/building systems**: For sabotage effects (implied by `executeCrateBehavior`)

## Design Patterns
- **Template Method**: `executeCrateBehavior` and `isValidToExecute` as virtual methods for behavior extension
- **Module Pattern**: Uses SAGE's module system for composable behaviors
- **Data-Driven Design**: Configuration via `buildFieldParse` for INI-based customization

*Not inferable*: Exact sabotage mechanics or power plant interaction details.
