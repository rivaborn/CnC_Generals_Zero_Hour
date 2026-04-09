# GeneralsMD/Code/GameEngine/Include/GameLogic/AISkirmishPlayer.h - Enhanced Analysis

## Architectural Role
This header defines the core AI logic for skirmish mode, extending the base AIPlayer class. It handles enemy targeting, base construction, and team management, serving as the primary interface for computer-controlled opponents in non-campaign gameplay.

## Cross-References
### Incoming
- **GameLogic/AIPlayer.h**: Base class interface
- **GameLogic/BuildListInfo.h**: For build list adjustments
- **GameLogic/SpecialPowerTemplate.h**: For superweapon targeting
- **GameEngine/Include/GameLogic/Player.h**: For enemy player tracking

### Outgoing
- **GameLogic/AIPlayer.cpp**: Implements inherited virtual methods
- **GameLogic/TeamPrototype.h**: For team building logic
- **GameLogic/WorkOrder.h**: For production order management
- **GameLogic/Waypoint.h**: For pathfinding/bridge checks

## Design Patterns
- **Template Method**: Overrides virtual methods from AIPlayer to customize skirmish behavior
- **Strategy**: Encapsulates different AI strategies (e.g., base defense, team building) as separate methods
- **Observer**: Reacts to game events (e.g., `onUnitProduced`) via callback methods
