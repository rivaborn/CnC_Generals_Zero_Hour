# GeneralsMD/Code/GameEngine/Include/GameLogic/Module/DamageModule.h - Enhanced Analysis

## Architectural Role
This file defines the core damage handling interface for the SAGE engine's entity component system. It serves as the foundation for all damage-related behavior in game objects, bridging the gap between damage application logic and object-specific responses.

## Cross-References
### Incoming
- `GameLogic/Damage.h` (uses `DamageInfo` struct)
- `GameLogic/Module/BehaviorModule.h` (inherits from `BehaviorModule`)
- Various derived damage modules (e.g., vehicle/building-specific implementations)

### Outgoing
- `Common/Module.h` (inherits from `Module`)
- `BehaviorModuleData` (extends for configuration)
- `DamageInfo` processing (passed to callbacks)

## Design Patterns
- **Interface Segregation**: `DamageModuleInterface` isolates damage-specific callbacks
- **Template Method**: `buildFieldParse` extends parsing behavior while maintaining base functionality
- **Component Pattern**: Damage handling is modularized as a separate component

*Not inferable*: Exact memory pool implementation details or `BodyDamageType` enum values.
