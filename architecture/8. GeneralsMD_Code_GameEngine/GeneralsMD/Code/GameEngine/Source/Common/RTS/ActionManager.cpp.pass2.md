# GeneralsMD/Code/GameEngine/Source/Common/RTS/ActionManager.cpp - Enhanced Analysis

## Architectural Role
This file implements the central action validation system for the game, bridging UI input validation, network command processing, and game logic. It serves as a critical abstraction layer that decouples action legality checks from both the UI and networking systems, ensuring consistent behavior across all input sources.

## Cross-References
### Incoming
- **UI System**: Calls action validation methods to enable/disable commands
- **Networking**: Uses the same validation for command processing
- **AI System**: Likely queries action validity for pathfinding/behavior decisions
- **Scripting**: Uses `CMD_FROM_SCRIPT` flag for scripted actions

### Outgoing
- **Game Logic**: Queries `Object`, `Weapon`, and module interfaces
- **Partition Manager**: For shroud/fog-of-war checks
- **Player/Team Systems**: For relationship and ownership validation

## Design Patterns
- **Singleton Pattern**: `TheActionManager` provides global access to action validation
- **Strategy Pattern**: Different action types (repair, attack, special powers) use distinct validation logic
- **Guard Clauses**: Early returns for invalid states (null checks, dead objects) improve readability

**Not inferable**: Exact pattern usage for special power validation (likely Template Method or State)
