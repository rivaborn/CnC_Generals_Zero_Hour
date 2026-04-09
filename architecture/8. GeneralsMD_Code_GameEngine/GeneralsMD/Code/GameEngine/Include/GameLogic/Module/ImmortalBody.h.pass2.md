# GeneralsMD/Code/GameEngine/Include/GameLogic/Module/ImmortalBody.h - Enhanced Analysis

## Architectural Role
This file defines a specialized body module that enforces a minimum health threshold (1), likely used for objects that should not be destroyed under normal circumstances (e.g., certain structures or AI-controlled units). It extends the `ActiveBody` module, integrating into the game's component-based entity system.

## Cross-References
### Incoming
- **GameLogic/Module/ActiveBody.h**: Base class inheritance.
- **Thing.h**: Parent object reference (forward-declared).
- **ModuleData.h**: Configuration data for module initialization.

### Outgoing
- **ActiveBody**: Calls parent constructor and overrides `internalChangeHealth`.
- **Memory management macros**: Uses engine-specific macros for memory pooling.

## Design Patterns
- **Template Method**: Overrides `internalChangeHealth` to modify default behavior while reusing `ActiveBody`'s structure.
- **Component-Based Design**: Fits into the engine's modular entity system where behavior is split into reusable modules.
- **Memory Pooling**: Uses engine-specific macros for optimized object allocation (common in SAGE for performance).

*Not inferable*: Exact health clamping logic or usage context (e.g., which objects use this module).
