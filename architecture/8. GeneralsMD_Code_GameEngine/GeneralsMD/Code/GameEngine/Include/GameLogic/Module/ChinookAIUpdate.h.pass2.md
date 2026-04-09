# GeneralsMD/Code/GameEngine/Include/GameLogic/Module/ChinookAIUpdate.h - Enhanced Analysis

## Architectural Role
This file defines the AI behavior for Chinook helicopters, extending the supply truck AI base class. It handles flight states, supply operations, and combat behaviors, acting as a bridge between the generic transport AI and Chinook-specific mechanics.

## Cross-References
### Incoming
- **AI System**: Calls `update()` and `aiDoCommand()` for state management
- **Command System**: Uses `AICommandParms` for command processing
- **Transport System**: Overrides methods from `SupplyTruckAIUpdate` for specialized behavior

### Outgoing
- **State Machine**: Uses `AIStateMachine` for behavior sequencing
- **Object System**: Interacts with `Object` instances for targets and occupants
- **Particle System**: References particle effects for rotor wash

## Design Patterns
- **Template Method**: Overrides base class methods (`update()`, `aiDoCommand()`) to extend behavior
- **State Pattern**: Uses `ChinookFlightStatus` enum to manage flight states via state machine
- **Composition**: Embeds `ChinookAIUpdateModuleData` for configuration, separating data from logic

*Not inferable*: Exact state machine implementation details or particle system integration.
