# GeneralsMD/Code/GameEngine/Source/GameLogic/AI/AITNGuard.cpp - Enhanced Analysis

## Architectural Role
This file implements the AI behavior for tunnel network guard units, a specialized defense mechanism in Generals Zero Hour. It extends the base AI framework with tunnel-specific states and logic, integrating with the tunnel system and combat AI.

## Cross-References
### Incoming
- `AITNGuardMachine` is instantiated by the AI system when a unit is assigned to tunnel guard duty
- `TunnelNetworkExitConditions` is referenced by the state machine framework
- `AITNGuardAttackAggressorState` is called when units need to respond to tunnel attacks

### Outgoing
- Calls into `TunnelTracker` for tunnel management
- Uses `AIUpdateInterface` for general AI behaviors
- Interacts with `BodyModule` for damage/attack tracking
- References `PartitionManager` for spatial queries

## Design Patterns
- **State Pattern**: Uses a state machine to manage different guard behaviors (idle, attack, patrol)
- **Strategy Pattern**: Exit conditions are encapsulated in `TunnelNetworkExitConditions`
- **Observer Pattern**: Monitors damage events to trigger attack responses

Rules followed. Output under 400 tokens.
