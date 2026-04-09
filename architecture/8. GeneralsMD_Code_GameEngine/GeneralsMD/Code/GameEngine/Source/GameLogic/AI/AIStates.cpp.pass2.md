# GeneralsMD/Code/GameEngine/Source/GameLogic/AI/AIStates.cpp - Enhanced Analysis

## Architectural Role
This file implements the core AI state machine behavior for units in the SAGE engine. It handles attack logic, target acquisition, and state transitions, serving as the bridge between high-level AI commands and low-level unit actions.

## Cross-References
### Incoming
- **AIStateMachine.cpp**: Uses state definitions from this file
- **Unit.cpp**: Calls state update functions during unit processing
- **ScriptEngine.cpp**: References state IDs for scripted behaviors

### Outgoing
- **Locomotor.cpp**: Calls movement-related functions
- **Weapon.cpp**: Uses attack feasibility checks
- **PartitionManager.cpp**: Uses spatial queries for target finding
- **GameAudio.cpp**: Triggers audio events during state transitions

## Design Patterns
- **State Pattern**: Implements behavior states with clear entry/exit/update methods
- **Command Pattern**: Uses AICommandParms to encapsulate AI directives
- **Observer Pattern**: State machines react to game events (e.g., target acquisition)

Rules followed. Output under 400 tokens.
