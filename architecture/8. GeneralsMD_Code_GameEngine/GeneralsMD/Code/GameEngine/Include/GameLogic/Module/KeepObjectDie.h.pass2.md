# GeneralsMD/Code/GameEngine/Include/GameLogic/Module/KeepObjectDie.h - Enhanced Analysis

## Architectural Role
This file defines a specialized die module for objects that need to leave rubble upon destruction but don't have other die modules. It fits into the game's component-based architecture, where object behavior is modularized into reusable "modules" that can be attached to game entities.

## Cross-References
### Incoming
- Likely called by the `Thing` class's destruction logic or the game's damage system when an object is destroyed.
- May be referenced in INI files that define object templates, specifying which die module to use.

### Outgoing
- Inherits from `DieModule`, so it calls into the base class's functionality.
- Likely interacts with the rubble/particle system to spawn rubble when `onDie` is called.

## Design Patterns
- **Component Pattern**: The `KeepObjectDie` is a modular component attached to `Thing` objects, following the engine's design where behavior is split into reusable modules.
- **Memory Pooling**: Uses `MEMORY_POOL_GLUE_WITH_USERLOOKUP_CREATE` for efficient object allocation, common in the SAGE engine for performance-critical systems.
- **Template Method**: The `onDie` method is overridden to provide custom destruction behavior while likely reusing base class logic.
