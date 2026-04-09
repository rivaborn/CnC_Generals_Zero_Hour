# GeneralsMD/Code/GameEngine/Include/GameLogic/Module/DozerAIUpdate.h - Enhanced Analysis

## Architectural Role
This file defines the core AI behavior for Dozer units, bridging the gap between high-level AI commands and low-level unit actions. It implements a state machine pattern to manage construction, repair, and fortification tasks while coordinating with the game's physics and audio systems.

## Cross-References
### Incoming
- `AIUpdate.h` (base class)
- `AudioEventRTS` (sound events)
- `StateMachine` (state transition framework)
- `ThingTemplate`, `Coord3D`, `Player` (game object types)

### Outgoing
- Calls into `Xfer` for serialization
- Uses `MultiIniFieldParse` for configuration
- Interacts with `Object` hierarchy for construction/repair targets

## Design Patterns
- **State Machine**: Manages Dozer behavior transitions (e.g., build â repair)
- **Strategy Pattern**: Task-specific behaviors (build/repair/fortify) encapsulated in methods
- **Observer Pattern**: Task completion/cancellation notifications via virtual methods

*Not inferable*: Exact serialization mechanism or memory pool integration details.
