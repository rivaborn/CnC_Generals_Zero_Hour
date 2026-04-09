# GeneralsMD/Code/GameEngine/Source/GameLogic/Object/Helper/StatusDamageHelper.cpp - Enhanced Analysis

## Architectural Role
This file implements a helper class for managing timed status effects on game objects, integrating with the SAGE engine's object-component system. It handles the lifecycle of status conditions (e.g., burns, stuns) by leveraging the engine's wake/sleep update mechanism for efficiency.

## Cross-References
### Incoming
- **GameLogic/Object.cpp**: Likely instantiates and attaches this helper to objects via `ObjectHelper` registration
- **GameLogic/Module/StatusDamageHelper.h**: Header inclusion implies module system integration
- **Networking subsystem**: Calls `xfer()` during serialization for multiplayer sync

### Outgoing
- **GameLogic/GameLogic.h**: Uses `TheGameLogic` for frame timing
- **GameLogic/Object.h**: Interacts with `Thing` objects via `getObject()`
- **GameLogic/Module/StatusDamageHelper.h**: Base class methods (`ObjectHelper::xfer()`)

## Design Patterns
- **Observer Pattern**: The helper "watches" the object's status via wake/sleep callbacks
- **State Machine**: Manages status transitions (apply/clear) with explicit timer logic
- **Dependency Injection**: Receives `Thing*` and `ModuleData*` in constructor for flexibility

*Not inferable*: No clear use of Strategy or Command patterns despite timer-based behavior.
