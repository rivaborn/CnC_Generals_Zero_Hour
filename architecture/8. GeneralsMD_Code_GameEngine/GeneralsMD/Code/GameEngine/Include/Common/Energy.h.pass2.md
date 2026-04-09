# GeneralsMD/Code/GameEngine/Include/Common/Energy.h - Enhanced Analysis

## Architectural Role
This file defines the `Energy` class, which is a core subsystem for managing player resource economics in the game. It bridges the gap between player state and object interactions, ensuring energy production/consumption is tracked globally while allowing individual objects to influence the system.

## Cross-References
### Incoming
- **Player**: Likely calls `init()` during player creation and `adjustPower()` for global energy adjustments
- **Object**: Calls `objectEnteringInfluence()`/`objectLeavingInfluence()` when objects enter/leave power grids
- **Game Logic**: Uses `getEnergySupplyRatio()` for power management decisions

### Outgoing
- **Snapshot**: Inherits serialization methods for save/load
- **Player**: Holds reference to owner for state queries
- **Object**: Interfaces with objects for power bonuses/sabotage

## Design Patterns
- **Observer Pattern**: Objects notify `Energy` of their influence changes via `objectEnteringInfluence`/`objectLeavingInfluence`
- **Resource Pool**: Encapsulates energy as a shared resource with production/consumption tracking
- **State Management**: Uses `m_powerSabotagedTillFrame` for temporal power state handling

*Not inferable: Exact serialization mechanism or how power bonuses are calculated.*
