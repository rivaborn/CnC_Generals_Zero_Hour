# GeneralsMD/Code/GameEngine/Include/GameLogic/Module/InactiveBody.h - Enhanced Analysis

## Architectural Role
This file defines a specialized `BodyModule` for objects that should ignore all damage and healing interactions, fitting into the game's component-based architecture where behavior is modularized. It serves as a base for environmental or decorative objects that must remain immutable regardless of gameplay events.

## Cross-References
### Incoming
- Likely called by `Thing` objects that require indestructible behavior (e.g., terrain features, static props).
- Referenced in module factory systems that instantiate body components.

### Outgoing
- Inherits from `BodyModule`, overriding its damage/healing interface.
- Uses memory pool macros (`MEMORY_POOL_GLUE_WITH_USERLOOKUP_CREATE`) and module system macros (`MAKE_STANDARD_MODULE_MACRO`).

## Design Patterns
- **Null Object Pattern**: Implements no-op behavior for damage/healing to represent objects that should ignore interactions.
- **Template Method Pattern**: Overrides virtual methods from `BodyModule` to customize behavior while retaining the parent class structure.
- **Memory Pool Pattern**: Uses custom memory allocation macros for performance optimization in object creation/destruction.
