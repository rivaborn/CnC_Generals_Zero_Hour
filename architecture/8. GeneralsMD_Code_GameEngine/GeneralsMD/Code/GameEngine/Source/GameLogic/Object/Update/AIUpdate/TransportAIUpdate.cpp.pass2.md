# GeneralsMD/Code/GameEngine/Source/GameLogic/Object/Update/AIUpdate/TransportAIUpdate.cpp - Enhanced Analysis

## Architectural Role
This file implements the AI behavior for transport units in the SAGE engine, specifically handling passenger attack delegation and evacuation logic. It extends the base `AIUpdateInterface` to provide transport-specific functionality, bridging the gap between the AI system and the containment module.

## Cross-References
### Incoming
- `AssaultTransportAIUpdate.cpp` (inherits and extends this class)
- `RailedTransportAIUpdate.cpp` (references similar patterns)

### Outgoing
- `ContainModule.h` (for passenger management)
- `BehaviorModule.h` (for AI state machine integration)
- `AIUpdateInterface` (base class methods)

## Design Patterns
- **Template Method**: Overrides base class attack methods to add passenger delegation logic before calling parent implementations.
- **Composite**: Manages a collection of passenger objects and delegates behavior to them when appropriate.
- **State**: Uses `AIStateMachine` for transport-specific state transitions (e.g., evacuation).

Rules followed. Output under 400 tokens.
