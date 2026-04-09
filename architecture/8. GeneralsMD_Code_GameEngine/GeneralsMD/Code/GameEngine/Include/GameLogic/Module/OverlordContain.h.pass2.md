# GeneralsMD/Code/GameEngine/Include/GameLogic/Module/OverlordContain.h - Enhanced Analysis

## Architectural Role
This file defines the `OverlordContain` module, a specialized transport container that implements a redirection pattern when full. It bridges the containment system with the game's object hierarchy, enabling units like the Overlord (GLA's mobile bunker) to delegate containment logic to its first passenger when full.

## Cross-References
### Incoming
- **GameLogic/Module/TransportContain.h**: Base class for containment behavior
- **GameLogic/GameLogic.h**: Core game logic interfaces and types
- **MultiIniFieldParse, INI**: Configuration parsing infrastructure
- **Memory pool macros**: Engine-wide object management

### Outgoing
- **ContainModuleInterface**: For redirection delegation
- **Object, Player, DamageInfo**: Core game entities
- **Draw module**: Friend access for rendering order workarounds

## Design Patterns
- **Proxy Pattern**: Redirects containment queries to the first passenger when full, decoupling the container from direct management.
- **Template Method**: Uses `buildFieldParse` and `parseInitialPayload` for configuration-driven behavior.
- **Strategy Variant**: Overrides multiple `Contain` virtual methods to customize behavior (e.g., `isPassengerAllowedToFire`).
