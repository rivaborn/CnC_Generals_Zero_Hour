# GeneralsMD/Code/GameEngine/Include/GameLogic/AIDock.h - Enhanced Analysis

## Architectural Role
This file defines the AI docking subsystem, a critical component of the game's unit management system. It implements a state machine for handling unit docking behavior, including queue management, clearance waiting, and processing actions like repairs.

## Cross-References
### Incoming
- AI state machine controller (likely in `GameLogic/AIStateMachine.cpp`)
- Unit movement system (calls `AIInternalMoveToState` implementations)
- Dock/building interaction logic (triggers docking sequences)

### Outgoing
- `AIStateMachine.h` (base class inheritance)
- `Common/GameMemory.h` (memory pool management)
- `Xfer` class (save/load serialization)
- `Object` class (for drone/unit references)

## Design Patterns
- **State Pattern**: Uses a state machine to encapsulate different docking behaviors (approach, wait, process, etc.).
- **Memory Pool Pattern**: Uses `MEMORY_POOL_GLUE_WITH_USERLOOKUP_CREATE` for object allocation optimization.
- **Strategy Pattern**: Docking actions are delegated to specific state classes, allowing runtime behavior modification.
