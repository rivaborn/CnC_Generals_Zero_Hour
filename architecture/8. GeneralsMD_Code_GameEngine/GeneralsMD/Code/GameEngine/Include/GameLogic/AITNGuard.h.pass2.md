# GeneralsMD/Code/GameEngine/Include/GameLogic/AITNGuard.h - Enhanced Analysis

## Architectural Role
This file defines the AI state machine for tunnel network guard behavior, a specialized AI subsystem for units guarding strategic positions. It integrates with the broader AI framework (AIStateMachine.h) and object system (Object.h), providing guard-specific logic that can be triggered by other AI systems or player commands.

## Cross-References
### Incoming
- AI subsystem (likely AI.h) - uses guard states for unit behavior
- Object system - attaches guard behavior to game objects
- Player input/command system - may trigger guard mode activation

### Outgoing
- AIStateMachine.h - inherits from StateMachine and State classes
- GameLogic.h - likely uses game logic utilities for target scanning
- AIAttackState - delegates attack behavior to specialized attack states

## Design Patterns
- **State Pattern** - Implements guard behavior as discrete states (Inner, Idle, Outer, etc.) with clear transitions
- **Strategy Pattern** - TunnelNetworkExitConditions encapsulates exit logic as a strategy that can be reused across states
- **Composite Pattern** - Guard states contain references to AIAttackState, composing attack behavior into guard states

Rules followed. Output under 400 tokens.
