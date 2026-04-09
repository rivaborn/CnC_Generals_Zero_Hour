# GeneralsMD/Code/GameEngine/Source/GameLogic/Object/Update/AIUpdate/AssaultTransportAIUpdate.cpp - Enhanced Analysis

## Architectural Role
This file implements the AI state machine for assault transport vehicles, bridging the gap between high-level AI commands and low-level unit behavior. It manages troop deployment, attack coordination, and healing logic, acting as a middleware layer between the AI system and unit modules.

## Cross-References
### Incoming
- **AI System**: Calls `aiDoCommand` to issue transport-specific orders
- **Weapon System**: Triggers `beginAssault` when in attack range
- **Containment System**: Uses `ContainModuleInterface` for troop management
- **Body System**: Checks unit health via `BodyModuleInterface`

### Outgoing
- **AI System**: Delegates to `AIUpdateInterface` for base behavior
- **Game Logic**: Queries `TheGameLogic` for object lookups
- **Partition Manager**: Likely used for spatial queries (implied by `ThePartitionManager` reference)
- **Unit AI**: Issues commands to transported units (`aiAttackObject`, `aiAttackMoveToPosition`)

## Design Patterns
- **State Machine**: Uses `AssaultStateTypes` enum to manage transport behavior states (IDLE, DEPLOYING, etc.)
- **Observer**: Reacts to external commands (player/AI) via `aiDoCommand`
- **Strategy**: Encapsulates transport-specific logic while inheriting from `AIUpdateInterface` (template method pattern)

*Not inferable*: Exact use of Command pattern for troop orders (implied but not explicit in shown code).
