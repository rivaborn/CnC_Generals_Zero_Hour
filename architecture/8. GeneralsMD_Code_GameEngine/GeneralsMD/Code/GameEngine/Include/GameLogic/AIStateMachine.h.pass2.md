# GeneralsMD/Code/GameEngine/Include/GameLogic/AIStateMachine.h - Enhanced Analysis

## Architectural Role
This file defines the core AI state machine framework, serving as the foundation for all unit behaviors in the game. It bridges the game logic layer with the state machine infrastructure, enabling modular AI behavior composition.

## Cross-References
### Incoming
- AI behavior controllers (e.g., `AIGroup`, `Squad`) use this state machine
- Game logic systems (e.g., `Team`) reference state transition conditions
- Weapon systems call `outOfWeaponRangeObject/Position` for targeting logic

### Outgoing
- Relies on `StateMachine` base class for core state machine functionality
- Uses `AudioEventRTS` for sound event triggers during state transitions
- Interacts with `TerrainLogic` for pathfinding and movement constraints

## Design Patterns
- **State Pattern**: Core implementation uses state objects for behavior encapsulation
- **Composite Pattern**: Nested state machines (e.g., `AIGuardMachine`) for hierarchical behavior
- **Strategy Pattern**: State transition conditions (`outOfWeaponRangeObject`) as interchangeable strategies
