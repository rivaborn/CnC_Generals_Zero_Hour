# GeneralsMD/Code/GameEngine/Include/GameLogic/Module/WorkerAIUpdate.h - Enhanced Analysis

## Architectural Role
This file defines the core AI logic for worker units, acting as a bridge between dozer and supply truck behaviors. It implements a hybrid state machine system where workers can dynamically switch between construction and supply delivery roles, reflecting the game's dual-purpose worker design.

## Cross-References
### Incoming
- **Player Command System**: Calls `aiDoCommand()` to handle player-issued orders
- **Game Logic Update Loop**: Calls `update()` during the AI update phase
- **Construction/Repair Systems**: Calls `privateRepair()` and `privateResumeConstruction()` when workers interact with buildings

### Outgoing
- **Dozer AI System**: Inherits from `DozerAIInterface` and uses `DozerPrimaryStateMachine`
- **Supply Truck AI System**: Inherits from `SupplyTruckAIInterface` and uses `SupplyTruckStateMachine`
- **State Machine Framework**: Uses `StateMachine` base class for behavior management
- **Audio System**: Plays construction and supply-related sound events

## Design Patterns
- **State Pattern**: Uses nested state machines (`WorkerStateMachine`, `DozerPrimaryStateMachine`, `SupplyTruckStateMachine`) to manage worker behaviors
- **Strategy Pattern**: Different task behaviors (repair, construction, supply delivery) are encapsulated in separate methods
- **Composite Pattern**: Worker AI aggregates both dozer and supply truck behaviors into a single unit

**Note**: The comment "Holy Fuck" in the file header suggests this dual-role design was particularly challenging to implement.
