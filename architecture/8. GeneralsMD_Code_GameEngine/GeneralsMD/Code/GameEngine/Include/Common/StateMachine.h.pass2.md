# GeneralsMD/Code/GameEngine/Include/Common/StateMachine.h - Enhanced Analysis

## Architectural Role
This file defines the core finite state machine framework used throughout the engine for game object behavior management. It provides the foundation for AI state machines, unit behaviors, and other state-driven systems.

## Cross-References
### Incoming
- AIStateMachine.h (uses CONVERT_SLEEP_TO_CONTINUE and MIN_SLEEP)
- GameLogic/AIStateMachine.h (references state machine utilities)

### Outgoing
- MemoryPoolObject, Snapshot, Xfer (inheritance/interface)
- Object (forward reference)
- std::map, std::vector (STL containers)

## Design Patterns
- **State Pattern**: Core implementation of state machines with State/StateMachine classes
- **Template Method**: State lifecycle methods (onEnter, update, onExit) define hooks for subclasses
- **Flyweight**: MemoryPoolObject usage suggests object pooling for state instances

Rules followed. Output under 400 tokens.
