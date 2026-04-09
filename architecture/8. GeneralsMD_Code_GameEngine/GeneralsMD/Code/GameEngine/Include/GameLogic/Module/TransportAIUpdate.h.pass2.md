# GeneralsMD/Code/GameEngine/Include/GameLogic/Module/TransportAIUpdate.h - Enhanced Analysis

## Architectural Role
This file defines the base AI behavior for transport units in the SAGE engine, bridging the generic AIUpdate system with transport-specific logic (e.g., soldier evacuation, occupant coordination). It serves as a parent class for specialized transports (e.g., AssaultTransportAIUpdate, RailedTransportAIUpdate).

## Cross-References
### Incoming
- **AssaultTransportAIUpdate.h**: Inherits and extends TransportAIUpdate for assault-specific behavior.
- **RailedTransportAIUpdate.h**: Inherits for rail-based transport logic.
- **AIUpdate.h**: Parent class interface.

### Outgoing
- **AIUpdateInterface**: Base class for AI behavior.
- **Memory pool macros**: SAGE engine utilities for object management.

## Design Patterns
- **Template Method**: `makeStateMachine()` and attack methods define hooks for subclasses to customize behavior.
- **Inheritance Hierarchy**: Serves as a base class for transport-specific AI modules.
- **Module System**: Uses SAGE's module macros for runtime registration and memory management.
