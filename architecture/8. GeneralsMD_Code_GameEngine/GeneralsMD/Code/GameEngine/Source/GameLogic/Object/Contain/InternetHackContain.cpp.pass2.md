# GeneralsMD/Code/GameEngine/Source/GameLogic/Object/Contain/InternetHackContain.cpp - Enhanced Analysis

## Architectural Role
This file implements a specialized containment module that integrates AI behavior with object containment. It bridges the AI system (via `aiHackInternet`) with the containment system (`TransportContain`), demonstrating how modular behavior can be attached to objects in the SAGE engine.

## Cross-References
### Incoming
- Likely called by `Object` or `Thing` subclasses that use containment (e.g., vehicles, buildings)
- AI system may reference this for hacking behavior validation

### Outgoing
- Directly calls `TransportContain` parent class methods
- Invokes `aiHackInternet` on the rider's AI controller
- Uses `Xfer` for serialization (network/load-save)

## Design Patterns
- **Template Method**: Extends `TransportContain` by overriding `onContaining` to add hacking behavior
- **Inheritance**: Specializes base containment module with AI-specific logic
- **Command Pattern**: `aiHackInternet` likely represents a deferred AI command (inferred from `CMD_FROM_AI`)

*Not inferable*: Exact relationship with networking layer or how `aiHackInternet` is synchronized across clients.
