# GeneralsMD/Code/GameEngine/Include/GameLogic/Module/FloatUpdate.h - Enhanced Analysis

## Architectural Role
This file defines a module for handling floating-on-water behavior, extending the `UpdateModule` base class. It integrates into the game's component-based architecture, allowing objects to dynamically adjust their floating state based on game logic.

## Cross-References
### Incoming
- Likely called by `Thing` objects during their update cycle (implied by `Thing *thing` parameter in constructor)
- Referenced in module initialization code (via `MAKE_STANDARD_MODULE_MACRO`)

### Outgoing
- Inherits from `UpdateModule` and `UpdateModuleData`
- Uses `MultiIniFieldParse` for configuration parsing
- Depends on memory pool macros for object management

## Design Patterns
- **Component Pattern**: Implements floating behavior as a modular component that can be attached to game objects
- **Strategy Pattern**: Encapsulates floating logic in a separate module that can be enabled/disabled dynamically
- **Template Method**: Uses virtual `update()` to define the floating update cycle while allowing subclass customization
