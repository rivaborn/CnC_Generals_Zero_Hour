# GeneralsMD/Code/GameEngine/Include/GameLogic/Module/HighlanderBody.h - Enhanced Analysis

## Architectural Role
This file defines a specialized body module for objects that exhibit "highlander" behaviorâtaking damage but resisting death from normal sources. It integrates into the game's modular body system, extending `ActiveBody` to override damage handling logic.

## Cross-References
### Incoming
- Likely called by damage-processing systems (e.g., `DamageInfo` handlers) and object initialization code.

### Outgoing
- Inherits from `ActiveBody`, so it calls into its parent's methods (e.g., constructor, virtual functions).
- Uses `MEMORY_POOL_GLUE` macros, indicating interaction with the engine's memory management system.

## Design Patterns
- **Template Method**: Overrides `attemptDamage` to customize damage logic while reusing `ActiveBody`'s structure.
- **Object Pooling**: Uses `MEMORY_POOL_GLUE` for performance-critical allocation.
- **Module Pattern**: Follows the engine's modular architecture (e.g., `MAKE_STANDARD_MODULE_MACRO`).
