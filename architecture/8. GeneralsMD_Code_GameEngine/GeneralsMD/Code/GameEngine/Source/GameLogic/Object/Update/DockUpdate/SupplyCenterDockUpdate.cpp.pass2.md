# GeneralsMD/Code/GameEngine/Source/GameLogic/Object/Update/DockUpdate/SupplyCenterDockUpdate.cpp - Enhanced Analysis

## Architectural Role
This file implements the economic core of supply centers, bridging the resource collection system (supply trucks) with the player's economy. It handles the conversion of supply boxes to money, temporary stealth mechanics, and UI feedback, acting as a critical link between the resource management and player progression systems.

## Cross-References
### Incoming
- **SupplyTruckAIUpdate**: Calls into this module's `action()` when supply trucks dock
- **Player/PlayerMoney**: Called when depositing earned money
- **StealthUpdate**: Interacts when granting temporary stealth
- **InGameUI**: Called for floating text display

### Outgoing
- **DockUpdate**: Base class for update logic
- **SupplyTruckAIInterface**: Queries for supply box management
- **ScoreKeeper**: Updates player statistics
- **TerrainLogic**: Used for positioning floating text

## Design Patterns
- **Strategy Pattern**: The `action()` method encapsulates the specific behavior for supply center docking, allowing different dock behaviors to be swapped via module data
- **Observer Pattern**: Floating text display is triggered based on docking events, with UI updates decoupled from economic logic
- **Template Method**: Base class `DockUpdate` provides skeletal implementation for update/crc/xfer/loadPostProcess, with this class extending specific behaviors

*Not inferable*: No clear use of Visitor, Factory, or Decorator patterns in this file.
