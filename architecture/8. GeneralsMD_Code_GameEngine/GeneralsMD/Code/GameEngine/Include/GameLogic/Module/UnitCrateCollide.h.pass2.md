# GeneralsMD/Code/GameEngine/Include/GameLogic/Module/UnitCrateCollide.h - Enhanced Analysis

## Architectural Role
This file defines a specialized crate module that extends the base `CrateCollide` behavior to spawn units when collected. It integrates with the game's INI-based modding system and object pooling infrastructure, bridging the gap between data-driven configuration and runtime behavior.

## Cross-References
### Incoming
- Likely called by crate interaction systems (e.g., `Crate::onCollide`) and modding infrastructure (INI parsing)
- May be referenced by unit spawning logic in `GameLogic/Module/UnitManager`

### Outgoing
- Calls `CrateCollideModuleData::buildFieldParse` for base field parsing
- Uses `INI` namespace utilities for configuration parsing
- Relies on `Thing` and `Object` classes for collision handling

## Design Patterns
- **Template Method**: `executeCrateBehavior` is a virtual method defining a hook for derived behavior
- **Object Pooling**: Uses `MEMORY_POOL_GLUE` macros for optimized memory management
- **Data-Driven Design**: Configuration stored in `UnitCrateCollideModuleData` parsed from INI files
