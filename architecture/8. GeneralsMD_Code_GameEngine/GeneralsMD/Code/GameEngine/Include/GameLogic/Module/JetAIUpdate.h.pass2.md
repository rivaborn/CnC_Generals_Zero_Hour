# GeneralsMD/Code/GameEngine/Include/GameLogic/Module/JetAIUpdate.h - Enhanced Analysis

## Architectural Role
This file defines the AI behavior module for jet aircraft in the SAGE engine, extending the base `AIUpdateInterface`. It handles jet-specific states (takeoff/landing/taxiing) and integrates with the locomotion, targeting, and audio systems.

## Cross-References
### Incoming
- Called by `AIStateMachine` for state transitions
- Used by `Thing` objects (jets) for AI updates
- Referenced in `AICommandParms` processing

### Outgoing
- Calls `AIStateMachine` methods for state management
- Uses `AudioEventRTS` for afterburner sounds
- Interacts with `LocomotorSetType` for movement logic

## Design Patterns
- **Strategy Pattern**: `chooseLocomotorSet` dynamically selects movement behavior
- **State Pattern**: Manages jet states via `AIStateMachine` integration
- **Observer Pattern**: Tracks targeters via `m_targetedBy` list

*Not inferable*: Exact memory pool implementation details.
