# GeneralsMD/Code/GameEngine/Source/GameLogic/Object/Update/EMPUpdate.cpp - Enhanced Analysis

## Architectural Role
This file implements specialized update modules for EMP effects and leaflet drops, extending the game's object behavior system. It handles temporal effects (growth/fading), spatial queries (radius-based target detection), and particle system integration, bridging game logic with rendering and physics subsystems.

## Cross-References
### Incoming
- Called by object update loops (via `UpdateModule` base class)
- Referenced in INI-based module definitions (data-driven configuration)
- Used by particle system manager for effect attachment

### Outgoing
- Queries `ThePartitionManager` for spatial object searches
- Interacts with `TheParticleSystemManager` for visual effects
- Modifies `Drawable` properties (tinting, scaling)
- Accesses `TheGameLogic` for frame timing and object lifecycle

## Design Patterns
- **Module Pattern**: Encapsulates behavior in self-contained update modules
- **Data-Driven Design**: Relies on external `*ModuleData` structs for configuration
- **Observer Pattern**: Reacts to object state changes (e.g., `onDie` callback)
