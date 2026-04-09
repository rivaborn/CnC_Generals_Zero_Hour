# GeneralsMD/Code/GameEngine/Include/GameLogic/Module/AssaultTransportAIUpdate.h - Enhanced Analysis

## Architectural Role
This file implements the AI behavior for assault transport units, bridging the gap between high-level AI commands and low-level unit control. It extends the generic AIUpdate framework with transport-specific logic for troop deployment, healing management, and assault coordination.

## Cross-References
### Incoming
- **AI System**: Calls `aiDoCommand` and `update` during AI processing cycles
- **Unit Control**: Likely invoked by transport unit classes when entering assault mode
- **Command System**: `beginAssault` called when player issues assault commands

### Outgoing
- **State Machine**: Uses `Common/StateMachine.h` for state transitions
- **Unit Management**: Interacts with `Thing` objects (troops/transports) via `ObjectID`
- **Configuration**: Parses INI data through `MultiIniFieldParse`

## Design Patterns
- **State Pattern**: Encapsulates assault transport behavior in discrete states (IDLE/ASSAULTING)
- **Strategy Pattern**: `AssaultTransportAIInterface` allows runtime behavior variation
- **Module Pattern**: Follows SAGE's modular AI architecture with `AIUpdateModuleData` configuration

*Not inferable*: Exact command processing flow or healing threshold calculations.
