# GeneralsMD/Code/GameEngine/Source/GameLogic/Object/Update/HordeUpdate.cpp - Enhanced Analysis

## Architectural Role
This file implements the horde behavior system, a key part of the game's group dynamics. It bridges the spatial partitioning system (PartitionManager) with visual effects (Drawable) and AI logic (AIUpdate), enabling collective behavior for units.

## Cross-References
### Incoming
- **AIUpdate.cpp**: Calls `evaluateMoraleBonus()` when horde status changes
- **Drawable.cpp**: Uses `setTerrainDecal()` and related methods for visual feedback
- **BehaviorModule implementations**: Query `getHordeUpdateInterface()` to access horde functionality

### Outgoing
- **PartitionManager**: Uses spatial queries via `PartitionFilterHordeMember`
- **AIUpdate**: Delegates morale calculations
- **Drawable**: Manages terrain decal effects for horde members

## Design Patterns
- **Strategy Pattern**: `PartitionFilterHordeMember` encapsulates horde membership rules
- **Observer Pattern**: Horde state changes trigger visual/audio updates (e.g., decal fading)
- **Configuration-Driven**: Uses `HordeUpdateModuleData` for INI-driven behavior customization

*Not inferable*: Exact serialization versioning strategy or thread-safety guarantees.
