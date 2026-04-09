# GeneralsMD/Code/GameEngine/Include/GameLogic/Module/SupplyTruckAIUpdate.h - Enhanced Analysis

## Architectural Role
This file implements the supply truck's AI behavior as a state machine, integrating with the broader AI system (AIUpdate) and object command handling. It bridges between high-level AI directives and low-level object behavior, particularly for resource management and docking mechanics.

## Cross-References
### Incoming
- **AI System**: Calls `update()` to drive state transitions
- **Command System**: Invokes `privateDock()` and `privateIdle()` for player/ai-issued commands
- **Object System**: Uses `Thing` ownership for state machine attachment

### Outgoing
- **State Machine Framework**: Extends `StateMachine` and `State` for behavior definition
- **Audio System**: Triggers `AudioEventRTS` for supply depletion feedback
- **Serialization**: Uses `Xfer` for save/load compatibility

## Design Patterns
- **State Pattern**: Encapsulates truck behavior in discrete states (idle, docking, etc.)
- **Strategy Pattern**: `SupplyTruckAIInterface` allows polymorphic supply management
- **Module Pattern**: `SupplyTruckAIUpdateModuleData` configures behavior via INI parsing

*Not inferable*: Exact command routing to `privateDock()`/`privateIdle()` (e.g., via event system or direct calls).
