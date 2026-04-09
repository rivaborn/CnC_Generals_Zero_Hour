# GeneralsMD/Code/GameEngine/Source/GameLogic/Object/Update/AutoFindHealingUpdate.cpp - Enhanced Analysis

## Architectural Role
This file implements the AI-driven healing behavior for units, acting as a specialized update module in the SAGE engine's component-based architecture. It bridges the AI system with the spatial partitioning system to locate heal pads efficiently.

## Cross-References
### Incoming
- **AIUpdate**: Calls `aiGetHealed()` to trigger healing behavior
- **PartitionManager**: Used for spatial queries in `scanClosestTarget()`
- **BodyModuleInterface**: Checks unit health via `getHealth()`/`getMaxHealth()`

### Outgoing
- **UpdateModule**: Base class for update loop and serialization
- **Object**: Accesses controlling player and AI interface
- **ThingTemplate**: Inherited for module data configuration

## Design Patterns
- **Strategy Pattern**: Encapsulates healing logic as a modular update component
- **Observer Pattern**: Reacts to health state changes via periodic updates
- **Template Method**: Uses `buildFieldParse()` for INI-based configuration

*Not inferable*: Exact spatial query optimization (e.g., quadtree traversal)
